# Log Analysis (Intro)

## 🧠 Overview
Log analysis involves examining system and application logs to detect suspicious or abnormal activity. It is a core skill for SOC (Security Operations Center) analysts.

---

## 🔑 Key Concepts

- Log → record of events occurring in a system
- Log entry → single line in a log file
- Event → action (login, request, error, etc.)

---

## 📁 Common Log Locations

- /var/log/ → main log directory
- /etc/logrotate.d/ → log rotation configuration

---

## 🔧 Log Processing Pipeline

In this lab, logs were processed using a sequence of Linux commands:

``bash
grep → filter log entries  
sort → sort entries  
uniq → remove duplicates

## 🧪 Commands Used

cat → view file  
less → explore logs  
grep → search for patterns  
sort → sort entries  
uniq → remove duplicates  
