
--- tag: package manger







### **1. Synchronize package databases**

```bash
sudo pacman -Sy         # Update package database only
sudo pacman -Syu        # Update package database and upgrade all packages
```

### **2. Install packages**

```bash
sudo pacman -S package_name          # Install a package
sudo pacman -S package1 package2     # Install multiple packages
sudo pacman -S --needed package_name # Skip reinstalling if already installed
```


### **3. Remove packages**

```bash
sudo pacman -R package_name          # Remove package
sudo pacman -Rs package_name         # Remove package + dependencies not needed by others
sudo pacman -Rns package_name        # Remove package + dependencies + config files
```


### **4. Search for packages**

```bash
pacman -Ss keyword                   # Search remote repositories
pacman -Qs keyword                   # Search installed packages
```


### **5. Query packages**

```bash
pacman -Si package_name               # Info about a package in repos
pacman -Qi package_name               # Info about an installed package
pacman -Ql package_name               # List files installed by package
pacman -Qdt                            # List orphaned packages
pacman -Qm                             # List packages not in official repos (AUR or manually installed)
```


### **6. Update and manage packages**

```bash
sudo pacman -Su                        # Upgrade all packages
sudo pacman -Sc                        # Clean old package cache (keep current version)
sudo pacman -Scc                       # Clean entire package cache
```


### **7. Manage package groups**

```bash
sudo pacman -S group_name              # Install a group of packages
sudo pacman -Qg                         # List all groups
```


### **8. Verify package integrity**

```bash
pacman -Qkk package_name               # Verify installed package files against database
```


### **9. Miscellaneous**

```bash
pacman -Q                                # List all installed packages
pacman -Qe                               # List explicitly installed packages
pacman -Qn                               # List packages installed from official repos
```


