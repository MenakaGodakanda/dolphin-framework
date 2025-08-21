# Simulation Output Analysis

## Simulation Output

### Simulation 01:

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/Sim01/README.md">Simulation 01</a>

### Simulation 02:

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/Sim02/README.md">Simulation 02</a>

### Simulation 03:

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/Sim03/README.md">Simulation 03</a>

### Simulation 04:

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/Sim04/README.md">Simulation 04</a>

### Simulation 05:

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/Sim05/README.md">Simulation 05</a>

## Results Overview


| Metric |	Sim01 |	Sim02 |	Sim03 |	Sim04 |	Sim05 |	Average |
|-------|-------|-------|-------|-------|-------|-------|
| Number of Attacks	| 6 |	6 |	6	| 6	| 6	| 6 |
| Detection Rate (%)	| 100.00	| 100.00	| 100.00	| 100.00	| 100.00	| 100.00 |
| Response Latency (s)	| 0.00	| 0.00	| 0.00	| 0.00	| 0.00	| 0.00 |
| CPU Overhead (%)	| 0.60	| 0.65	| 0.58	| 0.56	| 0.43	| 0.56 |
| Memory Usage (%)	| 65.80	| 66.41	| 66.31	| 66.36	| 67.18	| 66.41 |
| Q-Learning Episodes	| 26	| 28	| 26	| 26	| 27	| 26.6 |
| Average Reward	| 23.78	| 26.05	| 27.00	| 26.17	| 26.99	| 26.00 |
| Reconnaissance Tokens Triggered	| 8	| 6	| 6	| 8	| 9	| 7.4 |
| Exfiltration Tokens Triggered	| 16	| 16	| 12	| 11	| 11	| 13.2 |

## System Performance Impact Assessment

| Resource	| Minimum	| Maximum	| Impact |
|-------|-------|-------|-------|
| CPU Overhead (%)	| 0.43	| 0.65	| Negligible impact |
| Memory Usage (%) |	65.80 |	67.18 |	Stable utilisation |
| Disk I/O (MB/s)	| 21991.44	| 22314.74	| Consistent I/O |
| Network (KB/s)	| 1567321.97	| 1573487.31	| Minimal variation |

## Q-Learning Algorithm Performance

| Simulation	| Initial Reward	| Final Reward	| Convergence Pattern |
|-------|-------|-------|-------|
| 1	| 28.75	| 21.45	| Stable convergence |
| 2	| 27.14	| 24.35	| Gradual improvement |
| 3	| 27.14	| 26.33	| Rapid stabilization |
| 4	| 27.14	| 24.19	| Consistent learning |
| 5	| 27.14	| 26.70	| Strong performance |

## Learned Policy Effectiveness

| State	| Optimal Action	| Q-Value	| Rationale |
|-------|-------|-------|-------|
| (3, 2, 0)	| deploy_additional	| 14.599	| High threat, low honeytoken coverage |
| (3, 8, 0)	| cleanup_oldest	| 21.712	| High threat, near capacity limit |
| (3, 10, 0)	| deploy_baseline	| 46.395	| Maximum capacity reached |
| (2, 3, 0)	| emergency_cleanup	| 4.750	| Medium threat, maintain efficiency |

