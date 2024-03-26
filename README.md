# ESP8266 DNS Sinkhole 🛡️

A DNS sinkhole to block ads on your network, utilizing an ESP8266 microcontroller. This project aims to enhance network browsing experience by filtering unwanted content directly at the DNS level.

## Features 🌟

- **Basic Version:** Blocks websites based on a static blacklist. (file: sinkhole )
- **Advanced Version (OLED + Dynamic Blacklist):** Comes with an OLED display for real-time status updates and supports dynamically updating the blacklist from a remote source. (file: sinkhole_OLED_dynamicBlacklist )

## Getting Started 🚀

### Prerequisites

- Arduino IDE installed on your computer.
- An ESP8266 microcontroller.
- For the advanced version: An ESP8266 with an OLED display.

### Installation

#### Basic Sinkhole Setup

1. Clone this repository to your local machine.
2. Open the project file in Arduino IDE as a *.ino file, or paste the code into Arduino IDE directly.
3. Edit `SSID` and `password` in the code to match your WiFi network credentials.
4. Add websites to the `blacklist[]` array as needed.
5. Upload the code to your ESP8266 using Arduino IDE.

#### Advanced Sinkhole Setup (OLED + Dynamic Blacklist)

1. Make sure you have the specified ESP8266 Development Board with a 2.44 cm OLED Display. [Product Link](https://www.temu.com/esp8266-development-board-with-0-96-inch-oled-display-ch340-driver-esp-12e-wifi-wireless-module-and-micro-usb-works-great-for-arduino-ide-micropython-programming-pin-header-soldered-g-601099516598039.html)
2. Follow the same steps as the basic setup to clone the project and configure WiFi settings.
3. Optionally, modify the dynamic blacklist URL in the code for custom updates. Ensure the format matches the existing one to avoid modifications in parsing logic.
   - The ESP8266 memory limits the dynamic list to 500 URLs. Adjust `maxBlacklistSize` in the code if necessary.
4. Upload the code to your ESP8266 using Arduino IDE.

### Post-Installation

1. Determine the IP address assigned to your ESP8266 by your router.
2. Assign a static IP address to your ESP8266 in your router's settings.
3. Set the DNS server on your device (or router, for network-wide blocking) to the static IP address of your ESP8266.

## Usage 📖

- **Basic Version:** Visit `http://<ESP_IP>/logs` in your browser to view the DNS query logs.
- **Advanced Version:** Navigate to `http://<ESP_IP>/` to access the dashboard where you can view logs, update the blacklist manually, or see real-time status on the OLED display.
  - The blacklist will automatically update every 24 hours using the provided URL but can be immediately refreshed using the "Update Blacklist" button on the web interface.

## Contributing 🤝

Contributions to both the basic and advanced versions of the DNS sinkhole are welcome! Whether it's bug fixes, feature enhancements, or documentation improvements, feel free to fork this repository and submit a pull request.

## License 📜

This project is open-sourced under the MIT License.

Happy Blocking! 🎉
