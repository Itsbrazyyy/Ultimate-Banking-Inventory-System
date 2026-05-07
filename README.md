# Ultimate-Banking-Inventory-System

## Banking, inventory and time tracking script for AI Dungeon
![Image Alt](https://github.com/Itsbrazyyy/Ultimate-Banking-Inventory-System/blob/a93f8a837966306087a45145992ba9d9813d1628/AI-Dungeon-(7).png)

### UBIS brings structure, immersion, and world‑simulation to your AI Dungeon adventures.
It handles currency, inventory, bills, income, time progression, price references, quests and story card syncing — all automatically.
 Designed for players who want deeper worlds, consistent rules, and a smooth, Quality of life experience.
 # Features (New!)
| Feature | Description |
| --- | --- |
| **Automated Currency System** | 💵 Wallet tracking that automatically adds, deducts, converts, and declines purchases when funds are insufficient. |
| **Smart Inventory Tracking** | 👜 Auto‑detects item gains and losses using expanded keyword triggers for seamless inventory updates. |
| **Time Progression Engine** | 🕰️ Automatically advances time based on narration cues or player commands, including hours, days, weeks, and months. |
| **Bills & Income Automation** | 💳 Recurring expenses and income with improved interval parsing and automatic ledger logging. |
| **Holidays Story Card** | 🎊 Built‑in festivals, solstices, birthdays, and religious days synced to UBIS time. |
| **Events Story Card** | 📆 Create one‑time or repeating events with optional lead‑time reminders and automatic clearing. |
| **Seasonal Weather System** | 🌦️ Configurable weather tables for fantasy, modern, and sci‑fi settings. |
| **Bounty Board** | 🎯 Story card for defining minimum and maximum payouts for quests, jobs, and contracts. |
| **Narration Switch** | 🧭 Toggle to prevent the AI from narrating or deciding actions for your character. |
| **Expanded Price List** | 📦 Cost‑of‑living reference for realistic NPC pricing across multiple categories. |
| **Story Card Syncing** | 🔄 Inventory, wallet, bills, time, and config cards stay perfectly updated. |
| **Slash Commands** | ⌨️ Power‑user controls for configuration and debugging, including `/help`, `/keywords`, and `/ubis disable` (Story Mode only). |

# 📦 Installation Guide
#### 1. Open AI Dungeon on your computer (or switch your mobile browser to Desktop Mode).

#### 2. Create a new scenario or open one you want to edit.

#### 3. At the top of the editor, go to the DETAILS tab.

#### 4. Scroll down until you find Scripting, then toggle Scripts ON to Enable the script.

#### 5. Click EDIT SCRIPTS.

#### 6. In the left sidebar, select the Input script tab.

#### 7. Remove any existing code inside that tab.

#### 8. Paste the following script into the now‑empty Input section:
```javascript
// ============================================================
//  UBIS INPUT MODIFIER
// ============================================================
const modifier = (text) => {
  text = onInput_UBIS(text);
  return { text };
};

modifier(text);
```
#### 9. then proceed to your "Context" tab on the left. 
#### 10. Delete all the code within it and paste this code into your "Context" tab
```javascript
// ============================================================
//  UBIS CONTEXT MODIFIER
// ============================================================
const modifier = (text) => {
  text = onContext_UBIS(text);
  return { text };
};

modifier(text);
```
#### 11. Now go to your "Output" tab
#### 12. Follow the same process, delete everything inside and paste this:
```javascript
// ============================================================
//  UBIS OUTPUT MODIFIER
// ============================================================
const modifier = (text) => {
  text = onOutput_UBIS(text);
  return { text };
};

modifier(text);
```
#### 13. Go to your Library now, delete all within 
#### 14. Open the link below. Copy the entire Library code and and paste this into your Library: 
https://github.com/Itsbrazyyy/Ultimate-Banking-Inventory-System/blob/c21dfc1a83da26f2ef29522bcfc7a0e9d1473b6a/UBIS-Library-Script-V2txt

#### 15. Now Click SAVE in the top Right Corner
### And now you've successfully installed UBIS! 🥳 All adventures from this scenario, including existing ones will now have this script installed. 

## Gameplay Tips
1. If you dont see the script upon loading the scenario, ensure that you have Enabled Scripts in your gameplay settings. 
2.  If you're planning to customize currency within a scenario, I recommend doing so before progressing in your scenario. These changes can be made in the "Configure UBIS" story card.
3. use /keywords to see a list of useable phrases for your adventure. When you want currency to be tracked, try not to add words between the count and currency. For Example: "I received a single gold coin."🚫 "I recieved a gold coin."✅
4. Different models may react differently
5. Add additional triggers to the SC based on your needs. For example, if you want the AI to memorize your inventory if you bring it up later in the scenario just add "Inventory" or something else to the triggers. (Or simply put it in your Plot essentials or Ai instructions💗)
6. if you use /ubis disable to disable the script but want to enable it again later, enable it from the "Configure UBIS" SC. Switch the script from "OFF" to "ON"
7. If your slash commands arent working, make sure you are using slash commands in "Story" mode. Not Do, say or see.
8. If youre using events and your time progression is slow, I recommend manually toggling or deleting the event once its over. (Example: You have a surprise birthday party event and after the party you continue the scenario regularly. the ai will try to start the event again until the day ends. the event automatically deletes on its own the next day.)

# Creator Information
- In the "Library" Script at the top you will find a Boilerplate with full customization settings for your scenario. Adjust these to match your world settings💗
- I would appreciate the reference when using this script 💗 (Example: Made by "ItsBrazyyy")
# Useful Information 
- Ai Dungeon Link: https://play.aidungeon.com/
- Script link on Ai Dungeon: https://play.aidungeon.com/scenario/4MSdmu6UWa_-/ultimate-banking-inventory-system-v11?share=true&published=true
- Ai Dungeon Official Discord Link: https://discord.gg/HpuNBKSb
 
##📜 Changelog

<details>
<summary><strong>Click to expand</strong></summary>

 
📝Changelog — UBIS V.2
- Added Holidays Story Card (festivals, solstices, birthdays, religious days)
- Added Events Story Card with lead‑time reminders and auto‑clearing
- Added Seasonal Weather System with configurable tables
- Added Bounty Board for quest/job payout ranges
- Added Narration Switch to stop AI auto‑decision making
- Expanded currency and inventory keyword detection
- Improved bills & income interval parsing and automation
- Expanded Price List categories for consistent world pricing
- Enhanced Story Card syncing and slash command reliability
- General code cleanup, optimization, and stability improvements

### v1.1
#### Fixes: 
- the year can now be edited within the "Configure time Settings" story card along with the month, day and hour. 

#### New Features:
- UBIS Script now has a boilerplate at the top of the script for easy default adjustments. (Recommended by @Iairin)
- Added "Price List" story card to settings ( Can be enabled/disabled in Configure UBIS Story card.) this card allows you to adjust the cost of living concept of your world. Information here will be fed to your story for NPCs to recall for consistent gameplay. 
- Added "Currency Context" feature to the Configure UBIS story card. turning this off will stop feeding cost of living knowledge to the Ai.

### v1.1.0
- Initial release

</details>
