# Image Downloader

Image downloader python script finds image URLs scraped by Image Selector in a CSV file and downloads them.
Images are renamed as `.csv file link source`.

### Windows usage

1. Download & install python 3.x from:
[https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download `Image-Downloader.py` script from:
[https://github.com/amiMohammad/Image_Downloader][Image_Downloader]
3. Scrape the target site and export data as CSV file
4. Edit CSV file so that, CSV file has no `Serial column` or `Header row`. Only `Link column` is present
5. Drag and drop the CSV file on top of the `Image_Downloader.py`
![Fig. 1: windows image download][windows-image-download-script]

### Windows troubleshooting

If Windows reports that `python` or `py` is not recognized, or opens the Microsoft Store instead of starting Python, Python is installed but its command is not available in your command prompt. The `python.exe` and `py.exe` commands may also point to different installations.

#### Check which Python commands are available

Open **Command Prompt** (`cmd.exe`) and run:

```bat
python --version
py --version
where python
where py
```

- `python --version` and `py --version` should print a Python 3 version.
- `where python` and `where py` show the executable paths that Windows is using. If more than one path is listed, an older installation or a Microsoft Store alias may be taking priority.
- `py -3 --version` explicitly checks for the Python 3 launcher.

Run the script with whichever command works, for example:

```bat
py -3 Image_Downloader.py scraped_data.csv
```

If the script and CSV file are in the same folder, you can first change to that folder:

```bat
cd /d C:\Users\YourName\Downloads
py -3 Image_Downloader.py scraped_data.csv
```

Replace `YourName` and the file names with your own values. Drag-and-drop normally uses the file association configured for `.py` files; using Command Prompt makes it easier to see the actual error message.

#### Fix a missing or incorrect Python command

1. Uninstall duplicate or unused Python installations from **Settings > Apps > Installed apps**, if necessary. Keep the installation you intend to use.
2. Install Python from [python.org](https://www.python.org/downloads/windows/). During setup, enable **Add python.exe to PATH** before selecting **Install Now**. The Python installer includes the `py.exe` launcher on Windows.
3. Close and reopen Command Prompt, then run `python --version`, `py --version`, and `where python` again. A new command prompt is required because existing windows do not automatically reload PATH changes.
4. If Python is installed but is not on PATH, run the installer again and choose **Modify > Add Python to environment variables**, or add the Python installation directory and its `Scripts` directory to the user PATH manually. Typical paths include:
   - `%LocalAppData%\Programs\Python\Python3x\`
   - `%LocalAppData%\Programs\Python\Python3x\Scripts\`
   - `C:\Program Files\Python3x\`

The exact directory depends on the Python version and whether Python was installed for one user or for all users. Do not add a guessed path such as `C:\Windows\python.exe`; Python is normally installed under your user profile or `Program Files`, not in the Windows directory. Use the path returned by `where python` or the Python installer's **Customize installation** screen.

#### Microsoft Store, MSIX, and `python.exe` aliases

Windows may provide small `python.exe` and `python3.exe` **App execution aliases** in `C:\Windows\System32` that redirect to the Microsoft Store. This can happen when Python was not installed from python.org, or when the Microsoft Store version was installed as an MSIX package. It is not the same as the real Python interpreter.

To disable the Store redirect:

1. Open **Settings > Apps > Advanced app settings > App execution aliases**.
2. Turn off the `python.exe` and `python3.exe` aliases under **App Installer**.
3. Open a new Command Prompt and verify `where python` and `python --version`.
4. If no real installation is found, install Python from [python.org](https://www.python.org/downloads/windows/) or install the Microsoft Store version intentionally, then verify the command again.

The Microsoft Store/MSIX version can work, but its package location is managed by Windows and may differ from a traditional `.exe` installation. File associations, PATH behavior, permissions, virtual environments, and the `py` launcher may therefore behave differently. For the most predictable result with this script, use the official python.org `.exe` installer and enable **Add python.exe to PATH**. Avoid mixing Store/MSIX and python.org installations unless you know which one `where python` and `where py` select.

#### If `py.exe` is missing or points to another version

`py.exe` is the Python launcher, not the Python interpreter itself. It can be installed or removed separately from the main Python installation. If `py --version` fails, repair or reinstall Python using the python.org installer and include the launcher. If several Python versions are installed, use an explicit version:

```bat
py -3 Image_Downloader.py scraped_data.csv
```

If `py` starts a different version than expected, remove old installations or use the full path to the intended interpreter. You can find the interpreter selected by the launcher with:

```bat
py -0p
```

Do not copy or rename `python.exe` or `py.exe` into `C:\Windows`. Changing files in the Windows directory can create permission and security problems; fix PATH, app execution aliases, or the installation instead.

### macOS, Linux usage

1. Install python if necessary through your package manager. Most likely you already have it pre-installed.
2. Download `Image_Downloader.py` script from here:
[https://github.com/amiMohammad/Image_Downloader][Image_Downloader]
3. Move `Image_Downloader.py` to `Downloads` directory
4. Scrape the target site and export data as CSV file
5. Save the CSV file in `Downloads` directory
6. Edit CSV file so that, CSV file has no `Serial column` or `Header row`. Only `Link column` is present
7. Open `Terminal` application. You should have one pre-installed
8. Change working PATH to `Downloads` directory by typing:
    ```bash
    cd Downloads
    ```
9. Run image downloader script by typing:
    ````bash
    python Image_Downloader scraped_data.csv
    ````

![Fig. 2: macOS image download][osx-image-download-script]

 [windows-image-download-script]: Tutorials/Windows_Tutorial.gif?raw=true
 [osx-image-download-script]: Tutorials/OSX_Tutorial.gif?raw=true
 [Image_Downloader]: https://github.com/amiMohammad/Image_Downloader/releases
