Before you can securely connect your computer to GitHub without typing your username and password every time, you need to set up an **SSH key**.

An SSH key is a secure authentication method that allows Git to communicate with GitHub using encrypted credentials. It’s like giving your computer a digital ID card that GitHub trusts.

Follow these steps to generate, configure, and test your SSH key.

---
## Prerequisites

- Git must be installed on your computer.
    
- A GitHub account.

## Check for Existing SSH Keys

Look for files like `id_rsa.pub` or `id_ed25519.pub`. If they exist, you might already have an SSH key.
```
ls -al ~/.ssh
```

---
## 1. Generate a New SSH Key

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
- Replace `"your_email@example.com"` with your GitHub email.
    
- If your system doesn’t support `ed25519`, use:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

## 2. Save the Key

You'll be prompted to choose a file to save the key:
```
Enter a file in which to save the key (/home/you/.ssh/id_ed25519):
```
Press **Enter** to accept the default location.

## 3. Add the SSH Key to the SSH Agent

Start the agent:
```
eval "$(ssh-agent -s)"
```

Add your key:
```
ssh-add ~/.ssh/id_ed25519
```

## 4. Copy the Public Key

```
cat ~/.ssh/id_ed25519.pub
```

Copy the output to your clipboard. Or use:

- macOS: `pbcopy < ~/.ssh/id_ed25519.pub`
    
- Linux: `xclip -sel clip < ~/.ssh/id_ed25519.pub`
    
- Windows (Git Bash): `clip < ~/.ssh/id_ed25519.pub`

## 5. Add the Key to GitHub

1. Go to GitHub SSH Settings
    
2. Click **New SSH key**
    
3. Paste your key into the field
    
4.  Click **Add SSH key**

## 6. Test the Connection

```
ssh -T git@github.com
```

If successful, you’ll see:

```
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```