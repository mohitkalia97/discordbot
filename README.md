# Discord Bot for Medium Posts

This repository contains a Discord bot that automatically fetches the latest Medium post and sends it to a specified Discord channel. The bot uses Java with the JDA (Java Discord API) library.

# What the Bot Does:
Initialization: Upon being started, the bot logs in to Discord using a provided token.
Scheduled Posting: The bot is scheduled to fetch the latest Medium post and post it to a Discord channel twice a day, specifically at 9 AM and 5 PM.
Fetching Medium Post: It uses Rome tools to fetch the latest post from a specified Medium RSS feed.
Key Implementation Details:
JDA (Java Discord API): The bot uses JDA to interact with Discord. It listens for the ReadyEvent which is triggered once the bot has logged in successfully. Once this event is triggered, the bot starts its scheduled tasks.

Scheduled Posting: Java's built-in scheduling mechanism, ScheduledExecutorService, is used to run a specific task at desired intervals. We've set it up to run twice a day.

Fetching from Medium: The Rome tools library is used to fetch and parse the latest post from a Medium RSS feed. The bot then posts the title and link of the latest article to the specified Discord channel.

# How to Use:
Set Up Your Configurations:

Replace YOUR_BOT_TOKEN_HERE with your bot's token.
Update the MEDIUM_RSS_URL with the desired Medium RSS feed.
Modify the DISCORD_CHANNEL_ID to point to the channel where you want the bot to post.
Run the Bot:
Compile and run the DiscordBot main class.

Feel free to contribute or raise issues if you find any!
