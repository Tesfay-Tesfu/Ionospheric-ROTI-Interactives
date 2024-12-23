# TEC-ROTI Interactive Processing Tool
## Overview
This tool processes Total Electron Content (TEC) and calculates the Rate of TEC Index (ROTI) using data from both disturbed days and quiet days. It provides an interactive interface, allowing users to select elevation angles and upload TEC data folders for comparison. The output includes ROTI values computed for 30-second and 5-minute intervals.

This project leverages the GOPI (GPS-TEC Processing Software) for preprocessing TEC data, ensuring accurate and reliable ionospheric data analysis.


## TEC-ROTI Interactive Processing
### Overview
This tool processes Total Electron Content (TEC) and calculates the Rate of TEC Index (ROTI) using data from both disturbed days and quiet days. It provides an interactive interface, allowing users to select elevation angles and upload TEC data folders for comparison. The output includes ROTI values computed for 30-second and 5-minute intervals.

This project leverages the GOPI (GPS-TEC Processing Software) for preprocessing TEC data, ensuring accurate and reliable ionospheric data analysis.

## TEC and ROTI Calculations

### Rate of TEC (ROT):
ROT = (VTECₙ - VTECₙ₋₁) / (tₙ - tₙ₋₁)

Where:
- **VTECₙ**: Vertical TEC at time *tₙ*
- **VTECₙ₋₁**: Vertical TEC at time *tₙ₋₁*

### Rate of TEC Index (ROTI):
ROTI = √(⟨ROT²⟩ - ⟨ROT⟩²)

Where:
- ⟨ROT²⟩: Mean square of ROT over a specific interval
- ⟨ROT⟩: Mean ROT over the same interval

ROTI is a valuable metric for identifying ionospheric irregularities, especially during geomagnetic storms or solar flares.


## Prerequisites
Before running the code, ensure the following Python libraries are installed and available on your machine:

### File handling and operations
import os
import glob

### Data manipulation
import pandas as pd
import numpy as np

### GUI for file selection
import tkinter as tk
from tkinter import filedialog
from tkinter import simpledialog

### Jupyter Notebook widgets
import ipywidgets as widgets
from IPython.display import display

### Security and encryption
from cryptography.hazmat.primitives.kdf.pbkdf2 import PBKDF2HMAC
from cryptography.hazmat.backends import default_backend
from cryptography.hazmat.primitives import hashes
from cryptography.fernet import Fernet
import base64

#### Ensure you are using Python 3.7 or higher.
If tkinter is not available, you may need to install it separately (e.g., via your system package manager).

## Collaboration
We are open to collaborating with researchers and developers who want to utilize or contribute to this tool. For any inquiries, feel free to contact us at:

Email: tesfayphysics@gmail.com
