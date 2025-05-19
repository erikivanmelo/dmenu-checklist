# Checklist Manager Bash Script

A minimalistic, interactive checklist manager for your terminal, built in Bash. This script uses `dmenu` for a graphical menu interface, allowing you to create, view, edit, and manage plain-text checklists directly from your command line.

## Features

- **Create and manage multiple checklists** in a dedicated folder (`$HOME/Documents/Notes/checklists` by default).
- **Add or remove items** interactively in each checklist.
- **Rename or delete checklists** via special menu entries.
- **Customizable appearance** via dmenu color and font options.
- **Fast and keyboard-driven** workflow for productivity.

## Prerequisites

- **Bash** (compatible with most Unix-like systems)
- **dmenu** (available on most Linux distributions)
- Optional: [Fira Code](https://github.com/tonsky/FiraCode) font for the default look (can be changed in `THEME` variable)

## Installation

1. **Install dependencies**  
   On Debian/Ubuntu:
   ```sh
   sudo apt-get install dmenu
   ```
   On Arch Linux:
   ```sh
   sudo pacman -S dmenu
   ```

2. **Clone this repository**  
   ```sh
   git clone https://github.com/yourusername/checklist-bash.git
   cd checklist-bash
   ```

3. **Make the script executable**  
   ```sh
   chmod +x checklist.sh
   ```

4. **(Optional) Install Fira Code font**  
   Download and install from [Fira Code GitHub](https://github.com/tonsky/FiraCode).

## Usage

Run the script with:
```sh
./checklist.sh
```

- **Main Menu:** Shows all available checklists. Select one to open, or type a new name to create a checklist.
- **Checklist Items:** Shows all items in the selected checklist. Type a new item to add it or select an existing one to remove it.
- **Special Operations:**  
  - To delete a checklist: Select or type the checklist name followed by ` --remove`.
  - To rename a checklist: Type in the format `oldname.txt --rename newname`.

## Customization

### Theme Configuration (`THEME` variable)

You can adjust the look and feel of the menu by changing the `THEME` variable at the top of the script.  
The default theme looks like this:

```bash
THEME=(-fn "Fira Code-12" -nb "#1d2021" -nf "#ebdbb2" -sb "#689d6a" -sf "#1d2021")
```

Here’s what each option does:

- `-fn "Fira Code-12"`  
  **Font:** Uses the "Fira Code" font, size 12, for the menu text.

- `-nb "#1d2021"`  
  **Normal Background:** Background color for unselected menu items (dark gray).

- `-nf "#ebdbb2"`  
  **Normal Foreground:** Text color for unselected menu items (beige/light).

- `-sb "#689d6a"`  
  **Selected Background:** Background color for the selected menu item (green).

- `-sf "#1d2021"`  
  **Selected Foreground:** Text color for the selected menu item (dark gray).

To modify the appearance, simply change the hex color codes or font in the `THEME` array. For example, to use a blue theme with a different font:

```bash
THEME=(-fn "JetBrains Mono-14" -nb "#282c34" -nf "#ffffff" -sb "#61afef" -sf "#282c34")
```

This changes the font, makes the background dark gray, text white, and the active selection blue.

## Demo Video

If you'd like to see the script in action, check out the following demo video:

https://github.com/user-attachments/assets/f2b0f153-6156-4c13-bd40-3003ed1492ba

