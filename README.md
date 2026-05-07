# Ultimate-Banking-Inventory-System

## Banking, inventory and time tracking script for AI Dungeon
![Image Alt](https://github.com/Itsbrazyyy/Ultimate-Banking-Inventory-System/blob/a93f8a837966306087a45145992ba9d9813d1628/AI-Dungeon-(7).png)

### UBIS brings structure, immersion, and world‑simulation to your AI Dungeon adventures.
It handles currency, inventory, bills, income, time progression, price references, quests and story card syncing — all automatically.
 Designed for players who want deeper worlds, consistent rules, and a smooth, Quality of life experience.
 # Features
| Feature | Description |
| --- | --- |
| **Automated Currency System** |💵Wallet (Within the Inventory SC) that separately tracks, adds and deducts currency. It will also decline purchases if you lack the income😹|
| **Smart Inventory Tracking** |👜Inventory system that automatically adds and removes and updates items via keyword trigger. |
| **Time Progression Engine** |🕰️Time Tracking with triggerable skip features. Configurable advancing hours, days, weeks, or months based on narration or player commands. |
| **Bills & Income Automation** | 💳Bill tracking with automatic expense deduction and income addition to wallet. You can add or remove bills and income here and toggle them on and off.|
| **Price Reference System** |🏘️A Price List story card for AI‑readable cost of living ranges for realistic world pricing. |
| **Story Card Syncing** | Inventory, wallet, bills, time, and config cards stay perfectly updated. |
| **Slash Commands** | Power‑user controls for configuration, debugging, and customization. (Currently available: /ubis disable, /keywords, /help)|

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

# Creator Information
- In the "Library" Script at the top you will find a Boilerplate with full customization settings for your scenario. Adjust these to match your world settings💗
- I would appreciate the reference when using this script 💗 (Example: Made by "ItsBrazyyy")
# Useful Information 
- Ai Dungeon Link: https://play.aidungeon.com/
- Script link on Ai Dungeon: https://play.aidungeon.com/scenario/4MSdmu6UWa_-/ultimate-banking-inventory-system-v11?share=true&published=true
- Ai Dungeon Official Discord Link: https://discord.gg/HpuNBKSb
 
## 📜 Changelog

<details>
<summary><strong>Click to expand</strong></summary>

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
