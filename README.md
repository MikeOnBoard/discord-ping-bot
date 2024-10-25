# **Discord-ping-bot**
## **Project Structure**
```go
discord-ping-bot/
├── bot/
│   └── bot.go
├── config/
│   └── config.go
├── main.go
├── go.mod
├── go.sum
```
## **Description**
**``discord-ping-bot``** is a Discord bot built with Golang to demonstrate Discord API interactions through basic commands. This bot’s core functionality is to verify connectivity by responding to user messages, especially the "ping" command, allowing users to confirm the bot’s online status. It serves as a foundational project for developers interested in creating more advanced Discord bots.

## **Prerequisites**
- **Golang**: Make sure Go is installed. Refer to the official Golang installation guide if needed.
- **Discord Bot Token**: You need a bot token, which can be obtained by creating a new application and bot on the Discord Developer Portal.
## **Installation**
1.**Clone the Repository**:

```bash
git clone https://github.com/MikeOnBoard/discord-ping-bot.git
cd discord-ping-bot
```
2.**Install Dependencies**: Download the dependencies required for the project with:

```bash
go mod download
```
3.**Configure the Bot**:

- Update ``config/config.go`` to include your bot token. This token is crucial for the bot to authenticate with Discord.
## **Detailed File Overview**
- **main.go**: This is the entry point of the application, handling initial setup and execution. It initializes the bot, loads configuration, and runs the core function to start the bot.

- **bot/bot.go**: Contains the primary bot functionalities, such as defining commands and responding to Discord events. The ``bot.go`` file listens to messages in channels and interacts based on command keywords, especially for ``ping`` commands, providing an immediate response for connection testing.

- **config/config.go**: Stores configuration settings. This file defines and loads essential configurations, such as the bot token, making it easier to modify environment-specific settings without changing the main code.

- **go.mod** and **go.sum**: Manage Go module dependencies, ensuring that all required packages and libraries are specified and remain consistent.

## **Setting Up the Bot on Discord**
1.**Create the Bot**:

- Go to the Discord Developer Portal.
- Create a new application, then add a bot under the "Bot" section.
- Copy the bot token, as it will be used in the configuration.
2.**Add the Bot to a Server**:

- Under "OAuth2" > "URL Generator," select ``bot`` under "OAuth2 scopes."
- Assign required permissions (e.g., ``Send Messages``, ``Read Messages``).
- Copy the generated URL and paste it into your browser to add the bot to your server.
3.**Enable Intents**:

. Go to "Bot" > "Privileged Gateway Intents" and enable both M``ESSAGE CONTENT INTENT`` and ``SERVER MEMBERS INTENT``. This allows the bot to read messages and respond appropriately.
## **Usage**
To start the bot, run:

```bash
go run main.go
```
Once the bot is running, go to any channel where it has access and type ``ping``. The bot will respond with ``Pong``, confirming that it is active and listening to commands.

## **Example**
- **Ping Command**: Send ``ping`` in any channel where the bot is active.
  - **Expected Response**: The bot replies with ``Pong``, verifying it’s online and functional.
## **Key Features**
- **Message Interaction**: Listens to specific commands (``ping``) and responds, demonstrating core message-handling capabilities.
- **Extensible Structure**: Provides a base to add new commands and event listeners, which can be easily extended in ``bot.go``.
## **Conclusion**
The ``discord-ping-bot`` project offers a solid foundation for building more complex Discord bots. With a modular structure and focus on simplicity, it allows developers to extend functionality by adding custom commands, enhancing the bot’s interactivity. This bot serves as an introduction to Discord’s API and showcases how to establish responsive bot commands in a Golang environment.