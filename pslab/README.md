##Troubleshooting

Installation Issues
Error: "ModuleNotFoundError: No module named 'pslab'"

Solution: Make sure you ran pip3 install -e . (with -e flag for development)

Error: "Permission denied" on Linux

Solution: Run pip3 install --user -e . or use sudo

Error: "python3" command not found

Ubuntu/Debian:

sudo apt-get install python3 python3-pip

macOS:

brew install python3

Windows:

Download from https://www.python.org/downloads/

Run installer and check "Add Python to PATH"

Connection Issues
"Device not found"

Ensure PSLab hardware is connected via USB

Check USB port: ls /dev/ttyUSB* on Linux

Quick Start Examples
1. Connect to Your PSLab Device
text
from pslab import ScienceLab

# Connect to the device
I = ScienceLab()
print("✅ Connected to PSLab!")
2. Read a Voltage Measurement
text
# Measure voltage on Channel 1 (CH1)
voltage = I.get_average_voltage('CH1')
print(f"Voltage on CH1: {voltage} V")
3. Generate a Signal
text
# Generate 1kHz sine wave on output W1
I.set_sine1(1000)
print("Sine wave generated at 1 kHz")
