#  TikOsint — TikTok OSINT Metadata Recon Toolkit

**TikOsint** is an educational OSINT (Open Source Intelligence) tool that scrapes publicly available TikTok user metadata **directly from profile pages** using the hydration payload embedded in the HTML.

>  No login  
>  No API keys  
>  No browser automation  
>  Terminal-only recon

---

##  Why Use TikOsint?

-  Perform TikTok recon and passive footprinting  
-  Collect metadata for bug bounty reports  
-  Analyze privacy exposure of public and private profiles  
-  Explore fingerprinting vectors using `secUid`, `region`, etc.  
-  No TikTok developer account required

---

## Features

| Feature               | Description                                   |
|----------------------|-----------------------------------------------|
|  **Username**            | From profile URL or direct input             |
|  **Display Name**        | TikTok screen name                          |
|  **Bio**                | User’s bio field                            |
|  **Avatar URL**         | Direct image link                           |
|  **Verified**          | Shows if user is verified                    |
|  **Private Account**   | True/False from backend                      |
|  **Followers**           | Number of followers                         |
|  **Following**           | Number of accounts followed                 |
|  **Likes**              | Total likes                                 |
|  **Video Count**         | Total published videos                      |
|  **Region**              | Country code (from hydration JSON)          |
|  **Account Created**     | UTC timestamp of signup                     |
|  **secUid**              | Persistent backend identifier               |
|  **openId / unionId**    | Exposed internal IDs (if present)           |
|  **Profile Deep Link**   | Backend deep link URL                       |
|  **Privacy Flags**       | Includes `secret`, `openFavorite`, etc.     |
|  **Linked Accounts**     | Instagram, YouTube, Twitter, Discord, Email |

>  **Includes support for detecting leaks on _private_ profiles** — critical for recon and bug bounty analysis.

---

##  Installation (Linux)

```bash
git clone https://github.com/cybermoro/TikOsint.git
cd TikOsint
sudo apt update && sudo apt install python3 python3-pip -y
pip3 install -r requirements.txt
python3 TikOsint.py
```

## Usage:
```Python
python3 TikOsint.py
```
## Then:
```Python
[?] Enter TikTok username: 
```
## Output:
```
Username: user
Region: US
Account Created: 2024-07-08 00:37:28 UTC
secUid: MS4wLjABAAAAkqxwqPk...
Privacy Flags:
  secret: True
  openFavorite: False
  showFavoriteList: None
```
##  Dependencies :

- Python 3.x

- requests

- beautifulsoup4

- pystyle

- colorama

## Install requirements :
```
pip3 install -r requirements.txt
```
## Disclaimer :
This project is for educational and ethical hacking purposes only.

Use TikOsint only on targets you are authorized to test — such as for bug bounty programs that allow TikTok recon.
