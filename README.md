
ngrok config add-authtoken 35KAMdzOLABSjjpJVRoUJC9tIJD_3DVSf2bWuKxKojeEyrGHn

# Install
wget https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64
chmod +x cloudflared-linux-amd64
sudo mv cloudflared-linux-amd64 /usr/local/bin/cloudflared

# Setup tunnel
cloudflared tunnel login
cloudflared tunnel create kali-rdp
cloudflared tunnel run kali-rdp --url tcp://localhost:3389
