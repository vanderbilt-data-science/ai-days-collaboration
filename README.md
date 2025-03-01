# ai-days-collaboration
Process research statements/CVs and find relationship for attendees.

# AI Days Collaboration Matcher

A tool for AI Days 2025 conference organizers to process attendees' CVs and research statements to identify potential collaboration opportunities.

## 🔍 Overview

This Google Colab notebook extracts research interests from heterogeneous documents (CVs, resumes, and research statements), normalizes them into a consistent format, and helps identify potential research collaborations between conference attendees.

It's specifically designed to help AI Days 2025 conference organizers facilitate meaningful connections between participants who have complementary research interests, with the goal of fostering new collaborations during the 10-day conference.

## 🌟 Features

- **Document Processing**: Extract text from PDFs, Word documents, and plain text files
- **Smart Classification**: Automatically determine if a file is a resume or research statement
- **Research Interest Extraction**: Use Claude 3.7 Sonnet to convert resumes into research statements
- **Name Extraction**: Automatically extract attendee names from filenames and folders
- **Error Handling**: Robust processing that continues even if some files cause errors
- **Comprehensive Logging**: Detailed processing results saved to CSV

## 📋 Prerequisites

- Google Colab environment
- Anthropic API key with access to Claude 3.7 Sonnet
- Access to Google Drive with attendee documents
- The following Python packages (automatically installed in the notebook):
  - `anthropic`
  - `PyPDF2`
  - `python-docx`

## 🚀 Usage

1. Open the notebook in Google Colab
2. Run the setup cell to install required packages
3. Set your Anthropic API key and file paths
4. Run the processing cells

```python
# Install required packages
install_required_packages()

# Set your API key and paths
ANTHROPIC_API_KEY = "your_anthropic_api_key"
INPUT_DIR = "/content/drive/MyDrive/path/to/your/files"
OUTPUT_DIR = "/content/drive/MyDrive/path/to/output"

# Run the generator
generator = ResearchStatementGenerator(INPUT_DIR, OUTPUT_DIR, ANTHROPIC_API_KEY)
generator.scan_directory()
generator.process_files()
generator.save_results()
```

## 📊 Output

The tool generates several outputs:

1. **Individual research statements**: One text file per attendee
2. **Processing results CSV**: Records of all processed files
3. **Combined JSON**: All research statements in a single file for further analysis and matching

## 📎 Examples and Sample Outputs

[This section will be populated with examples after running the tool on sample data]

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Maintainer

Maintained by Jesse Spencer-Smith, Chief Data Scientist for the Data Science Institute at Vanderbilt University.

## 🙏 Acknowledgments

- [Anthropic](https://www.anthropic.com/) for the Claude API
- [Google Colab](https://colab.research.google.com/) for the notebook environment
