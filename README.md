# MidTown IT Training Solutions App

## Description
The MidTown IT Training Solutions App provides a GUI hub to switch between three algorithmic solutions:
- Rock Paper Scissors
- Multiplication Table
- Caesar Cipher

<p align="center">
  <img src="https://github.com/LukeWait/midtown-app/raw/main/assets/screenshots/midtown-app-home.png" alt="App Screenshot" width="600">
</p>

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Development](#development)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Source Code](#source-code)
- [Dependencies](#dependencies)

## Installation

### Executable
#### Windows
1. Download the `midtown_app_win_v2_0_1.zip` from the [releases page](https://github.com/LukeWait/midtown-app/releases).
2. Extract the contents to a desired location.
3. Run the `MidTownApp.exe` file.

#### Linux
1. Download the `midtown_app_linux_v2_0_1.zip` from the [releases page](https://github.com/LukeWait/midtown-app/releases).
2. Extract the contents to a desired location.
3. Make the MidTownApp file executable by running the following command in the terminal:
    ```sh
    chmod +x MidTownApp
    ```
4. Run the MidTownApp file by navigating to the directory in the terminal and executing:
    ```sh
    ./MidTownApp
    ```

### From Source
To install and run the application from source:

1. Clone the repository:
    ```sh
    git clone https://github.com/LukeWait/midtown-app.git
    cd midtown-app
    ```

2. (Optional) Create and activate a virtual environment:
    - **Windows**:
      ```sh
      python -m venv midtown_app_venv
      midtown_app_venv\Scripts\activate
      ```
    - **Linux**:
      ```sh
      python3 -m venv midtown_app_venv
      source midtown_app_venv/bin/activate
      ```

3. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Run the application:
    - **Windows**:
      ```sh
      python src\midtown_app.py
      ```
    - **Linux**:
      ```sh
      python src/midtown_app.py
      ```

## Usage
After running the application, you can easily switch between the following applets:
- **Rock Paper Scissors**: Play a classic game against another player.

<p align="center">
  <img src="https://github.com/LukeWait/midtown-app/raw/main/assets/screenshots/midtown-app-rps.png" alt="Rock Paper Scissors Screenshot" width="600">
</p>

- **Multiplication Table**: Generate and view multiplication tables.

<p align="center">
  <img src="https://github.com/LukeWait/midtown-app/raw/main/assets/screenshots/midtown-app-multiply-table.png" alt="Multiplication Table Screenshot" width="600">
</p>

- **Caesar Cipher**: Encrypt and decrypt text using the Caesar Cipher algorithm.

<p align="center">
  <img src="https://github.com/LukeWait/midtown-app/raw/main/assets/screenshots/midtown-app-caesar.png" alt="Caesar Cipher Screenshot" width="600">
</p>

## Development
### Building Executables with PyInstaller
To build executables for Windows, macOS, and Linux, you can use PyInstaller. I recommend using PyInstaller version 6.1.0 as it is stable and doesn't result in the executable being flagged as a virus like some newer versions. First, ensure you have PyInstaller installed:
```sh
pip install pyinstaller==6.1.0
```
Then, run the following command to create an executable:
```sh
pyinstaller --onefile --add-data "assets/images:assets/images" --add-data "assets/fonts:assets/fonts" --noconsole src/midtown_app.py
```
This will generate the executable in the `dist` directory. It will also create a `build` directory and `.spec` file. These are used in the build process and can be safely removed.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
This project was developed as part of an assignment at TAFE Queensland for subject ICTPRG434-435.

Icons used in the app are designed by Freepik - [www.freepik.com](https://www.freepik.com).

Fonts used in the app are open source Google Fonts.

## Source Code
The source code for this project can be found in the GitHub repository: [https://github.com/LukeWait/midtown-app](https://www.github.com/LukeWait/midtown-app).

## Dependencies
For those building from source, the dependencies listed in `requirements.txt` are:
- CTkToolTip==0.8
- customtkinter==5.2.1
- darkdetect==0.8.0
- Pillow==10.1.0
