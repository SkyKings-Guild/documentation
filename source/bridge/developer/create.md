# Creating an Extension

The base of an extension is a literal extension straight out of the discord.py extension system. 
You have a `setup` method that takes a `bot` parameter (the Discord bot class), 
and you can add in a cog to make commands, listen to events, and more.

This is a simple example of an extension that adds a command to the bot:

```python
from discord.ext import commands

class NewCommand(commands.Cog):
    def __init__(self, bot):
        self.bot = bot

    @commands.command()
    async def newcommand(self, ctx):
        await ctx.send("Hello, world!")

async def setup(bot):
    await bot.add_cog(NewCommand(bot))
```

If you want to send a message to Hypixel, you can use `bot.mineflayer_bot.chat`:

```python
@commands.command()
async def boop(self, ctx, *, player: str):
    await self.bot.mineflayer_bot.chat("/boop " + player)
    await ctx.send("Boop sent!")
```

For more information, visit the [discord.py documentation](https://discordpy.readthedocs.io/en/stable/ext/commands/index.html).