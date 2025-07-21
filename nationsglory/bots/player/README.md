# Player Bot for NationsGlory

This module provides a bot for automating player actions in Minecraft on NationsGlory servers.

## Features

### Basic Controls
- **Movement**: Move forward, backward, left, or right
- **Actions**: Jump, sneak, use/interact, attack
- **Inventory**: Open inventory
- **Chat**: Send messages in the game chat

### Automated Tasks
- **Anti-AFK**: Prevents being kicked for inactivity by performing random movements
- **Discord Chat Integration**: Connects game chat with Discord (placeholder functionality)
- **Auto Farm**: Automatically farms crops by moving forward and breaking blocks
- **Auto Mine**: Automatically mines by breaking blocks and moving forward
- **Auto Fish**: Automatically fishes by casting and reeling in the fishing rod

## Usage

### From the UI
1. Launch the NationsGlory Helper application
2. Navigate to the "Bot" page
3. Use the provided controls to perform actions or start automated tasks

### Programmatically

```python
from nationsglory.bots.player.bots import player_bot

# Basic controls
player_bot.move("forward", 2)  # Move forward 2 blocks
player_bot.jump()  # Jump
player_bot.attack()  # Attack or break a block
player_bot.use()  # Use item or interact with block

# Automated tasks
player_bot.anti_afk(True)  # Enable anti-AFK
player_bot.auto_farm(60)  # Farm for 60 seconds
player_bot.auto_mine(120)  # Mine for 120 seconds
player_bot.auto_fish(180)  # Fish for 180 seconds

# Chat
player_bot.write("Hello world!")  # Send a message in chat
```

## How It Works

The Player Bot uses PyAutoGUI to simulate keyboard and mouse inputs. It reads the key bindings from your Minecraft options.txt file and maps them to the appropriate PyAutoGUI commands.

## Requirements

- Python 3.10 or higher
- PyAutoGUI
- NationsGlory client installed

## Limitations

- The bot requires the Minecraft window to be in focus
- Some actions may not work correctly if your key bindings are non-standard
- The bot cannot read the game state, so it operates blindly
- Anti-cheat systems may detect and ban automated actions, use at your own risk