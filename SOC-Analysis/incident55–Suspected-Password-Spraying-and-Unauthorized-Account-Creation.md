# Incident 55 – Suspected Password Spraying and Unauthorized Account Creation

## Source Log

```text
07:55 User admin logged in from 10.0.0.5
07:57 GET /dashboard 200 from 10.0.0.5
08:00 User admin logged out from 10.0.0.5
10:12 Failed login for user hr_user from 192.168.1.210
10:13 Failed login for user finance_user from 192.168.1.210
10:14 Failed login for user support_user from 192.168.1.210
10:15 Failed login for user admin from 192.168.1.210
10:18 User support_user logged in from 192.168.1.210
10:20 GET /tickets 200 from 192.168.1.210
10:22 GET /users 200 from 192.168.1.210
10:25 POST /password-reset 200 from 192.168.1.210 target=admin
10:29 User admin logged in from 192.168.1.210
10:31 GET /admin 200 from 192.168.1.210
10:33 GET /config 200 from 192.168.1.210
10:36 POST /users/create 201 from 192.168.1.210 user=backup_admin
10:40 User admin logged out from 192.168.1.210
13:05 User admin logged in from 10.0.0.5
13:07 GET /users 200 from 10.0.0.5
13:09 GET /logs 200 from 10.0.0.5
```

## Initial Analysis

### A1 – Observed

* At 07:55, `admin` logged in from `10.0.0.5` and accessed `/dashboard`.
* The account logged out at 08:00.
* Failed login attempts for `hr_user`, `finance_user`, `support_user`, and `admin` were observed from `192.168.1.210`.
* At 10:18, `support_user` logged in from `192.168.1.210`.
* The account accessed `/tickets` and `/users`.
* A password-reset request targeting the `admin` account was made from the same IP address.
* At 10:29, `admin` logged in from `192.168.1.210`.
* The account accessed `/admin` and `/config`.
* A request to create the user `backup_admin` returned HTTP status `201`.
* At 10:40, `admin` logged out.
* At 13:05, `admin` logged in from `10.0.0.5` and accessed `/users` and `/logs`.

### A2 – Assessment

The activity may represent a password-spraying attempt against several accounts. After the successful `support_user` login, the same source requested an admin password reset, logged in as `admin`,
accessed administrative resources, and created `backup_admin`.

This sequence suggests possible account compromise followed by unauthorized privileged access and the creation of an account that could provide persistent access.

An alternative explanation is authorized administrative or security-testing activity performed from an internal system.

The later access to `/users` and `/logs` from `10.0.0.5` may represent an investigation by the legitimate administrator, but its purpose cannot be confirmed from the available log.

### A3 – Confidence

**Medium**

The sequence strongly suggests account compromise because failed login attempts were followed by a successful `support_user` login, an admin password reset, an admin login, and the creation of `backup_admin`.

However, the available evidence does not show whether these actions were authorized or who controlled `192.168.1.210`.

### A4 – Key Unknown

The key unknown is whether the admin password reset and the creation of `backup_admin` were authorized administrative actions.

Additional unknowns include:

* Who controlled `192.168.1.210`?
* Was the admin password changed successfully?
* What permissions were assigned to `backup_admin`?
* Was `backup_admin` used after its creation?
* Was the later activity from `10.0.0.5` an investigation or normal administrative activity?

---

## Incident Report

## Executive Summary

Multiple failed login attempts targeting four different accounts were observed from `192.168.1.210`. The attempts were followed by a successful `support_user` login from the same source.

The source subsequently requested a password reset for the `admin` account, authenticated as `admin`, accessed administrative resources, and successfully submitted a request to create `backup_admin`.

The sequence is consistent with possible password spraying, account compromise, privileged account access, and account creation for persistence. However,
the logs do not confirm whether the activity was unauthorized.

## IP Addresses of Interest

* `192.168.1.210` – Source of the failed login attempts, successful account access, admin password reset, privileged activity, and account creation.
* `10.0.0.5` – Source of the earlier and later admin activity.

Both addresses belong to private IP ranges. Their ownership, assigned devices, and authorized users must be established before the activity can be conclusively classified.

## Attack Type

* Suspected Password Spraying
* Potential Account Compromise
* Potential Privileged Account Abuse
* Account Manipulation
* Potential Persistence Through Account Creation

## Findings

* Four accounts were targeted by failed login attempts from `192.168.1.210`:

  * `hr_user`
  * `finance_user`
  * `support_user`
  * `admin`
* `support_user` successfully logged in from the same IP three minutes after the final failed attempt.
* The account accessed:

  * `/tickets`
  * `/users`
* A password-reset request targeting `admin` returned HTTP status `200`.
* Four minutes later, `admin` successfully logged in from the same source.
* The admin account accessed:

  * `/admin`
  * `/config`
* A request to create `backup_admin` returned HTTP status `201`, indicating that the requested resource was likely created successfully.
* The admin account logged out from `192.168.1.210` at 10:40.
* Later, `admin` logged in from `10.0.0.5` and accessed:

  * `/users`
  * `/logs`
* The purpose of the later admin activity cannot be determined from the available evidence.

## Timeline

1. **07:55–08:00** – `admin` logged in from `10.0.0.5`, accessed `/dashboard`, and logged out.
2. **10:12–10:15** – Failed login attempts targeting four different accounts were recorded from `192.168.1.210`.
3. **10:18** – `support_user` successfully logged in from `192.168.1.210`.
4. **10:20–10:22** – `/tickets` and `/users` were accessed.
5. **10:25** – A password-reset request targeting `admin` was submitted successfully.
6. **10:29** – `admin` logged in from the same IP address.
7. **10:31–10:33** – `/admin` and `/config` were accessed.
8. **10:36** – A request to create `backup_admin` returned HTTP status `201`.
9. **10:40** – `admin` logged out from `192.168.1.210`.
10. **13:05–13:09** – `admin` logged in from `10.0.0.5` and accessed `/users` and `/logs`.

## MITRE ATT&CK Mapping

### T1110.003 – Brute Force: Password Spraying

One source attempted to authenticate to several different accounts over a short period. This pattern is consistent with password spraying.

### T1078 – Valid Accounts

The `support_user` and `admin` accounts successfully authenticated from `192.168.1.210`. The log does not confirm whether valid credentials were obtained or whether the activity was authorized.

### T1098 – Account Manipulation

A password-reset request targeting the `admin` account occurred shortly before the successful admin login. This may represent account manipulation,
although the log does not explicitly confirm that the password was changed.

### T1136 – Create Account

The request to create `backup_admin` returned HTTP status `201`. The event is consistent with account creation that could be used to maintain access.

The available evidence does not identify whether `backup_admin` was a local, domain, cloud, or application account. Therefore, no more specific T1136 sub-technique can be confirmed.

## Evidence Limitations

* The logs do not identify the devices or users assigned to the two IP addresses.
* No MFA, identity-provider, endpoint, or session information is available.
* The log does not explicitly confirm that the admin password was changed.
* The permissions assigned to `backup_admin` are unknown.
* No later authentication by `backup_admin` is shown.
* The logs do not establish whether the actions were authorized.
* HTTP status codes confirm the application responses but do not establish the intent of the person performing the actions.

## Recommended Investigation Steps

1. Identify the device and user associated with `192.168.1.210`.
2. Confirm whether the activity was part of authorized administration or security testing.
3. Review authentication records for `support_user` and `admin`, including MFA results and session identifiers.
4. Confirm whether the admin password was changed at 10:25.
5. Inspect the creation time, permissions, and activity history of `backup_admin`.
6. Disable or restrict `backup_admin` if the account is not authorized.
7. Review endpoint telemetry from the device assigned to `192.168.1.210`.
8. Search for additional authentication attempts from the same source.
9. Determine whether the activity from `10.0.0.5` was an incident investigation.
10. Reset affected credentials and revoke active sessions if unauthorized access is confirmed.

## Conclusion

The activity from `192.168.1.210` is consistent with a suspected password-spraying attempt followed by possible compromise of `support_user`, manipulation of the `admin` account, privileged access,
and the creation of `backup_admin`.

The successful account-creation response raises the possibility that a new account was established to maintain access. However,
the logs do not confirm whether the activity was unauthorized or whether `backup_admin` was later used.

The incident should be treated as a high-priority investigation with medium confidence in account compromise until the ownership of `192.168.1.210`,
the authorization status of the actions, and the purpose of `backup_admin` are established.
