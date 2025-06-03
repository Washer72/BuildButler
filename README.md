# BuildButler

**BuildButler** is a professional Python packaging tool that streamlines the process of converting Python scripts into polished Windows executables using PyInstaller. Designed with a modern, user-friendly Tkinter GUI, BuildButler offers advanced features such as custom window icon injection (supporting both PNG and ICO formats), dynamic version metadata embedding (with locale support), animated progress feedback, asynchronous audio notifications upon build completion, and comprehensive cleanup of all temporary files generated during the build process.

---

## Features

- **User-Friendly GUI:**  
  A multi-tab interface featuring separate areas for selecting the source script, resource files, version metadata, and the build process.

- **Custom Window Icon Injection:**  
  Embed a custom window icon directly into your Python script. Supports both PNG and ICO files—ICO files are automatically converted to PNG using the Pillow library.

- **Dynamic Version Information:**  
  Automatically generate and embed detailed version metadata (including customizable software name, version, company information, and localized fields) into the final executable. The locale is selectable but locked during conversion to avoid mid-build changes.

- **Animated Progress Bar:**  
  An indeterminate green progress bar indicates build activity, keeping users informed throughout the packaging process.

- **Audio Completion Notification:**  
  Plays an embedded Base64-encoded WAV audio signal upon successful packaging. Playback occurs in a separate thread, ensuring the UI remains responsive.

- **Comprehensive Cleanup:**  
  Automatically removes all temporary artifacts (such as the PyInstaller spec file, build directory, injected script file, and version info file) along with any extra files created during conversion, leaving only the final executable.

---

## Prerequisites

- **Python 3.6+**

- **PyInstaller:**  
  Install via pip:
  ```bash
  pip install pyinstaller
  ```

- **Pillow (Optional):**  
  Required if you intend to use ICO files for window icons (to convert ICO to PNG). Install via:
  ```bash
  pip install pillow
  ```

*Note:* The `winsound` module used for audio notifications is built-in with Python on Windows.

---

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/buildbutler.git
   cd buildbutler
   ```

2. **Install Dependencies:**

   Ensure PyInstaller and Pillow (if needed) are installed as described above.

3. **Run BuildButler:**
   ```bash
   python buildbutler.py
   ```

---

## Usage

1. **Launch the Application:**  
   Start BuildButler by running the main Python script.

2. **Main Tab:**
   - **Select Python Script:** Choose the Python script you wish to convert.
   - **Output Folder:** Specify the directory where the final executable should be saved.
   - **Executable Filename:** Provide a custom filename or leave it blank to use the source file’s name.

3. **Resources Tab:**
   - **Window Icon:** Browse for an image file (PNG or ICO) to use as the window icon.
   - **Executable Icon:** Select an ICO file to serve as the icon for the final executable.

4. **Versioning Tab:**
   Enter the version metadata including:
   - Software name
   - Version number (e.g., 1.0.0.0)
   - Company name
   - A short description
   - Copyright details
   - Author
   - Locale  
   *Note:* The locale combobox is locked during the build process and re-enabled after conversion.

5. **Build Tab:**
   Click **Start Packaging** to begin the build. The progress bar will animate while PyInstaller processes your script, and when conversion is complete, a completion sound will play and all temporary files will be automatically cleaned up.

---

## Contributing

Contributions are welcome! To report a bug or propose a new feature, please follow these steps:

1. Fork this repository.
2. Create your feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -am 'Add a new feature'
   ```
4. Push your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a Pull Request against the main branch.

---

## License

This project is released under the **BuildButler Non-Commercial License**.

### BuildButler Non-Commercial License

```
BuildButler Non-Commercial License

Copyright (c) [Year] [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software (the "Software") and associated documentation files (the "Documentation"), to use, modify, and distribute the Software for non-commercial purposes only, subject to the following conditions:

1. **Non-Commercial Use:**  
   The Software is provided solely for non-commercial, personal, and educational use. The Software or any derivative works may not be sold, licensed, or otherwise used for commercial gain without the express written consent of the Copyright Holder.

2. **Disclaimer of Warranty:**  
   THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

3. **Liability:**  
   The Software is distributed without any guarantees regarding its functionality or suitability for any particular purpose. By using the Software, you agree that the authors are not liable for any corruption, damage, or loss of work files or data that may result from its use.

4. **Attribution:**  
   Any distribution of the Software, with or without modifications, must include this license text and appropriate attribution to the original author(s).

By using this Software, you agree to these terms.
```

---

## Contact

For any questions, feedback, or support, please contact [Your Name](mailto:your.email@example.com).

---

## Acknowledgements

- Built using Python's Tkinter library.
- Packaging powered by PyInstaller.
- Icon conversion provided by Pillow.
- Special thanks to the open-source community for continuous support and inspiration.

---

*BuildButler streamlines Python packaging while ensuring that every executable looks professional and functions seamlessly. Enjoy creating flawless builds with BuildButler!*
