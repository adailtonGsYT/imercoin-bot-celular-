# Limercoin Auto Game Bot

A comprehensive automation bot for playing games on the Limercoin platform. This bot can both simulate games locally and directly automate gameplay on the Limercoin website.

## Features

- **Multi-Game Support**: Automates gameplay for Coin Catcher, Puzzle, and 2048
- **Web Automation**: Directly plays games on the Limercoin website using Selenium
- **Configurable Settings**: Customize gameplay parameters, timing, and game selection probabilities
- **Interactive Dashboard**: Monitor bot status, statistics, and control gameplay through a Streamlit UI
- **Command-Line Interface**: Run web automation directly from the command line

## Components

1. **Limercoin Bot**: Core bot engine that simulates gameplay (limercoin_bot.py)
2. **Web Player**: Selenium-based automation for the actual Limercoin website (limercoin_web_player.py)
3. **CLI Interface**: Command-line interface for direct web automation (limercoin_cli.py)
4. **Streamlit Dashboard**: Web-based GUI for monitoring and controlling all bot functions (app.py)

## Quick Start

### Using the Dashboard

1. Start the Streamlit dashboard:
   ```
   streamlit run app.py --server.port 5000
   ```

2. Access the dashboard at http://localhost:5000

3. Configure settings in the Configuration tab

4. Use the Dashboard tab to start/stop the bot

5. Use the Web Automation tab to connect to the actual Limercoin website

### Using the Command Line

```bash
# Play the Coin Catcher game on Limercoin website
./limercoin_cli.py --username your_username --password your_password --game coin_catcher --cycles 3

# Run in visible browser mode
./limercoin_cli.py --username your_username --password your_password --show-browser

# Random game selection based on configuration probabilities
./limercoin_cli.py --username your_username --password your_password --game random
```

## Configuration

All bot settings are stored in `config.json` and can be modified through the Configuration tab in the dashboard.

## Game Modules

- **Coin Catcher**: Simulates gameplay for collecting coins
- **Puzzle**: Simulates sliding puzzle gameplay
- **2048**: Simulates the 2048 game with strategic moves

## Web Automation

The Web Automation feature uses Selenium to directly interact with the Limercoin website:

1. Log in to your Limercoin account
2. Navigate to the games page
3. Select and play the chosen game
4. Apply gameplay strategy based on configuration settings
5. Collect rewards and complete games

## Requirements

- Python 3.6+
- Streamlit
- Selenium
- ChromeDriver (automatically managed by webdriver-manager)
- Trafilatura (for web content extraction)

