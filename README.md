# DOLPHIN Framework

**D**eceptive **O**perations **L**ayer **P**rotocol for **H**ostile **I**ntelligence **N**egation

A multi-layered deception framework for securing autonomous multi-terrain robotic systems through adaptive honeytoken deployment using Q-learning algorithms.

## Overview

The DOLPHIN framework implements intelligent cybersecurity deception strategies specifically designed for autonomous robotic systems. By combining Q-learning algorithms with dynamic honeytoken management, DOLPHIN provides adaptive threat detection and response capabilities that evolve based on attack patterns and system performance.

### Key Features

- **Adaptive Q-Learning Engine**: Reinforcement learning for optimal honeytoken deployment decisions
- **Dynamic Honeytoken Management**: Automated creation, deployment, and lifecycle management of deceptive assets
- **Real-time Threat Detection**: File system monitoring with inotify-based attack detection
- **Attack Simulation Module**: Comprehensive testing framework for validation and training
- **Multi-layered Defense**: Baseline and dynamic honeytokens with varying attractiveness levels
- **Performance Optimization**: Resource-aware deployment strategies

## Architecture



## System Requirements

### Minimum Requirements
- **OS**: Ubuntu 22.04 LTS (recommended) or compatible Linux distribution
- **Python**: 3.8 or higher
- **RAM**: 2GB minimum, 4GB recommended
- **Storage**: 1GB free space for logs and honeytokens
- **CPU**: 2 cores recommended

### Dependencies
- `numpy>=1.21.0`
- `pandas>=1.3.0`
- `scikit-learn>=1.0.0`
- `psutil>=5.8.0`
- `watchdog>=2.1.0`
- `colorama>=0.4.4`
- `tabulate>=0.8.9`
- `pyyaml>=6.0`
- `jsonschema>=4.0.0`

## Installation

### Automated Installation (Recommended)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MenakaGodakanda/dolphin-framework.git
   cd dolphin-framework
   ```

2. **Run the installation script:**
   ```bash
   chmod +x scripts/install.sh
   ./scripts/install.sh
   ```

3. **Activate the virtual environment:**
   ```bash
   source venv/bin/activate
   ```

### Manual Installation

1. **System dependencies:**
   ```bash
   sudo apt update && sudo apt upgrade -y
   sudo apt install -y python3 python3-pip python3-venv python3-dev
   sudo apt install -y build-essential inotify-tools htop tree git
   ```

2. **Python environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install --upgrade pip setuptools wheel
   pip install -r requirements.txt
   ```

3. **Directory structure:**
   ```bash
   mkdir -p {data/{genuine,baseline,dynamic,archive},logs,config}
   ```

## Quick Start

### 1. Basic Framework Operation

Start the DOLPHIN framework with default settings:

```bash
python src/core/main.py --mode start
```

### 2. Attack Simulation

Run a combined reconnaissance and exfiltration simulation:
```bash
python src/core/main.py --mode simulate --duration 120
```
or
```bash
python src/core/main.py --mode simulate --simulation-type combined --duration 120
```

### 3. Framework Status

Check current framework status without starting:

```bash
python src/core/main.py --mode status
```

## Configuration

The framework uses JSON configuration files located in the `config/` directory:

### Q-Learning Configuration (`config/qlearning_config.json`)

```json
{
    "learning_rate": 0.1,
    "discount_factor": 0.9,
    "initial_exploration": 0.3,
    "min_exploration": 0.05,
    "exploration_decay": 0.95,
    "decay_episodes": 100,
    "q_table_path": "data/q_table.pkl"
}
```

### Honeytoken Configuration (`config/honeytoken_config.json`)

```json
{
    "base_path": "data",
    "max_tokens": 10,
    "token_lifetime_hours": 24,
    "baseline_tokens": [
        {
            "name": "sensor_calibration.json",
            "type": "sensor_data",
            "priority": "high"
        }
    ]
}
```

## Usage Examples

### Command Line Interface

```bash
# Start framework with verbose logging
python src/core/main.py --mode start --verbose

# Run reconnaissance attack simulation
python src/core/main.py --mode simulate --simulation-type recon --duration 60

# Check framework statistics
python src/core/main.py --mode status --config-dir custom_config/
```

### Standalone Attack Simulator

```bash
# Run reconnaissance attack
python src/simulation/attack_simulator.py --attack-type recon --target-path data

# Run multiple combined attacks
python src/simulation/attack_simulator.py --attack-type combined --repeat 3

# Target specific directory
python src/simulation/attack_simulator.py --target-path /path/to/targets --repeat 5
```

### Programmatic Usage

```python
from core.main import DolphinFramework

# Initialize framework
framework = DolphinFramework(config_dir="config")

# Start monitoring
framework.start()

# Run simulation
attack_thread = framework.run_simulation(
    attack_type='combined', 
    duration=300
)

# Get statistics
stats = framework.get_framework_statistics()
print(f"Q-Learning Episodes: {stats['qlearning_stats']['episodes']}")
print(f"Active Honeytokens: {stats['honeytoken_summary']['total_active']}")

# Stop framework
framework.stop()
```

## Framework Components

### 1. Q-Learning Engine (`src/qlearning/q_engine.py`)

Implements reinforcement learning for adaptive honeytoken deployment:

- **State Representation**: (threat_level, honeytoken_count, system_load)
- **Action Space**: Deploy baseline, deploy additional, cleanup oldest, maintain current, emergency cleanup
- **Reward Function**: Balances security effectiveness with system performance
- **Epsilon-Greedy**: Exploration vs exploitation with adaptive decay

### 2. Honeytoken Manager (`src/honeytokens/honeytoken_manager.py`)

Manages honeytoken lifecycle:

- **Content Generation**: Realistic sensor data, configuration files, and logs
- **Deployment Strategies**: Baseline and dynamic deployment based on threat level
- **Lifecycle Management**: Automatic cleanup and archival of expired tokens
- **Access Monitoring**: Integration with threat detection for trigger events

### 3. Threat Detector (`src/detection/threat_detector.py`)

Real-time monitoring and assessment:

- **File System Monitoring**: inotify-based real-time file access detection
- **Threat Assessment**: Pattern-based suspicious activity scoring
- **Adaptive Response**: Q-learning integration for automated response
- **System Monitoring**: Performance impact assessment

### 4. Attack Simulator (`src/simulation/attack_simulator.py`)

Comprehensive testing framework:

- **Reconnaissance Attacks**: Gradual system exploration simulation
- **Data Exfiltration**: Targeted high-value asset extraction
- **Combined Attacks**: Multi-phase attack scenarios
- **Realistic Behavior**: Random delays, file prioritization, access patterns

## Testing

### Automated Testing

Run the comprehensive test suite:

```bash
chmod +x scripts/run_tests.sh
./scripts/run_tests.sh
```

Validate components individually:

```bash
python src/core/main.py --mode status
```

### Manual Testing

1. **Component Tests:**
   ```bash
   # Test Q-Learning engine
   python -c "from src.qlearning.q_engine import QLearningEngine; print('Q-Learning OK')"
   
   # Test honeytoken manager
   python -c "from src.honeytokens.honeytoken_manager import HoneytokenManager; print('Honeytokens OK')"
   ```

2. **Integration Tests:**
   ```bash
   # Short integration test
   timeout 30s python src/core/main.py --mode simulate --duration 25
   ```

3. **Performance Tests:**
   ```bash
   # Monitor system impact during operation
   htop &
   python src/core/main.py --mode start
   ```

## Monitoring and Logging

The framework provides comprehensive logging across all components:

### Log Files

- `logs/dolphin_framework.log` - Main framework events
- `logs/qlearning.log` - Q-learning decisions and updates
- `logs/honeytokens.log` - Honeytoken lifecycle events
- `logs/threat_detection.log` - Security events and detections
- `logs/attack_simulation.log` - Simulation results and metrics

### Real-time Monitoring

```bash
# Monitor main framework log
tail -f logs/dolphin_framework.log

# Monitor security events
tail -f logs/threat_detection.log

# Monitor Q-learning progress
tail -f logs/qlearning.log
```

## Performance Metrics

### Q-Learning Metrics
- **Episodes Completed**: Total learning iterations
- **Average Reward**: Cumulative learning performance
- **Exploration Rate**: Current epsilon value
- **Q-table Size**: Number of learned state-action pairs
- **Convergence Rate**: Learning stability over time

### Security Metrics
- **Detection Rate**: Percentage of attacks triggering honeytokens
- **False Positive Rate**: Benign activities flagged as suspicious
- **Response Time**: Time from detection to adaptive action
- **Coverage**: Percentage of attack vectors with honeytokens
- **Threat Level Distribution**: Historical threat assessment patterns

### System Metrics
- **Resource Utilization**: CPU, memory, disk usage
- **Honeytoken Overhead**: Storage and processing costs
- **Monitoring Latency**: File system event processing time
- **Cleanup Efficiency**: Expired token management performance

## Troubleshooting

### Common Issues

1. **Permission Errors:**
   ```bash
   # Fix file permissions
   chmod 755 src/core/main.py
   chmod +x scripts/*.sh
   ```

2. **Missing Dependencies:**
   ```bash
   # Reinstall requirements
   pip install -r requirements.txt --force-reinstall
   ```

3. **inotify Limits:**
   ```bash
   # Increase inotify limits
   echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf
   sudo sysctl -p
   ```

4. **Log Directory Issues:**
   ```bash
   # Create log directory
   mkdir -p logs
   chmod 755 logs
   ```

### Debug Mode

Enable verbose logging for troubleshooting:

```bash
python src/core/main.py --mode start --verbose
```

### Memory Issues

For systems with limited memory:

1. Reduce `max_tokens` in honeytoken configuration
2. Increase `cleanup_frequency` to remove expired tokens more often
3. Lower Q-learning `save_frequency` to reduce memory usage

## Deployment

### Production Deployment

1. **Systemd Service:**
   ```bash
   # Install as systemd service (requires root)
   sudo ./scripts/install.sh
   sudo systemctl enable dolphin-framework
   sudo systemctl start dolphin-framework
   ```

2. **Docker Deployment:**
   ```bash
   # Build Docker image
   docker build -t dolphin-framework .
   
   # Run container
   docker run -d --name dolphin \
     -v $(pwd)/data:/app/data \
     -v $(pwd)/logs:/app/logs \
     -v $(pwd)/config:/app/config \
     dolphin-framework
   ```

3. **Security Considerations:**
   - Run with minimal privileges
   - Secure configuration files (restrict read access)
   - Monitor log files for sensitive information
   - Regular updates and security patches
   - Network isolation for attack simulation

### Configuration Management

For multiple deployments:

```bash
# Environment-specific configs
cp -r config config-production
cp -r config config-testing
cp -r config config-development

# Use specific configuration
python src/core/main.py --config-dir config-production
```

## Expected Output Analysis

<a href="https://github.com/MenakaGodakanda/dolphin-framework/blob/main/simulation.md">Simulation Output Analysis</a>

## File Structure
```
dolphin-framework/
├── .git/
├── src/
│   ├── __init__.py
│   ├── core/
│   │   └── __init__.py
│   ├── honeytokens/
│   │   └── __init__.py
│   ├── qlearning/
│   │   └── __init__.py
│   ├── detection/
│   │   └── __init__.py
│   └── simulation/
│       └── __init__.py
├── config/
├── data/
│   ├── genuine/
│   ├── baseline/
│   ├── dynamic/
│   └── archive/
├── logs/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── performance/
├── docs/
├── scripts/
├── README.md
├── LICENSE
├── requirements.txt
└── setup.py
```

## License
This project is licensed under the MIT License.
