# kavya-projects-report
Project Report: Banoth Kavya
B.Tech ECE (Industrial IoT), NIT Kurukshetra | github.com/kavyabanoth

1. Real-Time Sleep/Drowsiness Detection with Arduino Alerts
Type: IoT course project (team of 3) | Stack: Python, OpenCV, pyserial, Arduino, L298N driver Problem: Drowsiness of drivers and machine operators causes accidents; a low-cost real-time alert system is needed. Approach:

Python and OpenCV capture webcam video and detect the face and eyes with Haar cascades.
The eye-open/closed state is sent over serial (9600 baud) to an Arduino.
The Arduino drives a buzzer, red/green LEDs and a DC motor (through an L298N driver) as alerts. Results: Worked in real time on a basic laptop without a GPU; serial communication was stable. Detection depended on lighting and face angle. Future work: Add Eye Aspect Ratio with a consecutive-frame counter to reduce blink false alarms; add extra sensors or a cloud dashboard. Proof: Project report PDF in drowsiness/, code, wiring photo.

2. Real-Time Object Tracking in C++
Stack: C++, OpenCV (CSRT/KCF trackers), CMake, gdb Problem: Track a selected object in live video and show its status in real time. Approach:

Capture webcam or video with OpenCV in C++.
The user selects the target with an interactive ROI box.
A CSRT/KCF tracker follows it, drawing the box live with FPS and tracking status on screen.
Built with CMake and debugged with gdb. Test procedure: [add your steps, e.g. run with a webcam, select the object, move it, check status and FPS]. Results: [add your real FPS and what you observed]. Proof: Code, README and screen recording/screenshots in cpp-tracker/.

3. AgentHire AI: Multi-Agent Job Application Platform
Stack: Python, LangGraph, ChromaDB, Groq/Llama, Streamlit Problem: Tailoring a resume and application for each job is slow and error-prone. Approach:

A 7-node LangGraph workflow coordinates 6 agents: parsing, retrieval, matching, tailoring, ATS optimization and cover letter.
Match scoring combines keyword and embedding similarity.
Outputs are grounded in the candidate's real experience, with no fabricated content. 
Links: Code: https://github.com/kavyabanoth/AgentHire | Live demo: [add Streamlit link] Proof: Screenshots in agenthire/.
