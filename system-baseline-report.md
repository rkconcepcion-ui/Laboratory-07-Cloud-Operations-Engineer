# System Baseline Report

## Checkpoint 2 - Establish a Host System Baseline

### 1. Memory Check

**Command Executed:**
```bash
free -h
```

**Results:**
- Total RAM: 1.9 GiB
- Used RAM: 407 MiB
- Free RAM: 1.2 GiB
- Available RAM: 1.5 GiB
- Total Swap: 1.0 GiB

### 2. Disk Storage Check

**Command Executed:**
```bash
df -h /
```

**Results:**
- Total Storage: 19G
- Used Storage: 5.4G
- Available Storage: 13G
- Disk Usage: 30%
- Mounted on: /

### 3. CPU and Process Monitoring

**Command Executed:**
```bash
top
```

The `top` command was used to monitor active processes and observe CPU and memory usage in real time.

### 4. Importance of Disk Space Monitoring

Checking disk space before a massive traffic surge is important because the server needs sufficient storage for application logs, temporary files, and other data to prevent service interruptions.

### 5. Conclusion

The host system baseline check was completed using Linux monitoring commands in the KillerCoda Ubuntu Playground. The server has 1.9 GiB of RAM and 19G of root storage, with 13G of available disk space. These measurements provide a baseline for monitoring system health during the deployment and testing of the Nginx container.
