# Basic Network Packet Sniffer

A Python-based network packet sniffer that captures and decodes Ethernet frames on a specified network interface. It supports outputting detailed protocol data such as Ethernet, IPv4/IPv6, TCP, UDP, ICMP, and ARP.

## Features

- Capture raw network packets on specified interface
- Decode multiple protocols dynamically
- Display packet details with protocol-specific info
- Optionally display packet payload data
- Command-line interface options for interface selection and data display

## Requirements

- Python 3.x
- Run as root/admin (raw socket requires elevated permissions)

## Installation

1. Clone this repository:
git clone https://github.com/your-username/network-sniffer.git
cd network-sniffer

2. (Optional) Create and activate a virtual environment:
python3 -m venv venv
source venv/bin/activate # Windows: venv\Scripts\activate

3. Install any dependencies if added later (currently uses stdlib only).

## Usage

Run the sniffer script with optional arguments:
sudo python3 sniffer.py -i eth0 -d

- `-i`, `--interface` : Specify the network interface (default: all).
- `-d`, `--data` : Display packet payload data.

Press `Ctrl+C` to stop sniffing.

## Possible Improvements

- Add packet filtering by IP, port, or protocol.
- Save captured packets to file (e.g., PCAP format).
- Create log files for captured traffic.
- Develop a GUI for easier use.
- Expand protocol decoding support.

## License

MIT License

## Author

Created by Prateek Dangi

## Notes

### Code Improvements Suggestions
- Add error handling in core.py for socket creation and binding.
- Validate user inputs in sniffer.py CLI arguments.
- Optimize protocol decoding by caching or limiting depth to avoid infinite loops.
- Consider adding unit tests for decoding components.
- Add docstrings and comments consistently for easier maintenance.

