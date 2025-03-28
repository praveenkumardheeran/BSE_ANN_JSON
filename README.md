# BSE Announcement Downloader

This Python project allows users to download stock announcement data from the Bombay Stock Exchange (BSE) using its public API. The application provides a graphical user interface (GUI) built with **Tkinter** to interact with the BSE API and export the data to a JSON file.

### Features

- **Fetch Announcement Count**: Fetch the number of announcements for a specific date.
- **Download Data**: Download all announcements for the given date.
- **Export Data**: Export the downloaded announcement data into a JSON file.
- **Multi-page Support**: Handles downloading announcements across multiple pages from the BSE API.
- **Threading for Progress**: Uses threading to ensure the GUI remains responsive while downloading data.

---

## Requirements

To run this project, you'll need the following Python libraries installed:

- `tkinter` (for the GUI)
- `requests` (for API calls)
- `Pillow` (for image handling, though it's not directly used in this code)
- `json` (for processing data in JSON format)
- `datetime` (for managing date-related tasks)

You can install the required libraries with the following:

```bash
pip install requests Pillow
```

---

## Setup & Installation

1. **Clone the repository** or download the `bse_announcements.py` script.

2. Ensure you have Python installed (Python 3.x recommended).

3. Install the necessary Python packages as mentioned in the requirements section.

4. Run the script by executing the following command:

```bash
python bse_announcements.py
```

---

## How It Works

The application communicates with the BSE API to retrieve stock announcements. Here's an overview of how the program works:

1. **Get Page Counts**: 
   - Enter a specific date in the format `YYYYMMDD` in the date entry box.
   - Click the **"Get page counts"** button to retrieve the total number of announcements for that date.

2. **Download Announcements**:
   - After retrieving the page count, click **"Download Announcement"** to download the announcement data.
   - The application will download the announcements in batches (pages) and display progress on the interface.

3. **Export to JSON**:
   - Once the data has been downloaded, you can click the **"Export Json file"** button to export the data to a JSON file.
   - The file is saved in the format `BSE_ann_YYYYMMDD.json` where `YYYYMMDD` is the current date.

---

## GUI Overview

The GUI is created using **Tkinter**, and includes the following components:

- **Announcement Date**: 
  A text entry field where you can input the date for which you want to fetch announcements.

- **Get Page Counts**: 
  A button to retrieve the total count of announcements for the given date.

- **Download Announcement**: 
  A button that triggers the download of announcements from the BSE API.

- **Export Json file**: 
  A button to export the downloaded announcements to a JSON file.

- **Status Updates**: 
  Labels are used to show the status of the download and display page count information or any errors.

---

## Example Workflow

1. When you open the application, the default date (current date) is shown in the date entry field.
2. Enter the desired date for announcements in the format `YYYYMMDD` (e.g., `20250328`).
3. Click **"Get page counts"** to fetch the total number of announcements for that date.
4. Click **"Download Announcement"** to start downloading the announcements.
5. After the download completes, click **"Export Json file"** to save the announcements as a JSON file.

---

## Notes

- The BSE API returns data in paginated format, so the application downloads announcements in pages. The number of pages is calculated based on the total count of announcements.
- The download and export operations are executed in separate threads to prevent the GUI from freezing during the process.
- Ensure that you have a stable internet connection to retrieve data from the BSE API.

---

## Acknowledgments

- The **requests** library is used to interact with the BSE API.
- The **Tkinter** library is used to create the GUI.

---

Let me know if you need further modifications or additions!
