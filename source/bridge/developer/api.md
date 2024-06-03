# Example Extension

```python
from discord.ext import commands
from core.config import DiscordConfig

class MessageCog(commands.Cog):
    def __init__(self, bot):
        self.bot = bot

    @commands.command()
    @commands.has_role(DiscordConfig.overrideRole)
    async def message(self, ctx, player, *, message):
        await self.bot.mineflayer_bot.chat(f"/w {player} {message}")
        await ctx.send(f"Message sent to {player}!")

async def setup(bot):
    bot.add_cog(MessageCog(bot))
```
