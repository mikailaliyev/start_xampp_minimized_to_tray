import subprocess
import time
import pygetwindow as gw

def start_xampp(xampp_path):
    try:
        # Start XAMPP
        subprocess.Popen([xampp_path])
        return True
    except Exception as e:
        print(f"Error starting XAMPP: {e}")
        return False

def close_xampp_window(window_title):
    try:
        # Wait for XAMPP window to appear
        xampp_window = None
        while not xampp_window:
            xampp_window = gw.getWindowsWithTitle(window_title)
            time.sleep(1)
        
        # Close XAMPP window
        xampp_window[0].close()
        
        return True
    except Exception as e:
        print(f"Error closing XAMPP window: {e}")
        return False

if __name__ == "__main__":
    xampp_path = r"C:\xampp\xampp-control.exe"  # Path to xampp-control.exe or equivalent
    window_title = "XAMPP Control Panel"  # Title of the XAMPP window

    # Start XAMPP
    if start_xampp(xampp_path):
        print("XAMPP started successfully.")
        
        # Close XAMPP window
        if close_xampp_window(window_title):
            print("XAMPP window closed.")
        else:
            print("Failed to close XAMPP window.")
    else:
        print("Failed to start XAMPP.")
