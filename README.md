# PIA OpenVPN Configuration Files

Copy all files to `/etc/openvpn/`:

`
sudo cp * /etc/openvpn/
`

Create `account.txt` for autologin:

`
sudo touch /etc/openvpn/account.txt
`

Add username and password to `account.txt`:

`
echo 'username' >> /etc/openvpn/account.txt

echo 'password' >> /etc/openvpn/account.txt
`

Secure `account.txt`:

`
sudo chown root:root /etc/openvpn/account.txt

sudo chmod 0600 /etc/openvpn/account.txt
`

Active openvpn with server Japan:

`
sudo systemctl start openvpn@Japan.server
`
