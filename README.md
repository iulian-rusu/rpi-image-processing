# IoT Image Processing
A server that runs on a Raspbery Pi and uses a connected camera to track movements.
The tracked points are used to create a live drawing and stream it to a client connected with a web browser.
The server can also send an email with the drawing on client demand.

Technologies used:
* `Flask` for designing the web application
* HTML/CSS/JS on the client side
* `RPi.GPIO` for communicating with RPi ports
* `OpenCV` for image processing
* `PIL` for drawing the images
* `smtplib` for sending emails
* `socket` for communication between processes

The project contains one main script and 3 separate micro-applications ("microservices"):
1. `app.py` - the main process that runs the `Flask` server
2. `camera.py` - started on client demand to record the camera
3. `led.py` - started to turn on/off leds
4. `email_sender.py` - started to send emails with the drawing