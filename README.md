# PIA OpenVPN Configuration Files

Copy all files to `/etc/openvpn/`:

`sudo cp * /etc/openvpn/`

Create `account.txt` for autologin:

`sudo touch /etc/openvpn/account.txt`

Add username and password to `account.txt`:

```sh
echo 'username' >> /etc/openvpn/account.txt
echo 'password' >> /etc/openvpn/account.txt
```

Secure `account.txt`:

```sh
sudo chown root:root /etc/openvpn/account.txt
sudo chmod 0600 /etc/openvpn/account.txt
```

Active openvpn with server Japan:

`sudo systemctl start openvpn@Japan.server`

Use PIA DNS: open `/etc/resolv.conf` and add:

```sh
nameserver 209.222.18.222
nameserver 209.222.18.218
```
