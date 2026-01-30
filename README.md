# About
Turn documentation into markdown files as context for coding agents to use.

# What it does
Users input a URL (e.g. a youtube video covering best practices or regular text documentation), which generates a markdown file where users can download it.

# Setup
run these commands first
```bash
git clone https://github.com/aaronamano/doccraft-ai
conda create -n doccraft-ai -y python=3.14
conda activate doccraft-ai
pip install -r requirements.txt
```
add a `.env` file under the root directory and insert
```text
OPENAI_API_KEY=your-api-key
FIRECRAWL_API_KEY=your-api-key
```

then run
```bash
python main.py
```

# Demo
**NOTE:** this video has been trimmed and edited. it doesn't show the response accurately in real time from inputting a url to downloading the markdown file

https://github.com/user-attachments/assets/5264228d-57f6-469f-ace6-c0237226fd25

