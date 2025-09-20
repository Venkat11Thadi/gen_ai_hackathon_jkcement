# Sensor Monitoring System

A stateful multi-agent sensor monitoring system built with Google's Agent Development Kit (ADK).

## Project Structure

```
sensor_monitoring_system/
├── main.py
├── utils.py
├── .env
├── requirements.txt
└── sensor_monitoring_agent/
    ├── init.py
    ├── agent.py
    └── sub_agents/
        ├── constraint_agent/
        │   ├── init.py
        │   └── agent.py
        ├── sensor_agent/
        │   ├── init.py
        │   └── agent.py
        └── analysis_agent/
            ├── init.py
            └── agent.py
```


## Setup Instructions

1. Create virtual env for running the code.
2. Install dependencies:  
   ```pip install google-adk python-dotenv```
3. Set your Google API key in `.env`.

## Usage

Run the following:

```bash
cd sensor_monitoring_system
python main.py
```

You should be able to converse with our chat application (for now it's in terminal).

### Example Commands

- Set constraints: "Set temperature between 20 and 30 degrees"
- Generate report: "Generate a detailed report"

## System Features

**Agents:**

- Constraint Agent: Set and manage sensor thresholds
- Sensor Agent: Collect synthetic or real sensor data
- Analysis Agent: Analyze readings, detect violations, and generate reports

**State Features:**

- Shared state across all interactions
- Comprehensive history tracking
- Modular architecture for future scaling

## Notes

- To implement real sensors and advanced database storage, extend the sensor agent and swap InMemorySessionService for database-backed alternatives.
