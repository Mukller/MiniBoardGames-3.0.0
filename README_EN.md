<div align="center">

**English** • [Русский](README.md)

</div>

# MiniBoardGames 3.0.0

<div align="center">

🎮 **A Minecraft plugin** that adds mini-games right to your server

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Minecraft](https://img.shields.io/badge/Minecraft-1.16.5%2B-green)](https://www.minecraft.net/)
[![Java](https://img.shields.io/badge/Java-11%2B-orange)](https://www.java.com/)

[About](#-description) • [Installation](#-installation) • [Commands](#-main-commands) • [Configuration](#-configuration) • [Contributing](#-contributing) • [License](#-license)

</div>

---

## 📋 Description

**MiniBoardGames** is a powerful and flexible plugin for Minecraft servers that lets players take part in a variety of mini-games right on the server. It's perfect for creating an engaging experience, entertaining your community, and encouraging player interaction.

The plugin supports a large number of configurable mini-games, from classic card games to modern arcades.

---

## ✨ Key features

- 🎮 **20+ built-in mini-games** (2048, Flappy Bird, Battleship, Jack or Queen, and many more)
- 👥 **Full multiplayer support** (from 1 to N players per game)
- ⚙️ **Flexible configuration system** (each game is configured separately)
- 💾 **Statistics tracking** (wins, losses, and rating points)
- 🏆 **Built-in reward system** (coins, experience points, items)
- 🌍 **Localization support** (Russian, with easy addition of others)
- 🔧 **Hot-reload system** (change configs without restarting the server)
- 📊 **Detailed database** (storing all game events)

---

## 📋 Requirements

| Component | Version | Notes |
|-----------|--------|-----------|
| **Java** | 11 or higher | Required to run the plugin |
| **Minecraft Server** | 1.16.5+ | Supports all versions from 1.16.5 |
| **Bukkit/Spigot/Paper** | Any modern fork | Full compatibility |

---

## 🚀 Installation

### Quick start (3 steps)

1. **Download the plugin**
   - Download `MiniBoardGames.jar` from [Releases](https://github.com/Mukller/MiniBoardGames-3.0.0/releases)

2. **Install it on the server**
   ```bash
   cp MiniBoardGames.jar /path/to/server/plugins/
   ```

3. **Restart the server**
   ```bash
   # Full restart (recommended on first install)
   /stop
   # Start the server again
   ```

### Detailed instructions

On first launch the plugin automatically creates:
- 📁 `plugins/MiniBoardGames/` — the plugin's main folder
- ⚙️ `plugins/MiniBoardGames/config.yml` — main settings
- 🎮 `plugins/MiniBoardGames/games/` — configs for all mini-games
- 💾 `plugins/MiniBoardGames/miniboardgames.db` — the game-stats database

---

## 🎮 Main commands

### For players

| Command | Description | Example |
|---------|---------|---------|
| `/mbg help` | Plugin help | `/mbg help` |
| `/mbg play <game>` | Start a mini-game | `/mbg play 2048` |
| `/mbg list` | List all available games | `/mbg list` |
| `/mbg stats` | View your statistics | `/mbg stats` |
| `/mbg profile <player>` | Another player's profile | `/mbg profile Steve` |

### For administrators

| Command | Description | Requirement |
|---------|---------|-----------|
| `/mbg reload` | Reload the configuration | `mbg.admin` |
| `/mbg reset <player>` | Reset a player's stats | `mbg.admin` |
| `/mbg debug` | Toggle debug mode | `mbg.admin` |

### Permissions

```
mbg.play              - Permission to play mini-games
mbg.play.<game>       - Permission for a specific game (e.g. mbg.play.2048)
mbg.stats             - View statistics
mbg.admin             - All administrative commands
mbg.reload            - Reload configs
```

---

## ⚙️ Configuration

### Main config (`config.yml`)

```yaml
# Main plugin settings
plugin:
  debug: false                    # Enable debug mode
  language: ru_RU                 # Interface language (ru_RU, en_US)
  auto-save-interval: 300         # Save interval in seconds

# Game settings
games:
  enabled-games:
    - "2048"
    - "flappybird"
    - "battleship"
    - "coinflip"
    - "checkers"
    - "connect4"
    # Add/remove games as needed

# Reward system
rewards:
  enabled: true
  money-per-win: 100              # Money per win (if Vault is used)
  exp-per-win: 50                 # Experience per win
  multiplier-per-streak: 1.5      # Multiplier for a win streak

# Database settings
database:
  type: sqlite                    # DB type (sqlite or mysql)
  # If using MySQL:
  # host: localhost
  # port: 3306
  # name: minigames
  # user: root
  # password: password
```

### Per-game configuration

Each game has its own config file in the `games/` folder:

**Example: `games/2048_config.yml`**
```yaml
enabled: true
min-players: 1
max-players: 1
time-limit: 600                   # Seconds
difficulty: medium                # easy, medium, hard
```

**Example: `games/battleship_config.yml`**
```yaml
enabled: true
min-players: 2
max-players: 2
board-size: 10x10
time-per-move: 30
```

---

## 🎮 Available games

| Game | Players | Description |
|------|---------|---------|
| **2048** | 1 | Logic puzzle — merge the tiles |
| **FlappyBird** | 1 | Arcade — fly between the pipes |
| **BattleShip** | 2 | Strategy — find the enemy's ships |
| **CoinFlip** | 2 | Gambling — guess the coin side |
| **Checkers** | 2 | Strategy — classic checkers |
| **Connect4** | 2 | Logic — line up 4 in a row |
| **BlackJack** | 1-4 | Cards — reach 21 points |
| **Hearthstone** | 2 | Cards — a collectible card game |
| **HigherLower** | 1 | Logic — guess the next card |
| **CandyCrush** | 1 | Match-3 — collect candies |
| **FabulousFred** | 1-2 | Platformer — clear all levels |

And many more...

---

## 📊 Statistics system

The plugin tracks:
- 📈 Number of wins/losses
- ⏱️ Time spent in games
- 🏆 Achievements and records
- 💰 Rewards earned
- 🎯 Rating points

Stats are stored in the database and available via commands:
```
/mbg stats              - Your statistics
/mbg profile <player>   - A player's profile
```

---

## 🤝 Contributing

We welcome contributions from developers! Here's how to take part:

### Change process

1. **Fork the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/MiniBoardGames-3.0.0.git
   cd MiniBoardGames-3.0.0
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Make changes and commit them**
   ```bash
   git add .
   git commit -m 'Add: description of your change'
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/AmazingFeature
   ```

5. **Open a Pull Request** on GitHub

### Style guide

- Follow the existing code style
- Add comments to complex functions
- Update the documentation when needed
- Write clear commit messages

### PR types

- 🐛 **Bug fixes** — fixing errors
- ✨ **Features** — new capabilities
- 📚 **Documentation** — documentation improvements
- 🔧 **Refactoring** — code improvements

---

## 🐛 Reporting bugs

Found a bug? Help us fix it!

### How to write a good issue

1. **Check** that the bug isn't in existing issues
2. **Describe the problem** in as much detail as possible
3. **Attach logs** (`plugins/MiniBoardGames/debug.log`)
4. **State the version** of Minecraft, Java, and the plugin
5. **Reproduction steps** — how to reproduce the bug

### Issue template

```markdown
## Description
A detailed description of the bug

## Steps to reproduce
1. Do this
2. Then that
3. The error occurs

## Expected behavior
What should have happened

## System info
- Minecraft version: 1.19.2
- Java version: 17
- Plugin version: 3.0.0
- Logs: [attach log]

## Additional context
Any other information
```

Create an issue: [GitHub Issues](https://github.com/Mukller/MiniBoardGames-3.0.0/issues)

---

## 📖 Documentation

- [Full user guide](docs/USER_GUIDE.md)
- [Admin guide](docs/ADMIN_GUIDE.md)
- [Developer guide](docs/DEVELOPER_GUIDE.md)
- [FAQ — Frequently Asked Questions](docs/FAQ.md)

---

## 🔐 Security

If you discover a security vulnerability, please **do not report it in issues**. Instead, email [security@example.com](mailto:security@example.com).

---

## 📝 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for the full text.

**In short:**
- ✅ You can use it for personal and commercial purposes
- ✅ You can modify and distribute the code
- ⚠️ You must credit the authors of the original code
- ⚠️ The author is not liable for damages

---

## 👨‍💻 Author and contributors

| Role | Contact |
|------|---------|
| **Creator** | [Mukller](https://github.com/Mukller) |
| **Lead developer** | [@Mukller](https://github.com/Mukller) |

### Thanks to all contributors! 🙏

---

## 📞 Contact and support

- 💬 [Discord server](https://discord.gg/example) (if available)
- 🐛 [Bug reports](https://github.com/Mukller/MiniBoardGames-3.0.0/issues)

---

## 🎉 Acknowledgements

Thanks for using **MiniBoardGames**! If you like the plugin, a star ⭐ on GitHub helps a lot!

<div align="center">

**Made with ❤️ by Mukller**

</div>
