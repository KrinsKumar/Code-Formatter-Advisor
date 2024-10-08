# Code-Formatter-Advisor

Code-Formatter-Advisor is a command-line tool that leverages GroqCloud API to analyze code and provide formatting improvement suggestions. It offers a streamlined interface for specifying input files, customizing outputs, and enhancing code readability and consistency. The tool supports multiple programming languages and integrates seamlessly into your workflow by delivering suggestions directly in the terminal or saving them to a file.

## 📜Description

- Provides code formatting suggestions based on best practices.
- Supports multiple programming languages.
- Easy-to-use command-line interface.
- Ability to output suggestions to a file or display them in the terminal.

## ⚙️Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Elisassa/Code-Formatter-Advisor.git
    cd Code-Formatter-Advisor
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## 📝Usage 

### Command-Line Arguments

- `--output` or `-o`: Specify the output file name for the suggestions.
- `--version` or `-v`: Display the version of the tool.
- `files`: The code files to be analyzed (one or more).

### Example Commands

1. Analyze a single file and display suggestions in the terminal:
    ```bash
    python main.py test.py
    ```

2. Analyze multiple files and save suggestions to an output file:
    ```bash
    python main.py test1.py test2.py --output suggestions.txt
    ```

3. Check the version of the tool:
    ```bash
    python main.py --version
    ```

## 🔍Demonstration

The **Code-Formatter-Advisor** analyzes your code and provides actionable formatting suggestions to improve readability and consistency. Below is a demonstration of how the tool works:

#### Original Unformatted Code:

Below is an example of code before using Code-Formatter-Advisor. Notice the issues such as inconsistent indentation, missing type hints, and lack of descriptive comments.

![image](https://github.com/user-attachments/assets/668a2687-f656-45ff-9df1-680b10d19c03)


### Suggested Improvements by Code-Formatter-Advisor:

After running the code through Code-Formatter-Advisor, the tool suggests various improvements such as:

- **Consistent Indentation**: Standardizes indentation to 4 spaces for better readability.
- **Removal of Extra Spaces**: Removes unnecessary spaces around function arguments, colons, and assignment operators.
- **Descriptive Function Names**: Renames functions to be more descriptive, like changing `add_numbers` to `sum_numbers`.
- **Addition of Docstrings**: Adds docstrings to describe the purpose and usage of functions, making the code self-documenting.
- **Type Hints**: Adds type hints to function arguments and return values to clarify the expected input and output.

![Formatted Code Suggestions](https://github.com/user-attachments/assets/4c8b24ea-668a-4461-8cd4-16278cbfeef0)



## 🛠️How Code-Formatter-Advisor Was Created

### Project Setup

1. **Initialization**: The project was initialized by setting up a basic Python environment using `venv` to manage dependencies.

2. **Dependencies**: Required libraries were defined and installed via a `requirements.txt` file, including `argparse` for command-line argument parsing, `dotenv` for environment variable management, and others for formatting analysis.

3. **Development**:
   - The main logic is implemented in `main.py`, which handles reading files, interacting with the code formatting API, and processing user inputs.
   - `argparse` is used to handle command-line arguments, allowing users to specify files, output locations, and other options.
   - A custom API client (`Groq`) was integrated to analyze code and provide formatting suggestions.




