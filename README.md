# elevate-day2-EC2
Create EC2 Instance
- Logged into [AWS Management Console](https://aws.amazon.com/console/).  
- Navigated to **EC2 → Instances → Launch Instance**.  
- Selected:
  - **AMI:** Ubuntu Server 22.04 LTS (Free Tier Eligible)
  - **Instance type:** `t2.micro`
  - **Key pair:** Created and downloaded `.pem` file
  - **Network settings:**
    - Allowed **HTTP (80)** and **HTTPS (443)**
    - Allowed **SSH (22)** from *My IP*

### 2️ Security Group Rules
| Type | Protocol | Port | Source | Description |
|------|-----------|------|---------|-------------|
| SSH | TCP | 22 | My IP | Secure remote access |
| HTTP | TCP | 80 | 0.0.0.0/0 | Allow web traffic |
| HTTPS | TCP | 443 | 0.0.0.0/0 | Allow secure traffic |

 **Outbound rule:** All traffic allowed (default).

---

##  SSH Connection

### Option 1: Browser-Based SSH
- Used **EC2 Instance Connect** → “Connect”  
- Opened a browser terminal session directly from AWS Console.

