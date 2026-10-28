# Packet Tracer – Use FTP Services

## Overview
This lab demonstrates file transfers between a client PC and an FTP server using Cisco Packet Tracer. It covers uploading, downloading, renaming, listing, and deleting files through the FTP client.

## Objectives
- Connect to an FTP server.
- Authenticate using FTP credentials.
- Upload a file from a client to the server.
- Rename and download a file from the server.
- Delete a file from the FTP server.

## Tools Used
- Cisco Packet Tracer
- FTP client
- Command Prompt

## Network Configuration

| Device | IP Address | Subnet Mask |
|---|---|---|
| FTP Server (ftp.pka) | 209.165.200.226 | 255.255.255.224 |

## Procedure

### 1. Locate the file
Opened the Command Prompt on PC-A and used `dir` to locate `sampleFile.txt`.

### 2. Connect to the FTP server
Connected to the server using:

`ftp 209.165.200.226`

Logged in using the lab-provided credentials.

### 3. Upload a file
Used the following command:

`put sampleFile.txt`

Used `dir` to verify that the file was present on the server.

### 4. Rename the file
Renamed the uploaded file using:

`rename sampleFile.txt sampleFile_FTP.txt`

### 5. Download the file
Retrieved the renamed file using:

`get sampleFile_FTP.txt`

Used `dir` on PC-A to check the downloaded file.

### 6. Delete the server file
Removed the renamed file from the FTP server using:

`delete sampleFile_FTP.txt`

Exited the FTP client using `quit`.

## Key Concepts Learned
- FTP client-server communication
- FTP authentication
- File upload and download
- Remote file management
- FTP control and data connections
- Command-line networking tools

## Protocol and Security Notes
Traditional FTP uses TCP port 21 for control connections and commonly TCP port 20 for data connections in active mode. Passive mode uses server-selected data ports.

FTP does not encrypt credentials or file contents. For secure file transfers, SFTP or FTPS is generally preferable.

## Evidence
Screenshots of the FTP login, file upload, file download, and deletion are stored in the `screenshots/` directory.

## Skills Demonstrated
Cisco Packet Tracer, FTP, TCP/IP, client-server communication, file management, and command-line troubleshooting.
