# Oh My Posh Installation Guide for WSL2

This guide provides step-by-step instructions to install and configure **Oh My Posh** in WSL2.

## Step 1: Install Oh My Posh
Download and install Oh My Posh using the official script:

```sh
curl -s https://ohmyposh.dev/install.sh | bash
```

This installs **Oh My Posh** in `~/.local/bin/oh-my-posh`.

---

## Step 2: Add Oh My Posh to PATH
Since it is installed in `~/.local/bin`, we need to ensure it is in the system `PATH`.

Run this command to add `~/.local/bin` to your PATH:

```sh
echo 'export PATH=$HOME/.local/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

If you are using `zsh`, run:

```sh
echo 'export PATH=$HOME/.local/bin:$PATH' >> ~/.zshrc
source ~/.zshrc
```

---

## Step 3: Verify Installation
Check if Oh My Posh is now accessible:

```sh
oh-my-posh --version
```

If you see a version number, the installation was successful!

---

## Step 4: Configure Oh My Posh to Load Automatically
To enable Oh My Posh in your terminal, add the following line to the end of `~/.bashrc` (or `~/.zshrc` if you use `zsh`):

```sh
echo 'eval "$(oh-my-posh init bash)"' >> ~/.bashrc
source ~/.bashrc
```

For `zsh` users:

```sh
echo 'eval "$(oh-my-posh init zsh)"' >> ~/.zshrc
source ~/.zshrc
```

---

## Step 5: Apply a Theme
Oh My Posh comes with different themes. You can apply one by running:

```sh
oh-my-posh font install  # Install recommended fonts (optional)
oh-my-posh init bash --config ~/.poshthemes/atomic.omp.json
```

To make the theme persistent, add the following to `~/.bashrc`:

```sh
echo 'eval "$(oh-my-posh init bash --config ~/.poshthemes/atomic.omp.json)"' >> ~/.bashrc
source ~/.bashrc
```

---

## Step 6: Restart Your Terminal
Close and reopen your terminal, or run:

```sh
exec bash
```

For `zsh` users:

```sh
exec zsh
```

---

## Step 7: Enjoy Your New Prompt! 🎨
Your terminal should now have a **custom Oh My Posh prompt**! 🚀
