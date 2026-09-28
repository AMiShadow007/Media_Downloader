# Image Downloader

Image downloader script finds image urls scraped by Image Selector in a csv file and downloads them.
Images are renamed as `.csv file link source`.

### Windows usage

1. Download and install python 3.x from here:
[https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download image downloader script from here:
[https://github.com/amiMohammad/Image_Downloader][Image_Downloader]
3. Scrape the target site and export data in CSV format
4. Edit CSV file so that, CSV file has no `Serial column` or `Header row`. Only `Link column` is present
5. Drag and drop the CSV file on top of the `Image_Downloader.py`
![Fig. 1: windows image download][windows-image-download-script]

### macOS, Linux usage

1. Install python if necessary through your package manager. Most likely you already have it preinstalled.
2. Download image downloader script from here:
[https://github.com/amiMohammad/Image_Downloader][Image_Downloader]
3. Move `Image_Downloader.py` to `Downloads` directory
4. Scrape the target site and export data in CSV format
5. Save the CSV file in `Downloads` directory
6. Open `Terminal` application. You should have one pre-installed
7. Change working PATH to `Downloads` directory by typing:
    ```bash
    cd Downloads
    ```
8. Run image downloader script by typing:
    ````bash
    python Image_Downloader scraped_data.csv
    ````

![Fig. 2: macOS image download][osx-image-download-script]

 [windows-image-download-script]: Tutorials/Windows_Tutorial.gif?raw=true
 [osx-image-download-script]: Tutorials/OSX_Tutorial.gif?raw=true
 [Image_Downloader]: https://github.com/amiMohammad/Image_Downloader/releases