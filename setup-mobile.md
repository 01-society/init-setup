# Install VS Code Environment in Termux (Using code-server)

This guide walks you through setting up a VS Code-like environment inside **Termux** using **code-server**, along with essential developer tools.

---

## 1. Install Termux (From F-Droid)

Google Play has an outdated version. Install the updated one from F-Droid:

1. Go to **F-Droid** website.
2. Search for **Termux**.
3. Download and install the latest APK.

[download it from hare](https://f-droid.org/repo/com.termux_1022.apk)

[download kiwi browser](https://github.com/kiwibrowser/src.next/releases/download/14310011181/com.kiwibrowser.browser-arm64-14310011181-github.apk)


---

## 2. Update & Upgrade Package List

After opening Termux, run:



```sh
pkg update -y
pkg upgrade -y
```

---

## 3. Install tur-repo (Termux User Repository)

Adds extra packages:

```sh
pkg install tur-repo
```

---

## 4. Install Essential Packages

We install code-server, vim, git, openssh, python, and nodejs.

```sh
pkg install code-server vim git openssh python nodejs -y
```

---

## 5. Start code-server

Run:

```sh
code-server
```



---

## 6. Change code-server Password

### Open the config file:

```sh
mkdir -p ~/.config/code-server
vim ~/.config/code-server/config.yaml
```

### Add this content:

```yaml
bind-addr: 0.0.0.0:8080
auth: password
password: your_new_password
cert: false
```

### Save and restart:

```sh
pkill code-server
code-server
```

---

## 7. Test Your Setup

Open browser and visit:

```
http://127.0.0.1:8080
```

Login using the password you set.

---

## 8. Done!

You now have a full VS Code-like environment running inside Termux with Python, Node.js, Git, SSH package installed (but no setup steps), and more. Test Your Setup
Open browser and visit:

```
http://127.0.0.1:8080
```

Login using the password you set.

---

## 9. Done!

You now have a full VS Code-like environment running inside Termux with Python, Node.js, Git, SSH, and more.
