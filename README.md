# ETHstorage Guide
Complete guide for those who want to contribute for the ETH storage ceremony

For doing this, need a VPS and a Github Account 

Github requirements
- 1 month old
- atleast 1 follower
- atleast 5 following
- atleast have 1 public repository

### Deadline 22nd August 2025 

# STEP 1 - GETTING A VPS
Getting a VPS with less than 1 or 2$ is enough 
 - Go to [xorek.cloud](https://xorek.cloud) and sign up with Google
 - Go to **Payments** tab under **Billing**
 - Enter the payable amount (ex: 1.5$ or 2$.. depending on the VPS you choose)
 - Select payment method as **CryptoCurrency/Heleket** and click **Pay**
 - Proceed with the payment by sending USDT to the given address ☑️

 - Go back to **Virtual Private Servers** under **Products/Services** tab
 - Select a VPS (0.39$/day ,I chose DE-R9-2) and then **order**. (If possible, Choose higher specs for a faster contribution)
 - Select **Ubuntu 22.04** and **Pay**
 - Select **Personal Account** and then **Place an rder** ☑️

 - Go back to **Virtual Private Servers** and select your VPS name (Takes some minutes to show up)
 - Click on the icon **To Panel**
 - Change the password by clicking the 3 dots (Dont forget this password!)

#### IP address of our VPS is shown there. Need it to run the VPS


# STEP 2 - RUNNING THE VPS  

Now we’re going to set up the VPS from our local PC. Once it’s running, the process will continue on the VPS even if your PC is turned off

This is the main advantage of using a VPS

For contributing to the ETHStorage ceremony, you need to keep the terminal process on the VPS **running** while you are in the queue 

Since the VPS is hosted in the cloud, it will stay active even if you shut down your own PC ✅

- Press **Windows Key + R**, type **powershell**, and hit **Enter** to open PowerShell.
### Now copy and paste these commands one-by-one

## Connect your VPS
  ```bash
  ssh root@<your vps IP address>
  ```

## Update and install the dependencies
```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt install -y curl git build-essential
```

## Installing Node.js
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```
```bash
sudo apt install -y nodejs
```
```bash
sudo npm install -g npm@9.2
```

## Create temporary directory
```bash
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp
```

## Install Phase2 Cli
```bash
sudo npm install -g @p0tion/phase2cli
```

## Authenticate with GITHUB
```bash
phase2cli auth
```

- Copy the link shown in your terminal or click on [github.com/login/device](https://github.com/login/device)
- Authorise your github account by the **auth code** shown in your powershell
- Go back to your powershell

## Contributing to the ceremony
```bash
screen -S ceremony
```
```bash
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

- Choose **randomly** on the prompt came

## Final Steps
- Now wait for your queue
- When your turn comes the tool will automatically process your contribution
- Now.. You have successfully contributed to the ETHstorage V1 Trusted Setup Ceremony ✅
### If the queue is showing for so many days.. dont worry.. it would still get contributed before 22nd August

## Screen Session Controls
- Press **Ctrl A + D**  (Screen detaches)

Now you can safely close the powershell and let the queue run in your VPS safely. You can even turn off your WIFI and PC.
  
- For re-attaching screen (open your powershell and type these commands)
  ```bash
  ssh root@<your vps IP address>
  ```
  ```bash
  screen -r ceremony
  ```

# After successfull contribution remove the login permissions
```bash
  phase2cli clean
```
```bash
  phase2cli logout
```
```bash
  cd ~ && rm -rf ~/trusted-setup-tmp
```

### Drop a follow and star in my repository 😄
X Profile - [cryptoSid1564](https://x.com/cryptoSid1564)
  
  
  
  

  
  



