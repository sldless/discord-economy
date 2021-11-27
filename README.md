[![Downloads](https://static.pepy.tech/personalized-badge/discord-economy?period=total&units=international_system&left_color=black&right_color=blue&left_text=Total%20Downloads)](https://pepy.tech/project/discord-economy)

# Discord-Economy
##### ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ Makes Economy much easier
___
##### discord_economy.Client(db='discord_economy', db_cluster='Economy', mongo_database='localhost:27017')

###  Example 

```py
import discord, discord_economy, random
from discord.ext.commands import Bot

eco_discord = discord_economy.Client()
bot = Bot(command_prefix='e!')

@bot.event
async def on_ready(): 
     print(f'{bot.user.name} is online | e!help')
 
 @bot.command()
 async def work(self, ctx):
    amount = random.randint(1, 50)
    eco_discord.work(amount, ctx.author.id)
    await ctx.send(f'You worked and gained ${amount}')
    

```
```py
## Functions
discord_economy.Client().work(amount, user_id) # Gain more money
discord_economy.Client().deposit(amount, user_id) # deposit the money to the bank
discord_economy.Client().withdraw(amount, user_id) # withdraw the money from the bank
discord_economy.Client().get_cash(user_id) #Gets the user cash value
discord_economy.Client().get_bank(amount, user_id) #Gets the user bank value
discord_economy.Client().get_network(amount, user_id) # Cash + Bank = Network
discord_economy.Client().get_user_data(user_id) #Returns the user data 
discord_economy.Client().get_mongo_data() #Returns mongo data
```
Since discord.py is not in development anymore, This module will be using [pycord](https://github.com/Pycord-Development/pycord). Please uninstall discord.py and install py-cord :)

Only supports mongoDB
** **
[Discord Server](https://discord.gg/GcHFjejEWR)
