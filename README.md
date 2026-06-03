# Honeypot-Lab

## Objective

Deploy and operate a DShield honeypot by Sans Internet Storm Center (ISC) on an AWS EC2 instance to collect, analyze, and report real-world malicious scanning and attack activity. The honeypot is designed to emulate vulnerable services, capture attacker behavior, contribute threat intelligence to the SANS Internet Storm Center, and provide hands-on experience with honeypot deployment, monitoring, and log analysis.

### Skills Learned

- Deployed and configured a DShield honeypot on an AWS EC2 instance.
- Configured AWS networking components, including Security Groups and Elastic IPs.
- Implemented and validated port forwarding and firewall rules using iptables.
- Monitored and analyzed real-world internet scanning and attack activity.
- Investigated web and SSH honeypot logs to identify reconnaissance and exploitation attempts.
- Troubleshot network connectivity, NAT, and public service exposure issues.
- Managed Linux services, processes, and remote administration through SSH.
- Gained experience with threat intelligence collection and reporting through the SANS Internet Storm Center (ISC).
- Practiced cloud security monitoring and honeypot operations in a production-like environment.

### Tools Used

- Amazon Web Services (AWS) EC2
- Ubuntu
- DShield Honeypot
- SANS Internet Storm Center (ISC)
- Elastic IP
- AWS Security Groups
- iptables
- OpenSSH
- Linux Command Line (Bash)
- Cowrie SSH Honeypot
- Python 3

## Steps

1. Created an AWS EC2 t3.micro instance running Ubuntu Server 26.04 LTS.
   <img width="1510" height="90" alt="image" src="https://github.com/user-attachments/assets/299c01fd-520b-4dfd-9da3-e5f099f32a9a" />
   *Ref 1: AWS EC2 Instance Overview.*
   This screenshot shows the AWS EC2 instance hosting the DShield honeypot. The instance is running Ubuntu 26.04 LTS on a t3.micro instance and is assigned a public Elastic IP address for internet accessibility.

2. Assigned an Elastic IP address to provide a stable public endpoint.
   <img width="1429" height="80" alt="image" src="https://github.com/user-attachments/assets/4c172362-7c43-470b-8e1e-1e287e8f3f14" />
   *Ref 2: Elastic IP Assignment.*
   This screenshot shows the Elastic IP address associated with the EC2 instance. The Elastic IP provides a stable public endpoint that allows internet traffic to consistently reach the honeypot.

3. Connected to the EC2 instance using SSH and verified system configuration with a installed and configured the DShield Honeypot software.  
   <img width="782" height="782" alt="image" src="https://github.com/user-attachments/assets/d2d21778-2e2c-40c9-8f47-ef9aa9b1ef06" />  
   *Ref 3: SSH Access to EC2 with DShield Honeypot Installed.*
   This screenshot demonstrates a successful SSH connection to the EC2 instance and verifies that the operating system is accessible for administration and configuration with DShield honeypot installed and confirms that the software was successfully deployed on the Ubuntu server.

4. Configured AWS Security Groups to allow required traffic for the honeypot and administrative access.
   <img width="1643" height="788" alt="image" src="https://github.com/user-attachments/assets/406b42c6-b9c3-4723-a80b-50b77b73533a" />
   *Ref 4: AWS Security Group Configuration.*
   This screenshot displays the inbound security group rules configured to allow honeypot traffic while restricting administrative access to trusted sources.

5. Verified DShield services were running and listening.
   <img width="782" height="678" alt="image" src="https://github.com/user-attachments/assets/6433085e-4c1d-4c4b-bc85-1024caf35839" />  
   *Ref 5: DShield Service Verification.*
   This screenshot shows the DShield status.sh output and confirms that the honeypot services are running and listening on the expected ports.

7. Confirmed web honeypot exposure by accessing the public IP from an external network.
   <img width="1912" height="985" alt="image" src="https://github.com/user-attachments/assets/de74c8ed-9fdf-4730-ae9b-33f183793f1b" />
   *Ref 6: External Web Honeypot Test.*
   This screenshot demonstrates successful access to the web honeypot from an external network, confirming that the service is publicly reachable.
   
8. Validated SSH honeypot redirection and service availability.
   <img width="782" height="39" alt="image" src="https://github.com/user-attachments/assets/dc025e5d-1224-4d84-aa6e-bd15c7b73c6f"  />  
   *Ref 7: SSH Honeypot Port Redirection.*
   This screenshot shows the firewall or NAT configuration used to redirect public SSH traffic to the SSH honeypot services, validating proper honeypot exposure.

10. Monitored honeypot logs and verified collection of real-world scanning activity which confirmed successful operation of the honeypot.
   <img width="1161" height="797" alt="image" src="https://github.com/user-attachments/assets/092999e9-10fd-42d2-b4f0-4b9ff7894550" />
   *Ref 8: Honeypot Log Collection.*
   This screenshot displays captured honeypot logs containing real-world reconnaissance and scanning activity from external hosts, demonstrating successful detection and logging of malicious or suspicious network activity.

## References

SANS Internet Storm Center (ISC), "DShield Honeypot Project." Available:
https://isc.sans.edu/honeypot.html

Amazon Web Services (AWS), "Amazon EC2 Documentation." Available:
https://docs.aws.amazon.com/ec2/

Amazon Web Services (AWS), "Amazon VPC Documentation." Available:
https://docs.aws.amazon.com/vpc/
