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
  Plays an embedded Base64-encoded WAV audio signal upon successful packaging. Playback is handled in a separate thread so the UI remains responsive.

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
   git clone https://github.com/Washer72/buildbutler.git
   cd buildbutler
   ```

2. **Install Dependencies:**

   Ensure PyInstaller and Pillow (if needed) are installed as described in the prerequisites.

3. **Run BuildButler:**

   Launch the application by running the main Python script:
   ```bash
   python buildbutler.py
   ```

---

## Usage

1. **Launch the Application:**  
   Start BuildButler via the script.

2. **Main Tab:**  
   - **Select Python Script:** Choose the Python script you wish to convert.
   - **Output Folder:** Specify the folder where the final executable should be saved.
   - **Executable Filename:** Provide a custom filename or leave it blank to use the source file name.

3. **Resources Tab:**  
   - **Window Icon:** Browse for an image file (PNG or ICO) to use as the window icon.  
   - **Executable Icon:** Select an ICO file to serve as the icon for the executable.

4. **Versioning Tab:**  
   Enter the version metadata including software name, version number (e.g., 1.0.0.0), company name, a short description, copyright details, author, and locale.  
   *Note:* The locale combobox is locked during the build process and re-enabled once conversion is complete.

5. **Build Tab:**  
   Click **Start Packaging** to begin the build. The progress bar will animate while PyInstaller packages your script. When conversion is complete, a completion sound will play and all temporary files will be automatically cleaned up.

---

## Contributing

Contributions are welcome! If you find a bug or have new feature ideas, please follow these steps:

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

This project is licensed under the [MIT License](LICENSE).

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
