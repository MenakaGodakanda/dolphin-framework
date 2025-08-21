# Simulation 01 Output

## Video:


## Detailed Output:
```
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ python src/core/main.py --mode simulate --duration 240
2025-08-13 15:55:29,182 - INFO - DOLPHIN Framework initialized successfully
2025-08-13 15:55:29,182 - INFO - Starting DOLPHIN Framework...
2025-08-13 15:55:29,183 - INFO - Created genuine sensor data: data/genuine/current_sensor_data.json
2025-08-13 15:55:29,185 - INFO - Deployed 3 baseline honeytokens
2025-08-13 15:55:29,195 - INFO - DOLPHIN Framework started successfully
2025-08-13 15:55:29,195 - INFO - Starting combined attack simulation for 240 seconds
2025-08-13 15:55:29,197 - INFO - Attack simulation 1
Running combined attack simulation for 240 seconds...
Collecting detailed performance metrics...
Press Ctrl+C to stop early.
2025-08-13 15:55:50,884 - INFO - Attack 1 completed - Honeytokens triggered: 5
2025-08-13 15:56:12,517 - INFO - Attack simulation 2
2025-08-13 15:56:33,744 - INFO - Attack 2 completed - Honeytokens triggered: 5
2025-08-13 15:57:01,253 - INFO - Attack simulation 3
2025-08-13 15:57:19,219 - INFO - Attack 3 completed - Honeytokens triggered: 2
2025-08-13 15:57:30,640 - INFO - Attack simulation 4
2025-08-13 15:58:03,673 - INFO - Attack 4 completed - Honeytokens triggered: 5
2025-08-13 15:58:16,233 - INFO - Attack simulation 5
2025-08-13 15:58:35,876 - INFO - Attack 5 completed - Honeytokens triggered: 2
2025-08-13 15:59:04,643 - INFO - Attack simulation 6
2025-08-13 15:59:28,025 - INFO - Attack 6 completed - Honeytokens triggered: 4
2025-08-13 15:59:52,382 - INFO - Stopping DOLPHIN Framework...

================================================================================
DOLPHIN FRAMEWORK - COMPREHENSIVE RESULTS ANALYSIS
================================================================================

Table - Experimental Results Summary
--------------------------------------------------
Detection Success Rate        : 100.00%
Q-Learning Convergence        : Converging
Baseline Honeytoken Triggers  : 0
Dynamic Honeytoken Triggers   : 24
False Positive Rate           : 0.00%
Response Latency (Recon)      : 0.000s
Response Latency (Direct)     : 0.000s
CPU Overhead                  : 0.60%
Memory Usage                  : 65.80%
Disk I/O Overhead             : 21991.44 MB/s
Network Overhead              : 1567321.97 KB/s
Average Episode Reward        : 23.778
Extended Engagement Time      : 0.00s

--------------------------------------------------

Q-Learning Performance Progression
==================================================

Reward Range: 21.452 to 28.750

 28.75 |*                                                           
       |                                                            
       |                                                            
       | ****                                                       
       |                                                            
       |                                                            
       |     *****                                                  
 25.10 |                                                            
       |                                                            
       |          ****                                              
       |                                                            
       |                *                                           
       |              ** *                                          
       |                                                            
 21.45 |                  ********                                  
       ------------------------------------------------------------
       0                                                  26
       Episodes


Honeytoken Effectiveness Analysis
==================================================

Reconnaissance Token:
  Total Triggers: 8 (33.3%)
  Reconnaissance: 8
  Exfiltration: 0
  Other: 0

Exfiltration Token:
  Total Triggers: 16 (66.7%)
  Reconnaissance: 0
  Exfiltration: 16
  Other: 0


Attack Sequence Timeline Analysis
============================================================

Attack Sequence #1 - 15:55:50
----------------------------------------

Reconnaissance Phase:
  Duration: 8.77 seconds
  Files Accessed: 2
    15:55:29 - data/baseline/robot_config_backup.yaml
    15:55:32 - data/baseline/system_log_archive.txt
  Honeytokens Triggered: robot_config_backup.yaml, system_log_archive.txt
  Phase Success: True

Data Exfiltration Phase:
  Duration: 8.56 seconds
  Files Accessed: 3
    15:55:42 - data/archive/robot_config_backup.yaml_1755071733
    15:55:44 - data/archive/robot_config_backup.yaml_1755071733.meta
    15:55:46 - data/archive/sensor_calibration.json_1755071729.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733, robot_config_backup.yaml_1755071733.meta, sensor_calibration.json_1755071729.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 5

Attack Sequence #2 - 15:56:33
----------------------------------------

Reconnaissance Phase:
  Duration: 8.71 seconds
  Files Accessed: 2
    15:56:12 - data/archive/sensor_20250813_155544_backup.txt_1755071744
    15:56:15 - data/archive/params_20250813_155544_default.yml_1755071744
  Honeytokens Triggered: sensor_20250813_155544_backup.txt_1755071744
  Phase Success: True

Data Exfiltration Phase:
  Duration: 10.12 seconds
  Files Accessed: 4
    15:56:24 - data/baseline/robot_config_backup.yaml
    15:56:27 - data/archive/robot_config_backup.yaml_1755071733.meta
    15:56:28 - data/archive/robot_config_backup.yaml_1755071733
    15:56:31 - data/archive/sensor_calibration.json_1755071729.meta
  Honeytokens Triggered: robot_config_backup.yaml, robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071733, sensor_calibration.json_1755071729.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 5

Attack Sequence #3 - 15:57:19
----------------------------------------

Reconnaissance Phase:
  Duration: 8.71 seconds
  Files Accessed: 1
    15:57:01 - data/archive/config_20250813_155542_template.yml_1755071742
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 6.91 seconds
  Files Accessed: 2
    15:57:12 - data/archive/robot_config_backup.yaml_1755071783.meta
    15:57:16 - data/archive/robot_config_backup.yaml_1755071733
  Honeytokens Triggered: robot_config_backup.yaml_1755071783.meta, robot_config_backup.yaml_1755071733
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #4 - 15:58:03
----------------------------------------

Reconnaissance Phase:
  Duration: 18.83 seconds
  Files Accessed: 3
    15:57:30 - data/archive/robot_config_backup.yaml_1755071783
    15:57:36 - data/archive/calib_20250813_155542_backup.txt_1755071744.meta
    15:57:40 - data/archive/robot_20250813_155533_backup.conf_1755071733.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071783, calib_20250813_155542_backup.txt_1755071744.meta, robot_20250813_155533_backup.conf_1755071733.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 10.88 seconds
  Files Accessed: 3
    15:57:53 - data/archive/robot_config_backup.yaml_1755071783.meta
    15:57:55 - data/archive/robot_config_backup.yaml_1755071783
    15:57:59 - data/archive/robot_config_backup.yaml_1755071733.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071783.meta, robot_config_backup.yaml_1755071783, robot_config_backup.yaml_1755071733.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 5

Attack Sequence #5 - 15:58:35
----------------------------------------

Reconnaissance Phase:
  Duration: 6.84 seconds
  Files Accessed: 1
    15:58:16 - data/dynamic/robot_20250813_155623_template.yaml
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 8.96 seconds
  Files Accessed: 2
    15:58:27 - data/archive/robot_config_backup.yaml_1755071733.meta
    15:58:31 - data/archive/robot_config_backup.yaml_1755071783
  Honeytokens Triggered: robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071783
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #6 - 15:59:28
----------------------------------------

Reconnaissance Phase:
  Duration: 14.70 seconds
  Files Accessed: 2
    15:59:04 - data/archive/log_20250813_155544_backup.txt_1755071744.meta
    15:59:10 - data/archive/params_20250813_155542_backup.yaml_1755071744
  Honeytokens Triggered: log_20250813_155544_backup.txt_1755071744.meta, params_20250813_155542_backup.yaml_1755071744
  Phase Success: True

Data Exfiltration Phase:
  Duration: 6.36 seconds
  Files Accessed: 2
    15:59:21 - data/archive/robot_config_backup.yaml_1755071783.meta
    15:59:24 - data/archive/robot_config_backup.yaml_1755071783
  Honeytokens Triggered: robot_config_backup.yaml_1755071783.meta, robot_config_backup.yaml_1755071783
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4


Additional Framework Statistics
========================================
Total Runtime: 270.55 seconds (4.5 minutes)
Total Detection Events: 6
Total Honeytoken Triggers: 24
Total Attack Sequences: 6
Q-Learning Episodes Completed: 26
Average CPU Usage: 0.60%
Average Memory Usage: 65.80%

Learned Policy Summary
------------------------------
State (2, 3, 0): emergency_cleanup (Value: 2.500)
State (3, 2, 0): deploy_additional (Value: 10.956)
State (3, 5, 0): deploy_additional (Value: 17.095)
State (3, 8, 0): cleanup_oldest (Value: 18.987)
State (3, 7, 0): cleanup_oldest (Value: 14.708)
State (3, 6, 0): deploy_additional (Value: 10.003)
State (3, 9, 0): deploy_additional (Value: 12.916)
State (3, 10, 0): deploy_baseline (Value: 37.193)

================================================================================
END OF RESULTS ANALYSIS
================================================================================

Detailed results saved to: logs/dolphin_results_20250813_155959.json
2025-08-13 15:59:59,731 - INFO - DOLPHIN Framework stopped
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ 
```
