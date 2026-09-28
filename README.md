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

If Windows says `python` or `py` is not recognized, or opens the Microsoft Store, try this:

1. Open **Command Prompt**.
2. Run:

```bat
python --version
py --version
where python
where py
```

If these commands fail, install Python from [python.org](https://www.python.org/downloads/windows/) and make sure **Add python.exe to PATH** is checked.

Then use:

```bat
py -3 Image_Downloader.py scraped_data.csv
```

If your script and CSV file are in a different folder, first change to that folder:

```bat
cd /d C:\Users\YourName\Downloads
py -3 Image_Downloader.py scraped_data.csv
```

#### Common Windows issues

- `python` works but `py` does not: reinstall Python and include the launcher.
- Python opens the Microsoft Store: disable the App execution alias for `python.exe` and `python3.exe` in Windows settings.
- Multiple Python versions are installed: use `py -3` to force Python 3.
- Python is missing from PATH: reinstall Python and enable **Add python.exe to PATH**.

For most users, the easiest fix is to install Python from python.org and run the script with:

```bat
py -3 Image_Downloader.py scraped_data.csv
```

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
