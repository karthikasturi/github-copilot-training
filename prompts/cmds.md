
## Environment Switching Commands

### Switch to Older Environment (Python 3.5.15)
```bash
deactivate
pyenv global 3.5.15
source venv/bin/activate
```

### Switch to New Environment (Python 3.12.1)
```bash
deactivate
pyenv global 3.12.1
source venv-new/bin/activate
```

### Install Dependencies
```bash
pip install -r app-migration/requirements/modern.txt
```
