
# SharePoint Utility

The SharePoint Utility is a Python package designed to simplify the process of working with files and folders in SharePoint. It provides a set of utility functions that allow you to connect to SharePoint, read and upload files, and perform various operations on files and folders.

## Installation

To install the SharePoint Utility package, use the following pip command in your terminal:

```bash
!pip install sharepoint-utils
```

## Usage

The SharePoint Utility package provides several functions for connecting to SharePoint, reading and uploading files, and working with files and folders.

### Available Functions

```python
# Functions for establishing a connection, reading files, and uploading files.
from sharepoint_utils import read_file_from_different_library
from sharepoint_utils import read_file_from_default_library
from sharepoint_utils import combine_files_into_dataframe
from sharepoint_utils import copy_files_within_folders
from sharepoint_utils import upload_dataframe_as_csv
from sharepoint_utils import connect_to_sharepoint
from sharepoint_utils import get_folder_url
from sharepoint_utils import get_file_path
```

### Usage Examples

```python
# Establish a connection to SharePoint.
sharepoint_ctx = connect_to_sharepoint('your_username', 'your_password', 'https://your_sharepoint_site_url')

# Combine files into a DataFrame.
folder_path = 'relative/folder/path'
df = combine_files_into_dataframe(sharepoint_ctx, folder_path)

# Upload a DataFrame to a SharePoint folder as a CSV file.
folder_path = '/folder_path/'
upload_dataframe_as_csv(ctx, folder, df, 'your_file_name.csv')

# Retrieve SharePoint folder URLs as a list.
folder_urls = get_folder_url(sharepoint_ctx, document_library_relative_url)
print(folder_urls)

# Retrieve SharePoint file paths as a list.
file_paths = get_file_path(sharepoint_ctx, subfolder_urls_files)
print(file_paths)

# Copy files from one folder to another within the SharePoint site.
copy_files_within_folders(ctx, filepath , files_upload_to_path)
```

## Contributing

Contributions to the SharePoint Utility package are always welcome! If you have any suggestions for improvements or if you encounter any issues while using the package, please feel free to contact me. Your feedback and contributions will help make this package even better and more useful for everyone.