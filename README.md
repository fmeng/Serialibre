# Serialibre - A minimally maintained fork of [Serial Studio](https://github.com/Serial-Studio/Serial-Studio/)

<a href="#">
    <img width="192px" height="192px" src="doc/icon.svg" align="right" />
</a>

I needed a reliable, open-source, and intuitive serial monitor for my hardware projects.  Serial Studio was an ideal match, and even came with a tonne of features I'll admit I still have yet to ever use, but can absolutely see the immense utility of.

In early 2025, the project changed its licensing and monetization.  This repository is a fork from the last permissively-licensed commit to Serial Studio, with my own little fixes periodically tacked on as my personal projects require them.  I don't plan on becoming a thorough maintainer of this software *(certainly nowhere close to the dedication Alex has given this work)*, as this is my first exposure to working with the Qt Framework, and I have other projects I would like to prioritize.

That said, if you too are looking for a reliable, open-source, and intuitive serial monitor that you periodically add features to as you need them, then feel free to [submit a Pull Request](https://github.com/recursivenomad-forks/Serialibre/pulls/) and join the fun :)

And of course, check out Alex's [Serial Studio](https://github.com/Serial-Studio/Serial-Studio/) repository for lots more features, a real maintainer, and ways to donate.

> ***Alex Spataru:***  
> *(creator of the original Serial Studio)*
>
> Serial Studio is a multi-platform, versatile data visualization tool designed for embedded engineers, students, hackers, and teachers. It allows users to visualize, analyze, and represent data from their projects and devices without needing custom, project-specific visualization software. Serial Studio offers a flexible solution that adapts to a wide range of use cases, making it ideal for both educational and professional environments.
>
> The tool was born out of my experience in multiple CanSat-based competitions, where I often found myself developing new Ground Station Software for each project. Over time, I realized it would be more efficient and sustainable to maintain a single, flexible Ground Station Software that allows users to define how incoming data is processed and displayed.
>
> Today, Serial Studio is a powerful and adaptable tool, suitable not only for CanSat competitions but for any data acquisition and visualization project. It supports data retrieval from a wide range of sources, including hardware and software serial ports, MQTT, Bluetooth Low Energy (BLE), and network sockets (TCP/UDP).

*Read this document in other languages*: [Español](doc/README_ES.md) [简体中文](doc/README_ZH.md) [Deutsch](doc/README_DE.md) [Русский](doc/README_RU.md) [Français](doc/README_FR.md)

![Software usage](doc/screenshot.png)

## Features

- **Cross-platform:** Compatible with Windows, macOS, and Linux.
- **CSV Export:** Easily saves received data in CSV files for further analysis or processing.
- **Support for multiple data sources:** Handles a wide variety of sources, including serial ports, MQTT, Bluetooth Low Energy (BLE), and network sockets (TCP/UDP).
- **Customizable visualization:** Allows users to define and display data using various widgets, configurable via the project editor to meet specific needs.
- **Customizable frame analysis:** Provides the option to modify a JavaScript function to interpret incoming data frames, enabling the preprocessing of raw sensor data and handling of complex binary formats.
- **MQTT publishing and receiving:** Sends and receives data over the internet, enabling real-time data visualization from anywhere in the world.

Visit the **[Wiki](https://github.com/Serial-Studio/Serial-Studio/wiki)** for comprehensive guides, including:

- **Installation Instructions:** Set up Serial Studio on Windows, macOS, or Linux.  
- **Quick Start Guide:** Learn how to connect your device and visualize data in minutes.  
- **Advanced Topics:** Explore data flow, frame parsing, and building custom dashboards.
- **Examples:** Examples with code, projects, and explanations to help you learn Serial Studio.

## Development

### Requirements

To compile Serial Studio, the only required dependency is [Qt](http://www.qt.io/download-open-source/), preferrably with all plugins & modules installed. The desktop application compiles with **Qt 6.8.0**.

If you're compiling on GNU/Linux, you’ll also need to install `libgl1-mesa-dev`:

```bash
sudo apt install libgl1-mesa-dev
```

Once Qt is installed, you can compile the project by opening the **CMakeLists.txt** file in your preferred IDE or by using the command line:

```bash
mkdir build
cd build 
cmake ../ -DPRODUCTION_OPTIMIZATION=ON -DCMAKE_BUILD_TYPE=Release
cmake --build . -j 16 
```

## License

This project is licensed under the MIT License. For more details, see the [LICENSE](LICENSE.md) file.
