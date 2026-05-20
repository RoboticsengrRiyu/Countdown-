# Countdown-

import time

def countdown_timer(seconds):
    while seconds > 0:
        # Calculate minutes and remaining seconds
        mins, secs = divmod(seconds, 60)
        # Format as MM:SS with zero padding
        timer_format = f"{mins:02d}:{secs:02d}"
        
        # Print using \r to overwrite the line, and flush=True to force immediate display
        print(f"Time remaining: {timer_format}", end="\r", flush=True)
        
        time.sleep(1)
        seconds -= 1
        
    print("\nTime's up!      ")

# Example: Run a 5-minute countdown (300 seconds)
countdown_timer(300)
