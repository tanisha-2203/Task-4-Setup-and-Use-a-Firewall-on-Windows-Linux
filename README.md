# Task-4-Setup-and-Use-a-Firewall-on-Windows-Linux


sudo ufw status                # Check UFW status
sudo ufw enable                # Enable UFW if inactive ( "Firewall is active and enabled on system startup")
sudo ufw status verbose        # List current rules  (This command will show you the current rules and whether UFW is active.)
sudo ufw deny 23/tcp           # Block Telnet (This command tells UFW to block all incoming traffic on TCP port 23.)
telnet localhost 23            # Test the block rule  (This confirms the firewall blocked the request.)
sudo ufw allow 22/tcp          # Allow SSH 
sudo ufw delete deny 23/tcp    # Remove the block rule (Remove Test Rule (Telnet Block) ; No output means the rule was removed.)


Reset Firewall (Optional)
To revert all changes to default:  sudo ufw reset



Summary of How UFW Filters Traffic 
UFW filters network traffic based on rules you define. It can:
        Block or Allow Traffic: You can specify which ports to block or allow (e.g., blocking Telnet on port 23).
        Use Protocols: UFW can filter traffic based on protocols like TCP and UDP.
        Enhance Security: By configuring these rules, UFW helps protect your system from unauthorized access and potential threats.

   
