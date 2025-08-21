# Simulation 04 Output

## Video:


https://github.com/user-attachments/assets/fc30cb84-cd55-448a-8ab2-1a49c97337ba



## Detailed Output:
```
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ python src/core/main.py --mode simulate --duration 240
2025-08-13 17:45:19,223 - INFO - DOLPHIN Framework initialized successfully
2025-08-13 17:45:19,223 - INFO - Starting DOLPHIN Framework...
2025-08-13 17:45:19,224 - INFO - Deployed 3 baseline honeytokens
2025-08-13 17:45:19,229 - INFO - DOLPHIN Framework started successfully
2025-08-13 17:45:19,229 - INFO - Starting combined attack simulation for 240 seconds
Running combined attack simulation for 240 seconds...
Collecting detailed performance metrics...
Press Ctrl+C to stop early.
2025-08-13 17:45:19,229 - INFO - Attack simulation 1
2025-08-13 17:45:39,677 - INFO - Attack 1 completed - Honeytokens triggered: 3
2025-08-13 17:46:02,058 - INFO - Attack simulation 2
2025-08-13 17:46:23,286 - INFO - Attack 2 completed - Honeytokens triggered: 2
2025-08-13 17:46:48,187 - INFO - Attack simulation 3
2025-08-13 17:47:12,040 - INFO - Attack 3 completed - Honeytokens triggered: 3
2025-08-13 17:47:25,956 - INFO - Attack simulation 4
2025-08-13 17:47:48,158 - INFO - Attack 4 completed - Honeytokens triggered: 2
2025-08-13 17:48:06,857 - INFO - Attack simulation 5
2025-08-13 17:48:37,680 - INFO - Attack 5 completed - Honeytokens triggered: 4
2025-08-13 17:48:52,036 - INFO - Attack simulation 6
2025-08-13 17:49:16,295 - INFO - Attack 6 completed - Honeytokens triggered: 4
2025-08-13 17:49:30,342 - INFO - Stopping DOLPHIN Framework...

================================================================================
DOLPHIN FRAMEWORK - COMPREHENSIVE RESULTS ANALYSIS
================================================================================

Table - Experimental Results Summary
--------------------------------------------------
Detection Success Rate        : 100.00%
Q-Learning Convergence        : Converging
Baseline Honeytoken Triggers  : 0
Dynamic Honeytoken Triggers   : 19
False Positive Rate           : 0.00%
Response Latency (Recon)      : 0.000s
Response Latency (Direct)     : 0.000s
CPU Overhead                  : 0.56%
Memory Usage                  : 66.36%
Disk I/O Overhead             : 22260.36 MB/s
Network Overhead              : 1572231.75 KB/s
Average Episode Reward        : 26.173
Extended Engagement Time      : 0.00s

--------------------------------------------------

Q-Learning Performance Progression
==================================================

Reward Range: 24.187 to 27.246

 27.25 |***********                                                 
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |           ****                                             
       |                                                            
 25.72 |                                                            
       |               *********                                    
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |                                                            
 24.19 |                        **                                  
       ------------------------------------------------------------
       0                                                  26
       Episodes


Honeytoken Effectiveness Analysis
==================================================

Reconnaissance Token:
  Total Triggers: 8 (42.1%)
  Reconnaissance: 8
  Exfiltration: 0
  Other: 0

Exfiltration Token:
  Total Triggers: 11 (57.9%)
  Reconnaissance: 0
  Exfiltration: 11
  Other: 0


Attack Sequence Timeline Analysis
============================================================

Attack Sequence #1 - 17:45:39
----------------------------------------

Reconnaissance Phase:
  Duration: 12.37 seconds
  Files Accessed: 2
    17:45:19 - data/archive/sensor_20250813_155544_backup.txt_1755071744.meta
    17:45:24 - data/archive/sensor_calibration.json_1755071729
  Honeytokens Triggered: sensor_20250813_155544_backup.txt_1755071744.meta, sensor_calibration.json_1755071729
  Phase Success: True

Data Exfiltration Phase:
  Duration: 5.12 seconds
  Files Accessed: 1
    17:45:34 - data/archive/robot_config_backup.yaml_1755071783.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071783.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #2 - 17:46:23
----------------------------------------

Reconnaissance Phase:
  Duration: 9.72 seconds
  Files Accessed: 2
    17:46:02 - data/archive/robot_config_backup.yaml_1755071733
    17:46:06 - data/archive/params_20250813_155533_template.cfg_1755071742.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733
  Phase Success: True

Data Exfiltration Phase:
  Duration: 7.57 seconds
  Files Accessed: 2
    17:46:16 - data/archive/robot_config_backup.yaml_1755072712
    17:46:18 - data/archive/robot_config_backup.yaml_1755071733
  Honeytokens Triggered: robot_config_backup.yaml_1755072712, robot_config_backup.yaml_1755071733
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #3 - 17:47:12
----------------------------------------

Reconnaissance Phase:
  Duration: 12.51 seconds
  Files Accessed: 2
    17:46:48 - data/baseline/system_log_archive.txt
    17:46:53 - data/archive/sensor_20250813_155544_old.json_1755071744.meta
  Honeytokens Triggered: system_log_archive.txt
  Phase Success: True

Data Exfiltration Phase:
  Duration: 8.24 seconds
  Files Accessed: 2
    17:47:03 - data/archive/robot_config_backup.yaml_1755072712.meta
    17:47:07 - data/archive/robot_config_backup.yaml_1755071733
  Honeytokens Triggered: robot_config_backup.yaml_1755072712.meta, robot_config_backup.yaml_1755071733
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #4 - 17:47:48
----------------------------------------

Reconnaissance Phase:
  Duration: 12.42 seconds
  Files Accessed: 2
    17:47:25 - data/dynamic/robot_20250813_161152_default.yaml
    17:47:34 - data/dynamic/log_20250813_160440_backup.csv
  Honeytokens Triggered: log_20250813_160440_backup.csv
  Phase Success: True

Data Exfiltration Phase:
  Duration: 5.02 seconds
  Files Accessed: 1
    17:47:43 - data/archive/robot_config_backup.yaml_1755078408
  Honeytokens Triggered: robot_config_backup.yaml_1755078408
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #5 - 17:48:37
----------------------------------------

Reconnaissance Phase:
  Duration: 17.64 seconds
  Files Accessed: 2
    17:48:06 - data/dynamic/calib_20250813_174648_temp.csv
    17:48:15 - data/dynamic/calib_20250813_155623_old.txt
  Honeytokens Triggered: calib_20250813_174648_temp.csv, calib_20250813_155623_old.txt
  Phase Success: True

Data Exfiltration Phase:
  Duration: 9.10 seconds
  Files Accessed: 2
    17:48:28 - data/archive/robot_config_backup.yaml_1755072712.meta
    17:48:33 - data/archive/robot_config_backup.yaml_1755072712
  Honeytokens Triggered: robot_config_backup.yaml_1755072712.meta, robot_config_backup.yaml_1755072712
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #6 - 17:49:16
----------------------------------------

Reconnaissance Phase:
  Duration: 11.73 seconds
  Files Accessed: 3
    17:48:52 - data/archive/sensor_20250813_155544_backup.txt_1755071744
    17:48:55 - data/dynamic/sensor_20250813_155623_old.txt
    17:49:00 - data/archive/data_20250813_160440_old.txt_1755072280.meta
  Honeytokens Triggered: sensor_20250813_155544_backup.txt_1755071744
  Phase Success: True

Data Exfiltration Phase:
  Duration: 8.46 seconds
  Files Accessed: 3
    17:49:07 - data/archive/robot_config_backup.yaml_1755078408
    17:49:10 - data/archive/robot_config_backup.yaml_1755072712
    17:49:13 - data/archive/robot_config_backup.yaml_1755071733.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755078408, robot_config_backup.yaml_1755072712, robot_config_backup.yaml_1755071733.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4


Additional Framework Statistics
========================================
Total Runtime: 260.35 seconds (4.3 minutes)
Total Detection Events: 6
Total Honeytoken Triggers: 19
Total Attack Sequences: 6
Q-Learning Episodes Completed: 26
Average CPU Usage: 0.56%
Average Memory Usage: 66.36%

Learned Policy Summary
------------------------------
State (2, 3, 0): emergency_cleanup (Value: 2.500)
State (3, 2, 0): deploy_additional (Value: 14.599)
State (3, 5, 0): deploy_additional (Value: 20.494)
State (3, 8, 0): cleanup_oldest (Value: 18.987)
State (3, 7, 0): cleanup_oldest (Value: 14.708)
State (3, 6, 0): deploy_additional (Value: 10.003)
State (3, 9, 0): deploy_additional (Value: 14.843)
State (3, 10, 0): deploy_baseline (Value: 43.415)
State (3, 3, 0): deploy_baseline (Value: 5.174)

================================================================================
END OF RESULTS ANALYSIS
================================================================================

Detailed results saved to: logs/dolphin_results_20250813_174939.json
2025-08-13 17:49:39,575 - INFO - DOLPHIN Framework stopped
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ 
```
