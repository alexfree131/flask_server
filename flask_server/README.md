
# Flask Application Setup and Run Instructions on Ubuntu with VSCode

This guide provides step-by-step commands to create and run a Flask application on Ubuntu using VSCode, including virtual environment activation and handling `requirements.txt`.

## 1. Install Python and pip (if not already installed)
```sh
sudo apt update
sudo apt install python3 python3-pip
```

## 2. Install Virtual Environment
```sh
sudo apt install python3-venv
```

## 3. Create Project and Navigate to Project Directory
```sh
mkdir my_flask_app
cd my_flask_app
```

## 4. Create Virtual Environment
```sh
python3 -m venv venv
```

## 5. Activate Virtual Environment
```sh
source venv/bin/activate
```

## 6. Create `requirements.txt` File
```sh
touch requirements.txt
```

## 7. Install Flask and Other Dependencies
- Open `requirements.txt` and add the necessary packages:
    ```txt
    flask
    ```
- Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## 8. Create Application File (e.g., `app.py`)
```sh
touch app.py
```

## 9. Edit `app.py` with a Simple Application Example
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(debug=True)
```

## 10. Run Flask Application
```sh
flask run
```
If `flask` is not recognized as a command, use:
```sh
python3 app.py
```

## 11. Open Project in VSCode
```sh
code .
```

## 12. Deactivate Virtual Environment (if needed)
```sh
deactivate
```

This cheat sheet will help you quickly set up and run a Flask application on Ubuntu using VSCode.
