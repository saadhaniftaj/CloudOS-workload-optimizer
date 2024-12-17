# Hybrid Process Scheduling System

This repository contains the implementation of a **Hybrid Process Scheduling System** that integrates traditional operating system process management with cloud computing technologies. The project demonstrates the synergy between local and cloud resources, leveraging **Linux process monitoring tools**, **AWS Lambda**, and **AWS Simple Queue Service (SQS)** for optimized workload distribution. A GUI built with **Tkinter** enhances user interaction, allowing seamless local or cloud-based task execution.

## Features

- **Real-Time Process Monitoring**: View and track active processes and their resource usage on the local system.
- **Dynamic Task Offloading**: Automatically offloads resource-intensive tasks to AWS Lambda for serverless execution.
- **Task Queuing**: Utilizes AWS SQS to manage task distribution between local and cloud environments.
- **Customizable Scheduler**: Supports task prioritization and manual task execution via an intuitive GUI.
- **Performance Evaluation**: Compares local-only, cloud-only, and hybrid execution to demonstrate improved resource utilization and scalability.

---

## Prerequisites

Before running the project, ensure the following requirements are met:

### Local System
- Python 3.7 or higher
- Linux operating system (for process monitoring commands)
- Tkinter library (for GUI)

### AWS Services
- An active AWS account
- AWS Lambda configured with Python runtime
- AWS Simple Queue Service (SQS) set up with necessary permissions
- AWS CLI installed and configured on the local machine

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/hybrid-process-scheduler.git
   cd hybrid-process-scheduler
hybrid-process-scheduler/
│
├── aws/
│   ├── deploy_lambda.py       # Script to deploy Lambda function
│   └── lambda_function.py     # AWS Lambda function code
│
├── gui/
│   └── scheduler_gui.py       # Tkinter-based GUI implementation
│
├── scheduler/
│   ├── local_scheduler.py     # Local process management and scheduling
│   ├── cloud_scheduler.py     # AWS Lambda and SQS integration
│   └── hybrid_scheduler.py    # Hybrid scheduling logic
│
├── tests/
│   └── test_performance.py    # Scripts to evaluate system performance
│
├── requirements.txt           # Python dependencies
├── config.py                  # Configuration for AWS and system settings
├── main.py                    # Entry point to run the application
├── README.md                  # Project documentation
└── LICENSE                    # License information
