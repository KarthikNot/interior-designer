# <center> AI Interior Designer <center>

# READ THE LICENSE AND USE THIS PROJECT.

## How to Set Up This Project 🛠️

This guide walks you through setting up the project's environment.

**<u>1. Install Python </u>🐍**

If you don't have Python installed yet, head over to the official download page: [Python Download Guide](https://wiki.python.org/moin/BeginnersGuide/Download) and follow the instructions for your operating system (Windows, macOS, or Linux).

**<u>2. Creating a Virtual Environment</u>**

1. Install virtualenv (if not already installed):

   - If you haven't installed virtualenv, you can do so using pip:

   ```bash
   pip install virtualenv
   ```

2. Create a virtual environment:

   - In the terminal and run this command:

   ```bash
   virtualenv venv
   ```

3. Activate the virtual environment:

   - To activate the virtual environment:

   ```bash
   venv\Scripts\activate
   ```

**3. Clone the Repo 📥**

1. Open your Git client or terminal.
2. Navigate to the directory where you want to clone the repository.
3. Run the following command, replacing `<repository_url>` with the actual URL of the project's repository:

```bash
git clone <repository_url>
```

**3. Install required Dependencies 📦**

1. Open terminal/cmd.
2. Navigate to repo directory
3. Run the following command to install dependencies from requirements.txt:

```bash
pip install -r requirements.txt
```

**4. Add the Together.ai API KEY 📦**

1. Create a .env file.
2. add a env variable "TOGETHER_API_KEY" in the .env file.  
   Example of a sample API KEY

```bash
TOGETHER_API_KEY = "<API_KEY>"
```

**4. Host the project Locally 🌐**

- After installing the required dependencies, run the following command to start the project locally:

```bash
streamlit run ./src/server.py
```
