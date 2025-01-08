# System Utility Dashboard

The System Utility Dashboard is a simple Node.js application that provides detailed information about your system, including operating system type, memory usage, and CPU details. It also saves the system information in a structured log file for future reference.

## Features

- **System Information Display**:
  - OS Type
  - Total Memory
  - Free Memory
  - CPU Details
- **Log System Information**: Automatically saves the system information to a file in a standardized directory (`logs/system-info.txt`).
- **Directory Management**: Ensures the required directory structure exists before saving the log file.

## Prerequisites

- [Node.js](https://nodejs.org/) (version 12 or later)

## Installation

1. Clone the repository or copy the script to your local machine.
2. Ensure Node.js is installed on your system.
3. Navigate to the folder containing the script using a terminal.

## Usage

1. Run the script in your terminal:
   ```bash
   node app.js
   ```
2. The application will:
   - Display system information in the terminal.
   - Save the same information to `logs/system-info.txt`.

## Example Output

### **Terminal Output**
```plaintext
System Information:
{
  osType: "Linux",
  totalMemory: 8374140928,
  freeMemory: 512345678,
  cpuDetails: [ ... ] // CPU details array
}
System information saved to /path/to/logs/system-info.txt
```

### **Log File Contents**
```json
{
  "osType": "Linux",
  "totalMemory": 8374140928,
  "freeMemory": 512345678,
  "cpuDetails": [
    {
      "model": "Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz",
      "speed": 3600,
      "times": {
        "user": 252345600,
        "nice": 0,
        "sys": 12345678,
        "idle": 789012345,
        "irq": 0
      }
    },
    ...
  ]
}
```

## Technologies Used

- **Node.js Core Modules**:
  - `os`: For retrieving system information.
  - `fs`: For creating directories and writing files.
  - `path`: For handling and standardizing file paths.

## Code Overview

### Key Features

1. **Gathering System Information**:
   - The `os` module is used to collect system details like OS type, total memory, free memory, and CPU information.
2. **Directory Management**:
   - The `fs.mkdir` method ensures the `logs` directory exists before attempting to save the file.
3. **Saving Logs**:
   - The `fs.writeFile` method writes the formatted system information to `logs/system-info.txt` in JSON format.

---

Enjoy monitoring and logging your system's performance with the System Utility Dashboard!

