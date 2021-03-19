# Face-Recognizing-Doorbell
Raspberry Pi 4 camera detects known faces, sends a "[name] is at the door!" message to a smart speaker.   
*only works for Google Home at this time, user must add their device IP address  

Adapted from carolinedunn's project. See hers for installing and setting up the required software, including OpenCV.

Headshots are taken for each person's face, and trained on before using them for live detection.

This program creates a dictionary of known names, and alerts a Google Home smart speaker when one is detected, like a smart doorbell. Works for multiple known faces in the same frame.

The main problem that had to be solved was limiting the frequency the alert is sent, but allowing it to continue like when you press a doorbell again. I solved this by implementing an array of [detect1 (true/false), detect2 (true/false), timebetween1&2 (seconds)] as the value for each item in the dictionary.  
