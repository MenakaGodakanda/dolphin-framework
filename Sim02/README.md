# Simulation 02 Output

## Video:


## Detailed Output:
```
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ python src/core/main.py --mode simulate --duration 240
2025-08-13 16:04:28,183 - INFO - DOLPHIN Framework initialized successfully
2025-08-13 16:04:28,183 - INFO - Starting DOLPHIN Framework...
2025-08-13 16:04:28,184 - INFO - Deployed 3 baseline honeytokens
2025-08-13 16:04:28,190 - INFO - DOLPHIN Framework started successfully
2025-08-13 16:04:28,190 - INFO - Starting combined attack simulation for 240 seconds
Running combined attack simulation for 240 seconds...
Collecting detailed performance metrics...
Press Ctrl+C to stop early.
2025-08-13 16:04:28,190 - INFO - Attack simulation 1
2025-08-13 16:04:46,702 - INFO - Attack 1 completed - Honeytokens triggered: 3
2025-08-13 16:05:12,852 - INFO - Attack simulation 2
2025-08-13 16:05:39,650 - INFO - Attack 2 completed - Honeytokens triggered: 4
2025-08-13 16:06:02,655 - INFO - Attack simulation 3
2025-08-13 16:06:20,543 - INFO - Attack 3 completed - Honeytokens triggered: 2
2025-08-13 16:06:37,014 - INFO - Attack simulation 4
2025-08-13 16:07:10,050 - INFO - Attack 4 completed - Honeytokens triggered: 5
2025-08-13 16:07:27,039 - INFO - Attack simulation 5
2025-08-13 16:07:54,669 - INFO - Attack 5 completed - Honeytokens triggered: 4
2025-08-13 16:08:21,914 - INFO - Attack simulation 6
2025-08-13 16:08:43,941 - INFO - Attack 6 completed - Honeytokens triggered: 4
2025-08-13 16:09:08,553 - INFO - Stopping DOLPHIN Framework...

================================================================================
DOLPHIN FRAMEWORK - COMPREHENSIVE RESULTS ANALYSIS
================================================================================

Table - Experimental Results Summary
--------------------------------------------------
Detection Success Rate        : 100.00%
Q-Learning Convergence        : Converging
Baseline Honeytoken Triggers  : 0
Dynamic Honeytoken Triggers   : 22
False Positive Rate           : 0.00%
Response Latency (Recon)      : 0.000s
Response Latency (Direct)     : 0.000s
CPU Overhead                  : 0.65%
Memory Usage                  : 66.41%
Disk I/O Overhead             : 22069.40 MB/s
Network Overhead              : 1569146.35 KB/s
Average Episode Reward        : 26.047
Extended Engagement Time      : 0.00s

--------------------------------------------------

Q-Learning Performance Progression
==================================================

Reward Range: 24.345 to 27.580

 27.58 |  *****                                                     
       |**                                                          
       |                                                            
       |                                                            
       |                                                            
       |                                                            
       |       *********                                            
 25.96 |                ****                                        
       |                    *                                       
       |                                                            
       |                                                            
       |                     *****                                  
       |                                                            
       |                                                            
 24.35 |                          **                                
       ------------------------------------------------------------
       0                                                  28
       Episodes


Honeytoken Effectiveness Analysis
==================================================

Reconnaissance Token:
  Total Triggers: 6 (27.3%)
  Reconnaissance: 6
  Exfiltration: 0
  Other: 0

Exfiltration Token:
  Total Triggers: 16 (72.7%)
  Reconnaissance: 0
  Exfiltration: 16
  Other: 0


Attack Sequence Timeline Analysis
============================================================

Attack Sequence #1 - 16:04:46
----------------------------------------

Reconnaissance Phase:
  Duration: 8.75 seconds
  Files Accessed: 1
    16:04:28 - data/dynamic/robot_20250813_155623_backup.yml
  Honeytokens Triggered: robot_20250813_155623_backup.yml
  Phase Success: True

Data Exfiltration Phase:
  Duration: 5.97 seconds
  Files Accessed: 2
    16:04:40 - data/baseline/robot_config_backup.yaml
    16:04:45 - data/archive/robot_config_backup.yaml_1755071783
  Honeytokens Triggered: robot_config_backup.yaml, robot_config_backup.yaml_1755071783
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 3

Attack Sequence #2 - 16:05:39
----------------------------------------

Reconnaissance Phase:
  Duration: 13.07 seconds
  Files Accessed: 2
    16:05:12 - data/archive/sensor_20250813_155533_temp.json_1755071733.meta
    16:05:19 - data/archive/setup_20250813_155542_backup.yml_1755071742
  Honeytokens Triggered: setup_20250813_155542_backup.yml_1755071742
  Phase Success: True

Data Exfiltration Phase:
  Duration: 10.14 seconds
  Files Accessed: 3
    16:05:30 - data/archive/robot_config_backup.yaml_1755071783
    16:05:31 - data/archive/robot_config_backup.yaml_1755071733.meta
    16:05:34 - data/archive/robot_config_backup.yaml_1755071783.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071783, robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071783.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #3 - 16:06:20
----------------------------------------

Reconnaissance Phase:
  Duration: 7.35 seconds
  Files Accessed: 1
    16:06:02 - data/archive/config_20250813_155533_template.yml_1755071733.meta
  Honeytokens Triggered: None
  Phase Success: True

Data Exfiltration Phase:
  Duration: 7.39 seconds
  Files Accessed: 2
    16:06:13 - data/archive/robot_config_backup.yaml_1755071783
    16:06:16 - data/baseline/robot_config_backup.yaml
  Honeytokens Triggered: robot_config_backup.yaml_1755071783, robot_config_backup.yaml
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 2

Attack Sequence #4 - 16:07:10
----------------------------------------

Reconnaissance Phase:
  Duration: 20.14 seconds
  Files Accessed: 3
    16:06:37 - data/archive/setup_20250813_155542_backup.yml_1755071742
    16:06:39 - data/archive/sensor_20250813_155544_archive.txt_1755071744.meta
    16:06:48 - data/archive/data_20250813_155544_old.txt_1755071744.meta
  Honeytokens Triggered: setup_20250813_155542_backup.yml_1755071742, sensor_20250813_155544_archive.txt_1755071744.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 10.77 seconds
  Files Accessed: 3
    16:06:59 - data/archive/robot_config_backup.yaml_1755071733.meta
    16:07:01 - data/archive/robot_config_backup.yaml_1755071733
    16:07:05 - data/archive/robot_config_backup.yaml_1755071783.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071733, robot_config_backup.yaml_1755071783.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 5

Attack Sequence #5 - 16:07:54
----------------------------------------

Reconnaissance Phase:
  Duration: 12.96 seconds
  Files Accessed: 3
    16:07:27 - data/archive/params_20250813_155533_default.yaml_1755071733
    16:07:29 - data/dynamic/calib_20250813_160440_old.json
    16:07:33 - data/archive/log_20250813_155542_temp.txt_1755071744
  Honeytokens Triggered: calib_20250813_160440_old.json
  Phase Success: True

Data Exfiltration Phase:
  Duration: 10.00 seconds
  Files Accessed: 3
    16:07:44 - data/baseline/robot_config_backup.yaml
    16:07:47 - data/archive/robot_config_backup.yaml_1755071733.meta
    16:07:49 - data/archive/robot_config_backup.yaml_1755071783.meta
  Honeytokens Triggered: robot_config_backup.yaml, robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071783.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4

Attack Sequence #6 - 16:08:43
----------------------------------------

Reconnaissance Phase:
  Duration: 10.35 seconds
  Files Accessed: 2
    16:08:21 - data/dynamic/robot_20250813_155623_template.yaml
    16:08:29 - data/archive/sensor_20250813_155544_archive.txt_1755071744.meta
  Honeytokens Triggered: sensor_20250813_155544_archive.txt_1755071744.meta
  Phase Success: True

Data Exfiltration Phase:
  Duration: 7.57 seconds
  Files Accessed: 3
    16:08:36 - data/archive/robot_config_backup.yaml_1755071733.meta
    16:08:38 - data/archive/robot_config_backup.yaml_1755071733
    16:08:40 - data/archive/robot_config_backup.yaml_1755071783.meta
  Honeytokens Triggered: robot_config_backup.yaml_1755071733.meta, robot_config_backup.yaml_1755071733, robot_config_backup.yaml_1755071783.meta
  Phase Success: True
Overall Success: True
Total Honeytokens Triggered: 4


Additional Framework Statistics
========================================
Total Runtime: 283.02 seconds (4.7 minutes)
Total Detection Events: 6
Total Honeytoken Triggers: 22
Total Attack Sequences: 6
Q-Learning Episodes Completed: 28
Average CPU Usage: 0.65%
Average Memory Usage: 66.41%

Learned Policy Summary
------------------------------
State (2, 3, 0): emergency_cleanup (Value: 4.750)
State (3, 2, 0): deploy_additional (Value: 14.599)
State (3, 5, 0): deploy_additional (Value: 20.494)
State (3, 8, 0): cleanup_oldest (Value: 21.712)
State (3, 7, 0): cleanup_oldest (Value: 17.138)
State (3, 6, 0): deploy_additional (Value: 13.342)
State (3, 9, 0): deploy_additional (Value: 14.633)
State (3, 10, 0): deploy_baseline (Value: 46.395)

================================================================================
END OF RESULTS ANALYSIS
================================================================================

Detailed results saved to: logs/dolphin_results_20250813_160911.json
2025-08-13 16:09:11,210 - INFO - DOLPHIN Framework stopped
(venv) mcyber@mcyber-VirtualBox:~/dolphin-framework$ 
```
