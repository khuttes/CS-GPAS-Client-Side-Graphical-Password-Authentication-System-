# CS-GPAS-Client-Side-Graphical-Password-Authentication-System-
Traditional passwords are weak and prone to attacks. This paper introduces a client-side Graphical Password Authentication System using HTML, CSS, and JavaScript. Users select a sequence of four images to log in. Data is stored in localStorage. The system boosts security with image randomization and no backend dependency.
![image alt](https://github.com/khuttes/CS-GPAS-Client-Side-Graphical-Password-Authentication-System-/blob/main/Screenshot%202025-08-02%20182859.png?raw=true)


Client-Side Graphical Password Authentication System: Design, Implementation, and Analysis.
Author:
Md. Hasib Islam
Department of Computer Science

Abstract
Traditional text-based authentication methods suffer from weak password habits and are increasingly vulnerable to phishing and brute-force attacks. This paper presents a lightweight, client-side Graphical Password Authentication System (GPAS) that leverages image sequences instead of alphanumeric input. Implemented with HTML, CSS, and vanilla JavaScript, the system allows users to register and authenticate using a selected sequence of four images from a randomized set. Data is stored using the browser’s localStorage API. This paper outlines the design, functionality, security implications, limitations, and potential improvements to the system.

1. Introduction
Passwords are the backbone of most authentication systems, but users often choose weak, easily guessable credentials. Graphical passwords provide an alternative that is more intuitive and potentially more secure. This project explores a web-based graphical password system built entirely on the front-end to demonstrate core functionality, ease of use, and implementation feasibility without server-side logic.

2. System Architecture
2.1 Frontend Technologies
•	HTML5 structures the interface.
•	CSS3 handles styling and responsiveness.
•	JavaScript manages application logic, state, user input, and local storage.
2.2 No Backend
The system operates without a server or database. All credentials and optional password hints are stored using the localStorage API, making it fast but limited to a single browser and device.

3. Key Features
3.1 Registration
Users select four distinct images from a set of 20. A password hint is optional. Selections are stored as a sequence of image IDs.
3.2 Authentication
To log in, users must select the exact same four images in the same order. A mismatch results in authentication failure. A correct match displays a success message.
3.3 Visual Feedback
•	Thumbnails show selected images.
•	Sequence dots fill as the user selects images.
•	Selected images pulse to indicate interaction.
3.4 Image Randomization
Each time the user switches tabs, the image grid reshuffles. This ensures users remember images, not positions.
3.5 Password Hint
A user-defined hint can be stored and is displayed on the login tab to aid memory.

4. Security Considerations
4.1 Strengths
•	Resistant to brute-force attacks due to image combinations.
•	Visual interaction adds usability for some users.
4.2 Weaknesses
•	No encryption: Passwords are stored in plaintext in localStorage.
•	No server: Data is limited to one user and one browser.
•	No session handling or expiration: Always accessible unless manually cleared.
•	No resistance to shoulder surfing or screen capture attacks.



5. Usability and Design
The system is designed to be:
•	Mobile-friendly
•	Accessible via mouse or touch
•	Easy to understand with guidance messages
•	Lightweight and fast-loading
The use of color-coded feedback, animation, and visual selection makes the system intuitive, even for non-technical users.

6. Limitations
•	Only one password can be stored at a time.
•	The system is not scalable for multi-user environments.
•	Lacks encryption or hashing mechanisms.
•	Vulnerable to local inspection (e.g., browser dev tools).
•	Not suitable for production without backend security enforcement.

7. Future Improvements
To enhance the system’s viability:
•	Add password hashing before storage
•	Integrate a secure backend (e.g., Node.js + MongoDB)
•	Support multiple user accounts
•	Add CAPTCHA or biometric fallback
•	Implement session handling and auto logout

8. Conclusion
This project demonstrates a functional and user-friendly graphical password system built entirely on the front-end. While it is not secure enough for production use, it highlights key concepts in alternative authentication methods and serves as a prototype for further development into a more secure and scalable solution.



References
1.	Dhamija, R., & Perrig, A. (2000). Deja Vu: A User Study Using Images for Authentication. In Proceedings of the 9th USENIX Security Symposium.
2.	Wiedenbeck, S., Waters, J., Birget, J. C., Brodskiy, A., & Memon, N. (2005). PassPoints: Design and longitudinal evaluation of a graphical password system. International Journal of Human-Computer Studies, 63(1), 102–127.
3.	Mozilla Developer Network (MDN) Docs - localStorage: https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage

