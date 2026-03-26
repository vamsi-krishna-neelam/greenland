# GreenLand: Tamper-Proof Land Registration

A Django-based land registration system that combines:
- Ethereum smart contract storage (Web3)
- IPFS file storage
- ML-based fraud detection for transaction data

## Tech Stack

- Python 3.7.6
- Django 2.1.7
- Web3.py 4.7.2
- IPFS API 0.2.3
- LightGBM, Keras, TensorFlow 1.14

## Project Structure

- Land/: Django project settings and root URLs
- LandApp/: Main app (views, templates, static files)
- Dataset/: Training dataset
- model/: Saved model artifacts
- hello-eth/: Solidity contract artifacts and related files

## Prerequisites

Install and run the following before starting the web app:

1. Python virtual environment with dependencies
2. Ethereum local node on http://127.0.0.1:9545 (for Web3 contract calls)
3. IPFS daemon on local machine

## Setup

1. Create and activate virtual environment (if not already active)
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Apply migrations:

```bash
python manage.py migrate
```

## Run the Application

1. Start IPFS:

```bash
Start_IPFS.bat
```

or manually:

```bash
ipfs init
ipfs daemon
```

2. Ensure your Ethereum/Ganache node is running at:

```text
http://127.0.0.1:9545
```

3. Start Django server:

```bash
python manage.py runserver
```

4. Open in browser:

- http://127.0.0.1:8000/index.html

## Notes

- If Ethereum node is not running, contract-related operations will fail.
- If IPFS daemon is not running, file upload and hash storage will fail.
- This project is pinned to older package versions; Python 3.7 is recommended for compatibility.

## Helper Scripts

- runWebServer.bat: Runs Django development server
- runJupyter.bat: Starts Jupyter notebook
- Start_IPFS.bat: Initializes and starts IPFS daemon

## License

For academic/demo usage unless a separate license is specified.
