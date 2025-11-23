EX01 Developing a Simple Webserver
AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

DESIGN STEPS:
Step 1:
HTML content creation.

Step 2:
Design of webserver workflow.

Step 3:
Implementation using Python code.

Step 4:
Import the necessary modules.

Step 5:
Define a custom request handler.

Step 6:
Start an HTTP server on a specific port.

Step 7:
Run the Python script to serve web pages.

Step 8:
Serve the HTML pages.

Step 9:
Start the server script and check for errors.

Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

PROGRAM:
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''

<title> My Laptop</title>
TCP/IP Protocol Suite
TCP/IP Layer	Key Protocols
Application Layer	HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS, DHCP, TELNET, SNMP
Transport Layer	TCP, UDP, SCTP
Internet Layer	IP (IPv4, IPv6), ICMP, ARP, IGMP
Network Access Layer	Ethernet, Wi-Fi (IEEE 802.11), PPP, Frame Relay, DSL
'''
class MyServer(BaseHTTPRequestHandler): def do_GET(self): print("Get request received...") self.send_response(200) self.send_header("content-type", "text/html")
self.end_headers() self.wfile.write(content.encode())

print("This is my webserver") server_address =('',8000) httpd = HTTPServer(server_address,MyServer) httpd.serve_forever()

OUTPUT:
<img width="1048" height="524" alt="image" src="https://github.com/user-attachments/assets/bd16f32b-8a89-47bd-92c4-e4c107a79a94" />
<img width="1043" height="616" alt="image" src="https://github.com/user-attachments/assets/ad038c1c-16f9-4b4e-b593-ccad78e543a6" />


RESULT:
The program for implementing simple webserver is executed successfully.
