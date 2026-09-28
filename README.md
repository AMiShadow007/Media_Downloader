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
