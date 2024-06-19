EC2 Dashboard Project
This project hosts a dashboard application on an EC2 instance using Python and Panel.

Features
Real-time data visualization
Interactive dashboard interface
WebSocket support for live updates
Installation
To install and run the dashboard on your EC2 instance, follow these steps:

SSH into your EC2 instance:

bash
Copy code
ssh -i your-key.pem ec2-user@ec2-instance-public-ip
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/ec2-dashboard.git
cd ec2-dashboard
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the dashboard:

bash
Copy code
tmux new -s dashboard-session
panel serve dashboard.py --port 5006 --address 0.0.0.0 --allow-websocket-origin=*
Press Ctrl + B, then release both keys and press D to detach from the tmux session.

Access the dashboard:
Open a web browser and go to http://ec2-instance-public-ip:5006 to view the dashboard.

Usage
Navigate through different tabs and interact with visualizations.
Customize settings and filters as needed.
Configuration
Modify config.py to adjust application settings.
Ensure proper firewall settings to allow traffic on port 5006.
Contributing
Contributions are welcome! Please follow these guidelines:

Fork the repository and create your branch (git checkout -b feature/your-feature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/your-feature).
Create a new Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.
