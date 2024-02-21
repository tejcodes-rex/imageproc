Image Processing Tool Documentation
The Image Processing Tool is a command-line utility designed to perform various operations on image files within a specified directory. It supports common image processing tasks such as resizing, renaming, rotating, converting formats, compressing, applying watermarks, cropping, auto-orientation correction, and custom naming patterns.

Table of Contents
Installation
Usage
Operations
Resize
Rename
Rotate
Grayscale
Convert
Compress
Watermark
Crop
Auto-Orient
Custom Naming
Custom Output Naming
Command-line Options
Examples
Logging
Continue Processing
Contributing
License
Installation
The Image Processing Tool is a Python script that requires the following dependencies:

Python (version 3.6 or higher)
Pillow (Python Imaging Library Fork)
To install the required dependencies, run the following command:

bash
Copy code
pip install pillow
No additional installation steps are required for the Image Processing Tool.

Usage
The basic usage of the Image Processing Tool is as follows:

bash
Copy code
python image_processing_tool.py <operation> [options]
Replace <operation> with the desired operation (e.g., resize, rename). Additional options specific to each operation can be provided.

Operations
Resize
Resize images to a specified width and height.

Options:

--width: Width for resizing images (default: 400)
--height: Height for resizing images (default: 300)
Example:

bash
Copy code
python image_processing_tool.py resize --width 800 --height 600 --input /path/to/images --output /path/to/output
Rename
Rename images with a specified prefix and starting index.

Options:

--prefix: Prefix for renaming images (default: "project-")
--start-index: Starting index for renaming images (default: 1)
Example:

bash
Copy code
python image_processing_tool.py rename --prefix new-project- --start-index 10 --input /path/to/images --output /path/to/output
Rotate
Rotate images by a specified number of degrees.

Options:

--degrees: Degrees for rotating images (default: 90)
Example:

bash
Copy code
python image_processing_tool.py rotate --degrees 180 --input /path/to/images --output /path/to/output
Grayscale
Convert images to grayscale.

Example:

bash
Copy code
python image_processing_tool.py grayscale --input /path/to/images --output /path/to/output
Convert
Convert images to a specified format.

Options:

--format: Target format for conversion (default: "PNG")
Example:

bash
Copy code
python image_processing_tool.py convert --format JPEG --input /path/to/images --output /path/to/output
Compress
Compress images with a specified quality level.

Options:

--quality: Quality for image compression (1-100, default: 85)
Example:

bash
Copy code
python image_processing_tool.py compress --quality 75 --input /path/to/images --output /path/to/output
Watermark
Apply a watermark to images.

Options:

--watermark: Path to the watermark image
Example:

bash
Copy code
python image_processing_tool.py watermark --watermark /path/to/watermark.png --input /path/to/images --output /path/to/output
Crop
Crop images to specified dimensions.

Options:

--crop-left: Left coordinate for cropping (default: 0)
--crop-top: Top coordinate for cropping (default: 0)
--crop-right: Right coordinate for cropping (default: 0)
--crop-bottom: Bottom coordinate for cropping (default: 0)
Example:

bash
Copy code
python image_processing_tool.py crop --crop-left 10 --crop-top 20 --crop-right 30 --crop-bottom 40 --input /path/to/images --output /path/to/output
Auto-Orient
Apply auto-orientation correction to images based on EXIF data.

Example:

bash
Copy code
python image_processing_tool.py auto-orient --input /path/to/images --output /path/to/output
Custom Naming
Rename images using a custom naming pattern.

Options:

--naming-pattern: Custom naming pattern (default: "{name}_{index}")
Example:

bash
Copy code
python image_processing_tool.py custom-naming --naming-pattern custom_name_{index} --input /path/to/images --output /path/to/output
Custom Output Naming
Copy images to custom output folders based on a naming pattern.

Options:

--output-naming-pattern: Custom output folder naming pattern (default: "{name}_output")
Example:

bash
Copy code
python image_processing_tool.py custom-output-naming --output-naming-pattern output_{name} --input /path/to/images --output /path/to/output
Command-line Options
The Image Processing Tool supports the following command-line options:

--input: Input folder path (default: current working directory)
--output: Output folder path (default: "output")
--log-file: Log file path (default: "image_processing.log")
--continue: Continue processing images without prompts
For operation-specific options, refer to the documentation for each operation.

Examples
Here are some examples demonstrating the usage of the Image Processing Tool:

Resize images to 800x600:

bash
Copy code
python image_processing_tool.py resize --width 800 --height 600 --input /path/to/images --output /path/to/output
Rename images with a custom prefix and starting index:

bash
Copy code
python image_processing_tool.py rename --prefix new-project- --start-index 10 --input /path/to/images --output /path/to/output
Rotate images by 180 degrees:

bash
Copy code
python image_processing_tool.py rotate --degrees 180 --input /path/to/images --output /path/to/output
Convert images to JPEG format:

bash
Copy code
python image_processing_tool.py convert --format JPEG --input /path/to/images --output /path/to/output
Apply a watermark to images:

bash
Copy code
python image_processing_tool.py watermark --watermark /path/to/watermark.png --input /path/to/images --output /path/to/output
Crop images to specific dimensions:

bash
Copy code
python image_processing_tool.py crop --crop-left 10 --crop-top 20 --crop-right 30 --crop-bottom 40 --input /path/to/images --output /path/to/output
For more examples and details on each operation, refer to the Operations section.

Logging
The Image Processing Tool generates a log file (image_processing.log) in the current working directory. The log file contains information about each processed image, including successful operations and any encountered errors.

Continue Processing
By default, the Image Processing Tool prompts the user after each operation to confirm whether they want to continue processing more images. To bypass these prompts and continue processing images without interruptions, use the --continue option:

bash
Copy code
python image_processing_tool.py <operation> --continue
This option is useful when processing a large number of images in a batch.

Contributing
Contributions to the Image Processing Tool are welcome! If you encounter any issues, have suggestions for improvements, or want to add new features, feel free to open an issue or submit a pull request.

License
The Image Processing Tool is open-source software released under the MIT License. You are free to use, modify, and distribute the tool as per the terms of the license.
