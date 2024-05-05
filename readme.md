# SharePoint Utility

This Python package provides utility functions for working with SharePoint files & folders.

## Installation
  
```bash
!pip  install  sharepoint-utils
```
## Usage

### available functions
```python
# functions for connection, reading and uploading files.
from sharepoint_utils import  connect_to_sharepoint
from sharepoint_utils import  upload_dataframe_to_sharepoint
from sharepoint_utils import  read_file_from_sharepoint

# functions for reading files and folders.
from sharepoint_utils import  combine_files_into_dataframe
from sharepoint_utils import  get_folder_urls
from sharepoint_utils import  get_file_paths
from sharepoint_utils import  copy_files_within_folders
```
### Usage Examples

```python
# Create connection to sharepoint
sharepoint_ctx = connect_to_sharepoint('your_username', 'your_password', 'https://your_sharepoint_site_url')

# Combine files into a DataFrame
folder_path = 'relative/folder/path'
df = combine_files_into_dataframe(sharepoint_ctx, folder_path)

# Upload DataFrame to SharePoint folder as a csv file
folder_path = '/folder_path/'
upload_dataframe_to_sharepoint(ctx, folder, df, 'your_file_name.csv')

# get sharepoint folder url as a list
folder_urls  =  get_folder_urls(sharepoint_ctx, document_library_relative_url)
print(folder_urls)

# get sharepoint file path as a list
file_paths  =  get_file_paths(sharepoint_ctx, subfolder_urls_files)
print(file_paths)

# copy files from one folder to another within sharepoint site
copy_files_within_folders(ctx, filepath , files_upload_to_path)
``` 
### Contributing

  

Contributions are welcome! If you have any suggestions or find any issues, please feel free to contact me.