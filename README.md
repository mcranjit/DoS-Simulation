# DoS Simulation
DoS Simulation is a Python-based script designed for testing the resilience of web servers by simulating high traffic loads in a controlled and ethical manner. This script allows users to evaluate how their systems handle multiple simultaneous requests and identify potential performance bottlenecks.

## Features
- Multi-threaded HTTP request simulation.
- Real-time metrics for:
  - Requests per second.
  - Responses per second.
  - Average response time.
- Configurable rate limits and thread counts.

## Intended Use
This script is intended for educational purposes and controlled testing scenarios only. Ensure you have explicit permission to test any target system before using this tool.

## Prerequisites
- Python 3.7 or higher.
- Install required libraries using:
  ```bash
  pip install -r requirements.txt
  ```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mcranjit/dos-simulation.git
   ```
2. Navigate to the project directory:
   ```bash
   cd dos-simulation
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Update the target URL in the script:
   ```python
   TARGET_URL = "http://example.com/"
   ```
2. Run the script:
   ```bash
   python dos_test.py
   ```

## Configuration
- **Rate Limit:** Modify `RATE_LIMIT` to set the number of requests per second per thread.
- **Threads:** Adjust the `threads` variable to change the number of concurrent threads.

## Example Output
```
Starting thread #0...
Starting thread #1...
Starting thread #2...
...
Response code from thread 0: 200 took 123 ms
Response code from thread 1: 200 took 130 ms
Response code from thread 2: 200 took 140 ms
...

Calculating... wait for a while for it to adjust...
Average response time: 134.67ms; Requests/sec: 50; Responses/sec: 48; DoSing...
Average response time: 500.25ms; Requests/sec: 52; Responses/sec: 49; DoSing...
Average response time: 61000.00ms; Requests/sec: 45; Responses/sec: 0; DoS Successful. Site looks down for now.
```

## Disclaimer
This tool is provided for educational and testing purposes only. Unauthorized use against systems you do not own or have explicit permission to test is illegal and unethical. The creator is not responsible for misuse of this software.



