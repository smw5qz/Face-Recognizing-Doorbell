# Face-Recognizing-Doorbell
Raspberry Pi 4 camera detects known faces, sends a "[name] is at the door!" message to a smart speaker.   
*only works for Google Home at this time, user must add their device IP address  

Adapted from carolinedunn's project. See hers for installing and setting up the required software, including OpenCV.

This program creates a dictionary of known names, and alerts a smart speaker when one is detected, like a smart doorbell. Works for multiple known faces in the same frame. Will send another message when the face goes undetected for a set amount of time. The user controls this, is initialized to 8 seconds.

This time between detects, and detection event booleans are captured in an array in the dictionary values, keys being the users' names.
