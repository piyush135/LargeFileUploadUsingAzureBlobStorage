Azure Blob File Uploader
This project is a robust file uploader component with direct integration to Azure Blob Storage. It supports multiple file uploads, progress visualization, large file handling, and customizable configurations for an enhanced user experience.

Features
Multiple File Uploads: Users can select and upload multiple files simultaneously.
Progress Visualization: Each file's upload progress is displayed with a visual progress bar.
Large File Support: Capable of handling large files, with a default maximum file size set to 2 GiB, configurable to support larger sizes.
File Type Icons: Automatically displays icons for different file types such as images and videos.
Azure Blob Integration: Seamlessly integrated with Azure Blob Storage for backend file storage.
Dependencies
Azure.Storage.Blobs: SDK for accessing Azure Blob Storage.
Provision and Deploy to Azure
Install Azure Developer CLI: Follow the instructions here to set up the Azure Developer CLI.
Test the Deployment:
Go to the endpoint provided by azd after the setup and try uploading a file.
Run Locally
Open the Solution: Open the solution in Visual Studio.
Run the Application: Press F5 to start the application and begin uploading files locally.
Usage
Embed the Component: Place the uploader component in your Blazor server-side application.
Customize Parameters: Adjust parameters like MaximumFileCount, Folder, and BlobContainer to tailor the uploader to your needs.
Parameters
Parameter	Description	Default Value
BlobContainer	The Azure Blob Storage container where files are uploaded.	"uploads"
Folder	The default folder path for uploads.	"default"
MaximumFileCount	The maximum number of files allowed per upload.	5
PreviewWidth	The width in pixels for preview images or icons.	100
MaximumFileSize	Maximum file size allowed for uploads (in bytes).	2 GiB (2,147,483,648)
InitialTransferSize	Initial upload chunk size (in bytes).	4 MiB (4,194,304)
MaximumTransferSize	Maximum transfer chunk size (in bytes).	4 MiB (4,194,304)
MaximumConcurrency	Maximum number of concurrent operations during file transfer.	2
SingleUrl	URL for a single uploaded file, used to pre-populate the upload box.	"" (empty string)
Event Handling
OnSingleUrlChanged: Triggered when the URL of a single uploaded file changes.
OnUploadFilesChanged: Triggered when the list of uploaded files changes.
Custom Progress Handler
This uploader includes a custom progress handler class that monitors upload progress and updates the UI accordingly, leveraging the IProgress interface to track each file's upload status.

Utilities
FileHelper: A utility class that helps identify file types based on extensions and formats file sizes for display.
Future Enhancements
Security: Integration with Azure Defender to scan uploaded files for potential malware.
Performance Optimization: Additional tuning of chunk sizes and concurrency settings for even faster uploads.
Summary
This uploader is ideal for applications that require advanced file management capabilities, including upload progress tracking and integration with Azure Blob Storage. It’s highly customizable to fit various use cases and can support substantial file uploads with ease.

