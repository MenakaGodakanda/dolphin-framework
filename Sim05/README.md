# Simulation 05 Output

## Video:


## Detailed Output:
```
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ python src/core/main.py --mode simulate --duration 240
2025-08-13 18:04:42,645 - INFO - DOLPHIN Framework initialized successfully
2025-08-13 18:04:42,646 - INFO - Starting DOLPHIN Framework...
2025-08-13 18:04:42,647 - INFO - Deployed 3 baseline honeytokens
2025-08-13 18:04:42,661 - INFO - DOLPHIN Framework started successfully
2025-08-13 18:04:42,661 - INFO - Starting combined attack simulation for 240 seconds
2025-08-13 18:04:42,662 - INFO - Attack simulation 1
Running combined attack simulation for 240 seconds...
Collecting detailed performance metrics...
Press Ctrl+C to stop early.
2025-08-13 18:05:07,184 - INFO - Attack 1 completed - Honeytokens triggered: 4
2025-08-13 18:05:28,616 - INFO - Attack simulation 2
2025-08-13 18:05:45,321 - INFO - Attack 2 completed - Honeytokens triggered: 1
2025-08-13 18:05:57,229 - INFO - Attack simulation 3
2025-08-13 18:06:23,144 - INFO - Attack 3 completed - Honeytokens triggered: 3
2025-08-13 18:06:34,163 - INFO - Attack simulation 4
2025-08-13 18:07:00,428 - INFO - Attack 4 completed - Honeytokens triggered: 4
2025-08-13 18:07:28,373 - INFO - Attack simulation 5
2025-08-13 18:07:47,642 - INFO - Attack 5 completed - Honeytokens triggered: 3
2025-08-13 18:08:13,177 - INFO - Attack simulation 6
2025-08-13 18:08:34,825 - INFO - Attack 6 completed - Honeytokens triggered: 4
2025-08-13 18:09:04,142 - INFO - Stopping DOLPHIN Framework...

================================================================================
DOLPHIN FRAMEWORK - COMPREHENSIVE RESULTS ANALYSIS
================================================================================

Table - Experimental Results Summary
--------------------------------------------------
Detection Success Rate        : 100.00%
Q-Learning Convergence        : Converged
Baseline Honeytoken Triggers  : 0
Dynamic Honeytoken Triggers   : 20
False Positive Rate           : 0.00%
Response Latency (Recon)      : 0.000s
Response Latency (Direct)     : 0.000s
CPU Overhead                  : 0.43%
Memory Usage                  : 67.18%
Disk I/O Overhead             : 22314.74 MB/s
Network Overhead              : 1573487.31 KB/s
Average Episode Reward        : 26.989
Extended Engagement Time      : 0.00s

--------------------------------------------------

Q-Learning Performance Progression
==================================================

Reward Range: 26.701 to 27.492

 27.49 |          ****                                              
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |  *******                                                   
       |**       *                                                  
 27.10 |                                                            
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |                                                            
 26.70 |              *************                                 
       ------------------------------------------------------------
       0                                                  27
       Episodes


Honeytoken Effectiveness Analysis
==================================================

Reconnaissance Token:
  Total Triggers: 9 (45.0%)
  Reconnaissance: 9
  Exfiltration: 0
  Other: 0

Exfiltration Token:
  Total Triggers: 11 (55.0%)
  Reconnaissance: 0
  Exfiltration: 11
  Other: 0


Attack Sequence Timeline Analysis
============================================================

Attack Sequence #1 - 18:05:07
----------------------------------------

Reconnaissance Phase:
  Duration: 12.05 seconds
  Files Accessed: 2
    18:04:42 - data/archive/log_20250813_155542_temp.txt_1755071744
    18:04:45 - data/dynamic/calib_20250813_174648_temp.csv
  Honeytokens Triggered: calib_20250813_174648_temp.csv
  Phase Success: True

Data Exfiltration Phase:
  Duration: 8.86 seconds
  Files Accessed: 3
    18:04:58 - data/archive/robot_config_backup.yaml_1755071783
    18:05:01 - data/baseline/robot_config_backup.yaml
    18:05:02 - data/archive/robot_config_backup.yaml_1755078408
  Honeytokens Triggered: robot_config_backup.yaml_1755071783, robot_config_backup.yaml, robot_config_backup.yaml_1755078408
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #2 - 18:05:45
----------------------------------------

Reconnaissance Phase:
  Duration: 8.92 seconds
  Files Accessed: 1
    18:05:28 - data/dynamic/robot_20250813_155826_default.cfg
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 5.49 seconds
  Files Accessed: 1
    18:05:40 - data/archive/robot_config_backup.yaml_1755072712
  Honeytokens Triggered: robot_config_backup.yaml_1755072712
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 1

Attack Sequence #3 - 18:06:23
----------------------------------------

Reconnaissance Phase:
  Duration: 14.66 seconds
  Files Accessed: 3
    18:05:57 - data/genuine/current_sensor_data.json
    18:06:00 - data/archive/system_log_archive.txt_1755072712.meta
    18:06:06 - data/baseline/robot_config_backup.yaml
  Honeytokens Triggered: system_log_archive.txt_1755072712.meta, robot_config_backup.yaml
  Phase Success: True

Data Exfiltration Phase:
  Duration: 7.21 seconds
  Files Accessed: 2
    18:06:16 - data/archive/robot_config_backup.yaml_1755072712.meta
    18:06:18 - data/baseline/robot_config_backup.yaml
  Honeytokens Triggered: robot_config_backup.yaml_1755072712.meta, robot_config_backup.yaml
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #4 - 18:07:00
----------------------------------------

Reconnaissance Phase:
  Duration: 18.26 seconds
  Files Accessed: 3
    18:06:34 - data/dynamic/data_20250813_160440_backup.json
    18:06:36 - data/archive/system_log_archive.txt_1755071733
    18:06:43 - data/archive/system_log_archive.txt_1755071783
  Honeytokens Triggered: data_20250813_160440_backup.json, system_log_archive.txt_1755071733, system_log_archive.txt_1755071783
  Phase Success: True

Data Exfiltration Phase:
  Duration: 4.73 seconds
  Files Accessed: 1
    18:06:55 - data/archive/robot_config_backup.yaml_1755071733.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #5 - 18:07:47
----------------------------------------

Reconnaissance Phase:
  Duration: 8.19 seconds
  Files Accessed: 1
    18:07:28 - data/archive/sensor_calibration.json_1755079566.meta
  Honeytokens Triggered: sensor_calibration.json_1755079566.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 6.92 seconds
  Files Accessed: 2
    18:07:41 - data/archive/robot_config_backup.yaml_1755072712
    18:07:46 - data/archive/robot_config_backup.yaml_1755078408
  Honeytokens Triggered: robot_config_backup.yaml_1755072712, robot_config_backup.yaml_1755078408
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #6 - 18:08:34
----------------------------------------

Reconnaissance Phase:
  Duration: 12.84 seconds
  Files Accessed: 2
    18:08:13 - data/dynamic/calib_20250813_160440_old.json
    18:08:20 - data/archive/sensor_calibration.json_1755071744.meta
  Honeytokens Triggered: calib_20250813_160440_old.json, sensor_calibration.json_1755071744.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 4.32 seconds
  Files Accessed: 2
    18:08:30 - data/archive/robot_config_backup.yaml_1755072712
    18:08:32 - data/archive/robot_config_backup.yaml_1755079578.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755072712, robot_config_backup.yaml_1755079578.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4


Additional Framework Statistics
========================================
Total Runtime: 270.36 seconds (4.5 minutes)
Total Detection Events: 6
Total Honeytoken Triggers: 20
Total Attack Sequences: 6
Q-Learning Episodes Completed: 27
Average CPU Usage: 0.43%
Average Memory Usage: 67.18%

Learned Policy Summary
------------------------------
State (2, 3, 0): emergency_cleanup (Value: 2.500)
State (3, 2, 0): deploy_additional (Value: 14.599)
State (3, 5, 0): deploy_additional (Value: 20.494)
State (3, 8, 0): cleanup_oldest (Value: 21.712)
State (3, 7, 0): cleanup_oldest (Value: 17.138)
State (3, 6, 0): deploy_additional (Value: 13.342)
State (3, 9, 0): deploy_additional (Value: 14.633)
State (3, 10, 0): deploy_baseline (Value: 37.914)
State (3, 3, 0): maintain_current (Value: 5.572)

================================================================================
END OF RESULTS ANALYSIS
================================================================================

Detailed results saved to: logs/dolphin_results_20250813_180913.json
2025-08-13 18:09:13,011 - INFO - DOLPHIN Framework stopped
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ 
```
