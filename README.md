Requirements

Windows PC with Python 3.8+
MikroTik router running RouterOS 7 with the API service enabled
Network access between the PC and the router


Installation
1. Clone the repository

git clone https://github.com/yourusername/mikrotik-voucher-manager.git
cd mikrotik-voucher-manager
2. Install dependencies
pip install flask routeros-api

Configure your router connection
Open app.py and update these three lines:

MIKROTIK_HOST = "192.168.88.1"   # your router's IP address
MIKROTIK_USER = "admin"           # RouterOS API username
MIKROTIK_PASS = ""                # RouterOS API password

4. Enable the API service on your MikroTik
In Winbox go to: IP → Services → api and make sure it is enabled on port 8728.

5. Add your logo
Place your logo file named tana.png in the root project folder. 
It will appear in the header and on printed voucher cards. 
Rename the reference in app.py and the templates if your file is named differently.

6. Run the app
bashpython app.py

Or on Windows just double-click start.bat. The browser opens automatically at http://127.0.0.1:5000.
Project Structure

mikrotik-voucher-manager/
├── app.py              # Flask app + MikroTik API integration
├── start.bat           # One-click launcher for Windows
├── tana.png            # Your logo (replace with your own)
├── requirements.txt
└── templates/
    ├── index.html      # Main dashboard
    └── print.html      # Printable voucher cards

Built With

Python + Flask
routeros-api — Python client for the MikroTik RouterOS API

Contributing
Pull requests are welcome. If you're a network engineer or IT consultant deploying MikroTik hotspots and want to extend this — better profile management, usage reporting, multi-router support — open an issue or submit a PR.

License
UNIVERSITY OF NAIROBI — free to use, adapt and deploy.
