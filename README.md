# Task
Задача 4️⃣
Напишіть код, що генерує абсолютно випадкове число від 1 до 100… але без генератора випадкових чисел. Ви ж таке можете, чи не так? (yes, i can)

# Installation 💩 💩 💩 

## Prerequisites

- Python 3.6 or higher
- pip (usually comes with Python)
- Access to a terminal or command prompt

## Step 1: Clone the repository

Clone the repository from GitHub.

```bash
git clone https://github.com/vidnik/shitty-compt.git
```
Navigate to the `shitty-compt` directory.
```bash
cd shitty-compt
```

## Step 2: Create and activate a virtual environment

### On Windows:
```bash
python -m venv venv
venv\Scripts\activate
```
*I\'VE NEVER USED PYTHON ON WINDOWS SO JUST GOOGLED HOW TO DO THIS* 😅😅😅

### On macOS and Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

## Step 3: Install the required packages

```bash
pip install -r requirements.txt
```

## Step 4: Run the script

```bash
python shitty_random.py
```

## Notes

- Make sure your camera is connected and accessible. VERY IMPORTANT 🙏🙏🙏
- This script requires a working camera to generate the "random" number. If no camera is available, it will raise an error.

# How It Works

1. **Capture Video Frame**:
   - It initializes a video capture object with `cv2.VideoCapture(0)`, which accesses the default camera. 

2. **Check Camera Access**:
   - It checks if the camera is opened using `cam.isOpened()`. If the camera is not accessible, it raises an `IOError`.

3. **Process the Frame**:
   - If the camera is available, the current frame is read. The frame is encoded to JPEG format using `cv2.imencode()`, and its bytes are obtained.

4. **Get System Information**:
   - The script collects the current number of active processes (`len(psutil.pids())`) and the available memory (`psutil.virtual_memory().available`).

5. **Generate Hash**:
   - The combined byte data from the encoded frame and system information is encoded in base64. This data is then hashed using SHA-256. The first eight characters of the hexadecimal digest are converted to an integer.

6. **Generate Random Number**:
   - The generated integer is then transformed into a random number between 1 and 100 using the modulo operation: `n % 100 + 1`.

7. **Output**:
   ![example](https://github.com/user-attachments/assets/54baecab-a279-4137-89b9-a7a029f51690)

   


# Why it's sitty?
Bro, just take a look at the code.
