Linux Network Packet Statistics Display

This project captures and displays network packet statistics on a Linux system. It utilizes pcap for packet capturing and multi-threading for concurrent data processing and display.

Features

* Captures packets on a specified network interface.
* Tracks statistics for TCP, UDP, ICMP, IP, and other packets.
* Logs detailed packet information to a file.
* Displays packet statistics in both text and graphical formats.
* Supports multi-threaded data reading and writing.
  
Requirements

* Linux-based system
* libpcap library
* GCC (GNU Compiler Collection)
* POSIX Threads (Pthreads)

Installation

1. Install the necessary libraries:

sudo apt-get update
sudo apt-get install libpcap-dev gcc

2. Clone the repository:

git clone https://github.com/Rambabugupta0/packet-statistics.git
cd packet-statistics

3. Compile the project:

gcc -o packet_statistics main.c -lpcap -lpthread

Usage

1. Run the packet statistics program:

sudo ./packet_statistics -i <network_interface>

Replace <network_interface> with the name of your network interface (e.g., eth0, wlan0).

2. Run the display program:

./display text
or

./display graph

The text argument displays statistics in tabular format, while the graph argument shows a graphical representation.

Command-Line Options

* -i <network_interface>: Specify the network interface to capture packets from.

Files

-> main.c: Contains the main packet capturing and logging functionality.
-> display.c: Contains the code for reading from the log file and displaying the statistics.

Signal Handling
The program can be terminated gracefully by pressing Ctrl+C. This ensures proper cleanup of resources and termination of threads.

Logging
Packet details are logged in packet_logs.txt. Statistics are logged in packet_stats.txt.

Future Enhancements

* Add support for more protocols.
* Implement a web-based UI for real-time statistics display.
* Add unit tests for individual components.

Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

Acknowledgements

The libpcap library for packet capturing.
POSIX Threads for multi-threading support.
