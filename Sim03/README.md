# Simulation 03 Output

## Video:


https://github.com/user-attachments/assets/5495c9ed-42f7-4f95-8376-55ac23174210



## Detailed Output:
```

(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ python src/core/main.py --mode simulate --duration 240
2025-08-13 16:11:28,042 - INFO - DOLPHIN Framework initialized successfully
2025-08-13 16:11:28,043 - INFO - Starting DOLPHIN Framework...
2025-08-13 16:11:28,044 - INFO - Deployed 3 baseline honeytokens
2025-08-13 16:11:28,046 - INFO - DOLPHIN Framework started successfully
2025-08-13 16:11:28,046 - INFO - Starting combined attack simulation for 240 seconds
Running combined attack simulation for 240 seconds...
Collecting detailed performance metrics...
Press Ctrl+C to stop early.
2025-08-13 16:11:28,047 - INFO - Attack simulation 1
2025-08-13 16:11:55,153 - INFO - Attack 1 completed - Honeytokens triggered: 4
2025-08-13 16:12:23,041 - INFO - Attack simulation 2
2025-08-13 16:12:49,104 - INFO - Attack 2 completed - Honeytokens triggered: 2
2025-08-13 16:13:04,709 - INFO - Attack simulation 3
2025-08-13 16:13:32,071 - INFO - Attack 3 completed - Honeytokens triggered: 3
2025-08-13 16:13:45,649 - INFO - Attack simulation 4
2025-08-13 16:14:03,101 - INFO - Attack 4 completed - Honeytokens triggered: 2
2025-08-13 16:14:26,152 - INFO - Attack simulation 5
2025-08-13 16:14:47,678 - INFO - Attack 5 completed - Honeytokens triggered: 3
2025-08-13 16:15:03,704 - INFO - Attack simulation 6
2025-08-13 16:15:29,539 - INFO - Attack 6 completed - Honeytokens triggered: 3
2025-08-13 16:15:44,204 - INFO - Stopping DOLPHIN Framework...

================================================================================
DOLPHIN FRAMEWORK - COMPREHENSIVE RESULTS ANALYSIS
================================================================================

Table - Experimental Results Summary
--------------------------------------------------
Detection Success Rate        : 100.00%
Q-Learning Convergence        : Converged
Baseline Honeytoken Triggers  : 0
Dynamic Honeytoken Triggers   : 18
False Positive Rate           : 0.00%
Response Latency (Recon)      : 0.000s
Response Latency (Direct)     : 0.000s
CPU Overhead                  : 0.58%
Memory Usage                  : 66.31%
Disk I/O Overhead             : 22104.10 MB/s
Network Overhead              : 1570483.07 KB/s
Average Episode Reward        : 27.002
Extended Engagement Time      : 0.00s

--------------------------------------------------

Q-Learning Performance Progression
==================================================

Reward Range: 26.333 to 27.508

 27.51 |   *********                                                
       |                                                            
       |                                                            
       |                                                            
       |***         ****                                            
       |                                                            
       |                                                            
 26.92 |                                                            
       |                                                            
       |                ****                                        
       |                                                            
       |                                                            
       |                                                            
       |                                                            
 26.33 |                    ******                                  
       ------------------------------------------------------------
       0                                                  26
       Episodes


Honeytoken Effectiveness Analysis
==================================================

Reconnaissance Token:
  Total Triggers: 6 (33.3%)
  Reconnaissance: 6
  Exfiltration: 0
  Other: 0

Exfiltration Token:
  Total Triggers: 12 (66.7%)
  Reconnaissance: 0
  Exfiltration: 12
  Other: 0


Attack Sequence Timeline Analysis
============================================================

Attack Sequence #1 - 16:11:55
----------------------------------------

Reconnaissance Phase:
  Duration: 14.24 seconds
  Files Accessed: 2
    16:11:28 - data/archive/params_20250813_155533_backup.yml_1755071733.meta
    16:11:34 - data/baseline/robot_config_backup.yaml
  Honeytokens Triggered: params_20250813_155533_backup.yml_1755071733.meta, robot_config_backup.yaml
  Phase Success: True

Data Exfiltration Phase:
  Duration: 9.90 seconds
  Files Accessed: 3
    16:11:45 - data/archive/robot_config_backup.yaml_1755071733
    16:11:50 - data/archive/robot_config_backup.yaml_1755071783.meta
    16:11:52 - data/baseline/robot_config_backup.yaml
  Honeytokens Triggered: robot_config_backup.yaml_1755071733, robot_config_backup.yaml_1755071783.meta, robot_config_backup.yaml
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #2 - 16:12:49
----------------------------------------

Reconnaissance Phase:
  Duration: 14.12 seconds
  Files Accessed: 2
    16:12:23 - data/dynamic/sensor_20250813_160440_old.csv
    16:12:28 - data/archive/params_20250813_155533_default.yaml_1755071733.meta
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 7.81 seconds
  Files Accessed: 2
    16:12:41 - data/archive/robot_config_backup.yaml_1755072712.meta
    16:12:45 - data/archive/robot_config_backup.yaml_1755071733
  Honeytokens Triggered: robot_config_backup.yaml_1755072712.meta, robot_config_backup.yaml_1755071733
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #3 - 16:13:32
----------------------------------------

Reconnaissance Phase:
  Duration: 14.26 seconds
  Files Accessed: 2
    16:13:04 - data/archive/log_20250813_155533_backup.txt_1755071733
    16:13:10 - data/archive/sensor_20250813_155544_old.json_1755071744
  Honeytokens Triggered: log_20250813_155533_backup.txt_1755071733
  Phase Success: True

Data Exfiltration Phase:
  Duration: 9.18 seconds
  Files Accessed: 2
    16:13:23 - data/archive/robot_config_backup.yaml_1755071733
    16:13:27 - data/archive/robot_config_backup.yaml_1755072712.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733, robot_config_backup.yaml_1755072712.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #4 - 16:14:03
----------------------------------------

Reconnaissance Phase:
  Duration: 8.63 seconds
  Files Accessed: 1
    16:13:45 - data/archive/log_20250813_155623_temp.txt_1755071896
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 6.49 seconds
  Files Accessed: 2
    16:13:56 - data/archive/robot_config_backup.yaml_1755071733.meta
    16:13:59 - data/archive/robot_config_backup.yaml_1755071783
  Honeytokens Triggered: robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071783
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #5 - 16:14:47
----------------------------------------

Reconnaissance Phase:
  Duration: 13.80 seconds
  Files Accessed: 2
    16:14:26 - data/archive/system_log_archive.txt_1755072712.meta
    16:14:32 - data/archive/params_20250813_155544_default.yml_1755071744.meta
  Honeytokens Triggered: system_log_archive.txt_1755072712.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 5.69 seconds
  Files Accessed: 2
    16:14:42 - data/archive/robot_config_backup.yaml_1755071783
    16:14:44 - data/archive/robot_config_backup.yaml_1755071733.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071783, robot_config_backup.yaml_1755071733.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #6 - 16:15:29
----------------------------------------

Reconnaissance Phase:
  Duration: 16.68 seconds
  Files Accessed: 2
    16:15:03 - data/archive/system_log_archive.txt_1755071733
    16:15:10 - data/archive/params_20250813_155542_backup.yaml_1755071744.meta
  Honeytokens Triggered: system_log_archive.txt_1755071733, params_20250813_155542_backup.yaml_1755071744.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 4.96 seconds
  Files Accessed: 1
    16:15:24 - data/archive/robot_config_backup.yaml_1755071783
  Honeytokens Triggered: robot_config_backup.yaml_1755071783
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3


Additional Framework Statistics
========================================
Total Runtime: 260.30 seconds (4.3 minutes)
Total Detection Events: 6
Total Honeytoken Triggers: 18
Total Attack Sequences: 6
Q-Learning Episodes Completed: 26
Average CPU Usage: 0.58%
Average Memory Usage: 66.31%

Learned Policy Summary
------------------------------
State (2, 3, 0): emergency_cleanup (Value: 4.750)
State (3, 2, 0): deploy_additional (Value: 14.599)
State (3, 5, 0): deploy_additional (Value: 20.494)
State (3, 8, 0): cleanup_oldest (Value: 21.712)
State (3, 7, 0): cleanup_oldest (Value: 17.138)
State (3, 6, 0): deploy_additional (Value: 13.342)
State (3, 9, 0): deploy_additional (Value: 14.633)
State (3, 10, 0): deploy_baseline (Value: 37.914)

================================================================================
END OF RESULTS ANALYSIS
================================================================================

Detailed results saved to: logs/dolphin_results_20250813_161548.json
2025-08-13 16:15:48,344 - INFO - DOLPHIN Framework stopped
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ 

```
