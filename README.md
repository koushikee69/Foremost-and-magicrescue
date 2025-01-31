File Carving Tool using Foremost and MagicRescue
===============================================

This Python script allows you to run **foremost** and **magicrescue** to carve specific files from an image or device. The program accepts command-line arguments to specify the tool, input file, output directory, and the type of file to recover.

Features
--------
- Supports both **foremost** and **magicrescue** tools.
- Recovers files based on user-specified file types or recipe types.
- Saves recovered files to the specified output directory.
- Takes input and output paths, and the file type or recipe type as command-line arguments.

Prerequisites
-------------
- Python 3.x
- **foremost** and **magicrescue** tools installed
- `sudo` privileges for running the tools with the necessary permissions

Usage
-----
Run the script with the following command-line arguments:

    python carve_files.py <toolName> <inputDirectory> <outputDirectory> <configFile>

Arguments:
1. **toolName**: The tool to use (`foremost` or `magicrescue`).
2. **inputDirectory**: The file or device image from which files will be recovered.
3. **outputDirectory**: The directory where recovered files will be saved.
4. **configFile**: The type of file(s) to carve for `foremost`, or the recipe type for `magicrescue`.

Example:
--------

For **foremost**:

    python carve_files.py foremost /path/to/image /path/to/output png

For **magicrescue**:

    python carve_files.py magicrescue /path/to/image /path/to/output jpg

How It Works
------------
1. The script checks which tool (`foremost` or `magicrescue`) is provided.
2. It then runs the appropriate tool using the specified file type (for **foremost**) or recipe type (for **magicrescue**).
3. Recovered files are stored in the output directory.
