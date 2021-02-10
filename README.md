![Preview](images/preview.gif)

# Updater
Delphi App to synchronize folder contents

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/C0C53LVFN)

Please, read the article on my website: http://digaodalpiaz.com/wp/folder-and-file-synchronizer/

**Warning! The incorrect use of this application can result in data loss, considering that the sync destination folder may have its files replaced and / or deleted according to the configuration. Always confirm the destination folder path and use secure mode to test your settings.**

## Description

This application allows you to keep files synchronized by creating a list of repositories and allowing options like masks inclusions and exclusions.

The synchronization method is based on files write date/time property, so the application can quickly check if a file is updated.

There is a masks tables area, where you can insert several lists of masks, avoiding repeating group of masks in your repositories. In inclusions and exclusions masks, you can specify a literal mask, or specify a masks table, by prefixing table name with `:`.

![Masks Tables](images/masks_tables.png)

![Edit Definition](images/edit_definition.png)

> All changes to files are made only in the destination folder. The source folder is never modified.

### The changes can be of the following types:
- Added: When a file exists at the source but does not exist at the destination. In this case, the file will be created at the destination.
- Modified: When a file exists at the source and at the destination, but the file change timestamp is different, that is, the file has been modified. In this case, the file will be replaced at the destination with the new content from the source.
- Deleted: When a file or folder exists at the destination, but no longer exists at the source. **In this case, the file will be excluded from the destination (only when the exclusion option is enabled in the definition settings)**.

## Dependency

To compile this application you need the DzDirSeek component, available here on GitHub: https://github.com/digao-dalpiaz/DzDirSeek

## To Do

- ~~ToolBar hidden when process running may look strange.~~
- ~~Splitter locked when process running because CheckListBox disabled.~~
- ~~Implement Masks Tables.~~
- ~~Help info in inclusions/exclusions memo.~~
- ~~Allow comments in inclusions/exclusions masks.~~
- ~~Change app theme.~~
- ~~Show total size on files report.~~
- ~~Deleted files are internally getting size but never used.~~
- ~~Folders are not being deleted from the destination when there are no more files left.~~
- Attributes are not being copied from the file/folder.
