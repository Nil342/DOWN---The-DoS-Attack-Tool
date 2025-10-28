# Down DOS Proxy - Advanced Flood Test Tool

A powerful Bash script for network stress testing and load analysis with support for multiple attack vectors and proxy rotation.

![Banner](https://img.shields.io/badge/Network-Testing-blue)
![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey)

## ⚠️ Important Legal Disclaimer

**This tool is designed for educational purposes, authorized penetration testing, and security research only. Unauthorized use against networks you don't own or have explicit permission to test is illegal and unethical. The developers are not responsible for any misuse of this tool.**

## Features

- **Multiple Attack Vectors**
  - TCP SYN Flood
  - UDP Flood  
  - TCP ACK Flood
  - HTTP Flood through Proxies
  - Mixed Browser Traffic Simulation

- **Proxy Support**
  - Built-in list of 10 free web proxies
  - Automatic request distribution across proxies
  - Realistic traffic simulation

- **User-Friendly Interface**
  - Animated ASCII banner
  - Interactive menu system
  - Configurable parameters

## Prerequisites

```bash
# Install required tools on Debian/Ubuntu
sudo apt update
sudo apt install hping3 netcat

# Or on CentOS/RHEL
sudo yum install hping3 nc
```

## Installation

```bash
git clone https://github.com/yourusername/down-dos-proxy.git
cd down-dos-proxy
chmod +x down-dos-proxy.sh
```

## Usage

```bash
./down-dos-proxy.sh
```

Follow the interactive prompts:

1. **Enter target IP** (default: 127.0.0.1)
2. **Enter target port** (default: 80)
3. **Enter packet count** (default: 1000)
4. **Select flood type** (1-5)

### Flood Types

1. **TCP SYN Flood** - Traditional SYN packet flooding
2. **UDP Flood** - UDP packet flooding
3. **TCP ACK Flood** - ACK packet flooding  
4. **HTTP Flood** - HTTP requests through multiple proxies
5. **Mixed Browser Traffic** - Realistic browser traffic simulation

## Proxy Configuration

The script includes a built-in list of free web proxies. To update or add your own proxies, modify the `PROXIES` array in the script:

```bash
PROXIES=(
    "your.proxy.ip:port"
    "another.proxy.ip:port"
)
```

## Technical Details

### HTTP Flood Features
- Distributed requests across multiple proxies
- Real HTTP/1.1 protocol implementation
- Proper request headers and formatting

### Mixed Browser Traffic
- Multiple user agent rotation
- Various HTTP methods (GET, POST, HEAD)
- Different request paths and content types
- Realistic browser behavior simulation

## Use Cases

- ✅ **Authorized** penetration testing
- ✅ Network infrastructure stress testing
- ✅ Load balancer performance evaluation
- ✅ DDoS protection system validation
- ✅ Educational security research

## Legal and Ethical Usage

Always ensure you have:
- Written permission from the target owner
- Testing conducted in controlled environments
- Compliance with local laws and regulations
- Proper documentation of authorization

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is for educational purposes. Users are responsible for ensuring compliance with all applicable laws and regulations.

## Support

For issues and questions:
1. Check the prerequisites are installed
2. Verify proxy availability
3. Ensure proper permissions for network operations

---

**Remember: With great power comes great responsibility. Use this tool wisely and ethically.**
