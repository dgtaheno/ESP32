<div id="top"></div>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![GNU License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/dgtaheno">
    <img src="https://github.com/dgtaheno/Imail/blob/master/pictures/logo.png?raw=true" alt="Logo" width="200" height="200">
  </a>

  <h3 align="center">LCD I2C Date & Time display</h3>

  <p align="left">
    Do you want to have actual date and time to the second online updated? Then that´s your project.
    <br />
  <p align="left">
    Using ESP32DevKit C V4 hardware and a LCD display with I2C module, now I have time under control.
    <br />
  
  <a href="https://github.com/dgtaheno/ESP32/tree/main/LCD_I2C%20display%20time/LCD_I2C_Time%26Date"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/dgtaheno/ESP32/tree/main/LCD_I2C%20display%20time/LCD_I2C_Time%26Date">View Demo</a>
    ·
    <a href="https://github.com/dgtaheno/ESP32/issues">Report Bug</a>
    ·
    <a href="https://github.com/dgtaheno/ESP32/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

[![Product Name Screen Shot][product-screenshot]](https://github.com/dgtaheno/ESP32/tree/main/LCD_I2C%20display%20time)

I´m in a process of learning further about Embedded software and in the process I found thi interesting project which will allow us to learn about Online Time update and I2C displays.

Why should you create your own LCD I2C Time display?

- It is a cool way to invest your time.
- You will hopefully increase your knowledge on C++ programming, ESP32, Arduino and so many other tools.
- You will have always updated time under control.(that´s cool!)
- It´s cheap, and try to make it as easy as possible.

In order to upload LCD I2C Time display the following files were generated for this project:

<li><a href="https://github.com/dgtaheno/ESP32/blob/71145b9ea02182c14f01afcd3006fc98b02ad644/LCD_I2C display time/LCD_I2C_Time&Date/LCD_I2C_Time&Date.ino">LCD_I2C_Time&Date.ino</a></li>

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

This is the software used to create this project:

- [Arduino IDE](https://www.arduino.cc/en/software)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

You will need some basic electronic and programming knowledge, but I will try to keep it easy.

### Prerequisites

Hardware:

[![Hardware Name Screen Shot][hardware-screenshot]](https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/circuit.jpg)

- [ESP32DEVKIT c V4 board](https://www.amazon.de/s?k=esp32+devkitc+v4&sprefix=ESP32+devkit%2Caps%2C135&ref=nb_sb_ss_ts-doa-p_1_12)
  (or any similar ESP32 board)

See related [link](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/hw-reference/esp32/get-started-devkitc.html) for serial programming with Arduino IDE.

Software:

I programmed ESP32 DevKit C V4 using Arduino IDE but it is also possible to do it with VS Code + Platform IO extension.

Please follow this [ESP32 Arduino IDE Tutorial](https://www.iottechtrends.com/getting-started-with-esp32-wroom-devkitc/) so you can learn how to program it.

Please note that the following libraries should be installed in the project:

- [Wifi.h](https://www.arduino.cc/reference/en/libraries/wifi/)
- [Time.h](https://www.arduino.cc/reference/en/libraries/time/)
- [sntp.h](https://github.com/esp8266/Arduino/blob/master/tools/sdk/include/sntp.h)
- [LiquidCrystal_I2C.h](https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library/blob/master/LiquidCrystal_I2C.h)


### Installation

Prior to flash the board with the program it is necessary to adjust LCD_I2C_Time&Date.ino in src.

The required part to adjust is the following:

- // Wifi network station credentials

  #define WIFI_SSID "**\*\***\***\*\***"

  #define WIFI_PASSWORD "**\*\*\*\***\*\***\*\*\*\***"

- // LiquidCrystal_I2C lcd(0x27, 16, 2); //(Address, number of characters per line, number of lines)

  If you don´t know your lcd address you can follow the instructions [here](https://todbot.com/blog/2009/11/29/i2cscanner-pde-arduino-as-i2c-bus-scanner/) to scan for the address.

With your own parameters, please note that Wifi credential must be filled with your WIFI data.

Once you have adapted the code and connected, click on ESP32 Devkit C V4 "rst" button which will put the board in upload mode.

Click on upload in Arduino IDE and once it is uploaded it is ready to go.

ESP32 DEVKIT C V4 will reboot when finished.

You can now disconnect the board from computer if you don not need to serial monitor anymore and just connect as per connection diagram in hardware section.

Now LCD I2C Date & Time is ready to work.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

Once ESP 32 DEVKIT C V4 is powered with 5 V, the program will automatically start.

The program works as follows:

[![Hardware diagram][software-diagram]](https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/circuit.jpg)

You should be able to see on the display Date & Time:

[![LCD picture][LCD-picture]](https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/example.jpg)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ROADMAP -->

## Roadmap

- [x] Create LCD_I2C_Time&Date.ino
- [x] Include all libraries dependencies
  - [x] Wifi.h
  - [x] Time.h
  - [x] sntp.h
  - [x] LiquidCrystal_I2C.h

- [x] Design and build all hardware configuration.
- [x] Upload program to ESP32 DevKIT C V4.
- [x] Test
- [x] Create README.md

- [ ] Upgrade with new features:
  - Not planned

See the [open issues](https://github.com/dgtaheno/ESP32/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the GNU License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

David García-Taheno Fernández - dgtaheno@hotmail.com

Project Link: [https://github.com/dgtaheno/ESP32/tree/main/LCD_I2C%20display%20time](https://github.com/dgtaheno/ESP32/tree/main/LCD_I2C%20display%20time)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

Resources I found helpful and would like to give credit to.

- [Best README.md template](https://github.com/othneildrew/Best-README-Template)
- [Rui Santos](https://github.com/RuiSantosdotme/ESP32-Course)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/dgtaheno/ESP32.svg?style=for-the-badge
[contributors-url]: https://github.com/dgtaheno/ESP32/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/dgtaheno/ESP32.svg?style=for-the-badge
[forks-url]: https://github.com/dgtaheno/ESP32/network/members
[stars-shield]: https://img.shields.io/github/stars/dgtaheno/ESP32.svg?style=for-the-badge
[stars-url]: https://github.com/dgtaheno/ESP32/stargazers
[issues-shield]: https://img.shields.io/github/issues/dgtaheno/ESP32.svg?style=for-the-badge
[issues-url]: https://github.com/dgtaheno/ESP32/issues
[license-shield]: https://img.shields.io/github/license/dgtaheno/ESP32.svg?style=for-the-badge
[license-url]: https://github.com/dgtaheno/ESP32/blob/f916f11d36e570b180b5d8b98a3717dbaca18b02/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/dgtaheno/?locale=en_US
[product-screenshot]: https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/example.jpg
[hardware-screenshot]: https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/circuit.jpg
[software-diagram]: https://github.com/dgtaheno/ESP32/blob/52555a4f461ef37b45af659f3b6e6c576568df58/LCD_I2C%20display%20time/LCD_I2C_Time&Date/pictures/circuit.jpg