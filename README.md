📟 prompt-cli

> ⚠️ Notice: This project is currently under development and not fully functional.
Some features may be incomplete or unstable. Please use with caution.



A Node.js-based command-line interface (CLI) that takes unstructured or messy developer prompts and returns clean, structured prompts suitable for input into LLMs like OpenAI's GPT-4o.


---

📌 Purpose

prompt-cli is designed for:

Solo devs or teams using AI tools (e.g., ChatGPT, Cursor AI)

Streamlining messy feature requests into actionable coding instructions

Ensuring consistent, high-quality prompt inputs for AI-assisted development

Translating prompts from any language to English



---

🚀 Installation

From npm (recommended)

npm install -g prompt-cli-cleaner

Setting up your OpenAI API Key

After installation, you need to set up your OpenAI API key. There are two ways to do this:

Option 1: Create a .env file in your working directory

Create a file named .env in the directory where you'll be running the prompt command with the following content:

OPENAI_API_KEY=your_openai_api_key_here

Replace your_openai_api_key_here with your actual OpenAI API key.

Option 2: Set an environment variable

Windows (Command Prompt):

set OPENAI_API_KEY=your_openai_api_key_here

Windows (PowerShell):

$env:OPENAI_API_KEY="your_openai_api_key_here"

macOS/Linux:

export OPENAI_API_KEY=your_openai_api_key_here

To make this permanent, add it to your shell profile file (~/.bashrc, ~/.zshrc, etc.).

From source

1. Clone this repository


2. Install dependencies:

npm install


3. Install globally:

npm install -g .


4. Create a .env file in the root directory with your OpenAI API key:

OPENAI_API_KEY=your_openai_api_key_here




---

🔧 Usage

After installation, you can use the prompt command from anywhere:

prompt "just impeet one more logic, right now when you passe the weclome screen..."

The cleaned prompt will be automatically copied to your clipboard!

Input in any language is automatically translated to English:

prompt "Añadir función para enviar correos electrónicos"

CLI Flags

--model <name>: Override default model (defaults to gpt-4o)

--display, -d: Display the cleaned prompt in the terminal (default: false)

--version: Displays CLI version

--help: Displays usage instructions


Examples:

# Use a different model
prompt --model gpt-3.5-turbo "add a feature to send email notifications"

# Show the cleaned prompt in the terminal
prompt --display "improve the login screen"

# Translate from another language
prompt "Implementar autenticación de dos factores"


---

⚙️ Technical Design

Language: Node.js (ESM modules)

Dependencies:

openai (official SDK)

dotenv for config

commander for CLI arguments

clipboardy for clipboard integration


Cross-platform Support:

Works on Windows, macOS, Linux




---

⚠️ Troubleshooting

Issue	Solution

OpenAI API errors	Check your API key and quota limits
Missing API key	Set up your OpenAI API key as described in the installation section
Model input errors	Ensure you're using a valid OpenAI model name
Clipboard issues	Try using the --display flag to view the output in terminal



---

🌟 Example

Input (Spanish):

prompt "Añadir una función para enviar notificaciones por correo electrónico"

Output:

✅ Cleaned prompt copied to clipboard! (translated to English)

Clipboard content:

Add a function to send email notifications


---

📄 License

MIT License © Luka Löhr

Attribution Requirement: When using this software, the name "Luka Löhr" must be mentioned in the credits, documentation, or appropriate acknowledgement section of any derivative work.


---

🙏 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

