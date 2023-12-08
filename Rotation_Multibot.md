# Rotation Multibot Script Version 2.05


## PROXY SETTINGS
- `Add_Proxy`: To add a proxy [Options: yes or no]
- `Proxy_Limit`: Fill in with number [Bot/Proxy]
### Example
```
Proxy_Limit = 2 
which means 2 Bot / 1 Proxy
```

- `Proxy_List`: To add a proxy to the list
### FORMAT FOR ADDING ONE PROXY
```
Proxy_List = {
  "IP1:PORT1:USERNAME1:PASSWORD1"
}
```

### FORMAT FOR ADDING MORE THAN ONE PROXY
```
Proxy_List = {
  "IP1:PORT1:USERNAME1:PASSWORD1",
  "IP2:PORT2:USERNAME2:PASSWORD2",
  "IP3:PORT3:USERNAME3:PASSWORD3"
}
```


## BOT/INDEX SETTINGS
- `Number_Of_Config_Used`: Represents the total config used / total `sequence number`

## CONFIG INDEX
What is a `sequential number` that has a red box mark

![image](https://github.com/gkshelp/Lucifer-Script/assets/152979525/fd5b96e4-30da-4925-8669-bccf64950cde)

### CONFIG INDEX FORMAT SINGLE BOT
```
----------------- [ CONFIG INDEX `sequence number` ] -----------------
bots[getBots()[`sequence number`].name] = {
  COPY ALL CONFIGS IN IT <*CONFIGS>
}
----------------- [ END CONFIG INDEX `sequence number` ] -----------------
```

### CONFIG INDEX FORMAT MULTI BOT
```
----------------- [ CONFIG INDEX 1 ] -----------------
bots[getBots()[1].name] = {
  COPY ALL CONFIGS IN IT <*CONFIGS>
}
----------------- [ END CONFIG INDEX 1 ] -----------------


----------------- [ CONFIG INDEX 2 ] -----------------
bots[getBots()[2].name] = {
  COPY ALL CONFIGS IN IT <*CONFIGS>
}
----------------- [ END CONFIG INDEX 2 ] -----------------


----------------- [ CONFIG INDEX 3 ] -----------------
bots[getBots()[3].name] = {
  COPY ALL CONFIGS IN IT <*CONFIGS>
}
----------------- [ END CONFIG INDEX 3 ] -----------------
```


## CONFIGS
- `Bot_Format`: Type of bot to be used (cid, guest, createguest, or ubi)
- `Bot_List`: To add a bot to the list
### BOT LIST FORMAT SINGLE BOT
```
CID account: 
Bot_List = {
  {"GROWID1", "PASSWORD"} --Running bot
}

Guest account: 
Bot_List = {
  {"MAC1"} --Running bot
}

Ubisoft Connect account: 
Bot_List = {
  {"EMAIL1", "PASSWORD"} --Running bot
}
```

### BOT LIST FORMAT WITH BACKUP BOT
```
CID account: 
Bot_List = {
  {"GROWID1", "PASSWORD"}, --Running bot
  {"GROWID2", "PASSWORD"}, --Back-up bot
  {"GROWID3", "PASSWORD"}  --Back-up bot
}

Guest account: 
Bot_List = {
  {"MAC1"}, --Running bot
  {"MAC2"}, --Back-up bot
  {"MAC3"}  --Back-up bot
}

Ubisoft Connect account: 
Bot_List = {
  {"EMAIL1", "PASSWORD"}, --Running bot
  {"EMAIL2", "PASSWORD"}, --Back-up bot
  {"EMAIL3", "PASSWORD"}  --Back-up bot
}
```

- `AAP_Verification`: Options: yes or no
```
If you choose `YES` then the bot will wait 1.5 minutes to be verified from AAP.
But if you choose `NO` then the bot will switch to the next bot list if there is an AAP.
```
- `Block_ID`: Fill with the item id of the block to be rotation
- `Rotation_World`: Fill with the rotation world name
- `Rotation_Door_ID`: Fill with the door id of the rotation world
- `Save_Seed_World`: Fill with the save seed world name
- `Save_Seed_Door_ID`: Fill with the door id of the save seed world
- `Drop_Seed_Marker`: Fill with item id as a marker for drop seed
- `Save_Pack_World`: Fill with the save pack world name
- `Save_Pack_Door_ID`: Fill with the door id of the save pack world
- `Drop_Pack_Marker`: Fill with item id as a marker for drop pack
- `Use_Break_Other_World`: To make the bot perform PNB on other world [Options: yes or no]
- `Use_Random_World_For_Break_Other_Break`: To create a random PNB world [Options: yes or no]
- `Break_Other_World`: Fill with the break world name [This section is filled if Use_Break_Other_World = YES and Use_Random_World_For_Break_Other_Break = NO]
- `Break_Other_World_Door_ID`: Fill with the door id of the break world [This section is filled if Use_Break_Other_World = YES and Use_Random_World_For_Break_Other_Break = NO]
- `X_Break`: Fill with the position to perform PNB (Position X)
- `Y_Break`: Fill with the position to perform PNB (Position Y)
- `Auto_Retrieve`: To retrieve an item from GAUT [Options: yes or no]
- `Auto_Buy_Pack`: To purchase an item from the store [Options: yes or no]
- `Pack_Name_To_Buy`: Fill with debug pack name / pack you want to buy
- `Pack_Price`: Fill with the price of the pack to be purchased
- `Max_Buy_Pack`: Maximum pack to be purchased
- `Max_Pack_To_Drop`: Maximum pack to be dropped
- `Drop_Pack_ID`: Fill with the item id of the pack that will be dropped
- `Use_Webhook`: To send a message to a webhook [Options: yes or no]
- `Edit_Webhook_Message`: To edit a message from a webhook [Options: yes or no]
- `Webhook_Link_Bot_Information`: Fill with webhook link
- `Message_ID_Bot_Information`: Fill with webhook message id
- `Webhook_Link_Dropped_Item`: Fill with webhook link
- `Message_ID_Dropped_Item`: Fill with webhook message id
- `Webhook_Link_Reconnect`: Fill with webhook link
- `Message_ID_Reconnect`: Fill with webhook message id
- `Equipment_World`: Fill with the equipment world name
- `Equipment_Door_ID`: Fill with the door id of the equipment world
- `Drop_Equipment_Marker`: Fill with item id as a marker for drop equipment
- `Auto_Fossil`: To perform fossil retrieval in the rotation world (Must have equipment such as: Rock Hammer, Rock Chisel, and Fossil Brush) [Options: yes or no]
- `Auto_Kill_Ghost`: To perform killing all ghost in the rotation world (Must have equipment such as: Neutron Power Glove) [Options: yes or no]
- `Anti_Fire`: To perform clearing all fire in the rotation world (Must have equipment such as: Fire Hose) [Options: yes or no]
- `Anti_Toxic`: To perform clearing all toxic waste in the rotation world
- `Wearing_Specific_Item`: To wear specific item
- `Wearing_Specific_Item_ID`: Fill with the item id that you want to wear 
- `Max_Specific_Item_To_Retrieve`: Maximum for specific item retrieval


## MAIN SETTINGS
- `Looping_World`: To looping the rotation world [Options: yes or no]
- `Auto_Plant`: To plant the seed [Options: yes or no]
```
If you choose `YES` the seed will be planted.
But if you choose `NO` the seed will not be planted and will only be dropped in the save seed world.
```
- `Ignore_Gems`: Creating bot will not take the gems [Options: yes or no]
- `Custom_Break_Tile`: Number of tile to be PNB [Options: 1 tile to 5 tile]
- `Change_Bot`: To change bot [Options: yes or no]
- `Change_Bot_Cooldown`: cooldown for change bot [In minutes]
- `Change_Bot_On_Max_Level`: To change bot if the current bot reaches the set maximum level
- `Min_Level`: Set the minimum level
- `Max_Level`: Set the maximum level
- `Change_Bot_On_Playtime`: To change bot if the current bot reaches the set playtime
- `Playtime`: Set the playtime
- `Take_Pickaxe`: To take a pickaxe [Options: yes or no]
- `Pickaxe_World`: Fill with the pickaxe world name
- `Pickaxe_Door_ID`: Fill with the door id of the pickaxe world
- `Pickaxe_ID`: Fill with the item id that you want to wear (You can use hand items like Pickaxe, Death Ray, and other hand items)
- `Auto_Buy_Rare_Clothes_Pack`: To buy rare clothes pack (Only buy 1× rare clothes pack per bot) [Options: yes or no]
- `Auto_Take_Floating_Block`: To take the floating block [Options: yes or no]
- `Auto_Hidden_World`: To hide the history of various worlds (Such as hide rotation world, save seed world, save pack world, etc.) [Options: yes or no]
- `Hidden_World_List`: Fill with random world list
- `Use_Webhook_For_All_Bot_Information`: To send a message to a webhook [Options: yes or no]
- `Edit_Webhook_Message_For_All_Bot_Information`: To edit a message from a webhook [Options: yes or no]
- `Webhook_Link_All_Bot_Information`: Fill with webhook link
- `Message_ID_All_Bot_Information`: Fill with webhook message id
- `All_Bot_Information_Cooldown`: Cooldown of sending messages to the webhook [In seconds]
- `Ban_Wave_Estimated`: To estimate the ban wave time (Bot will go offline if enabled) [Options: yes or no]
- `Growtopia_Time_Difference`: The bot will go offline according to Growtopia time. Enter the time difference between your device and Growtopia time using the /gks-timecalculator command to help your calculation
- `Ban_Wave_Estimated_Time`: Fill in with the estimated ban wave time [In Growtopia time]
- `Ban_Wave_Estimated_Cooldown`: Offline time cooldown as long as the estimate expires [In minutes]


## OPTIONAL SETTINGS
- `Harvest_Delay`: Set harvest delay [In milliseconds]
- `Plant_Delay`: Set plant delay [In milliseconds]
- `Hit_Block_Delay`: Set hit block delay [In milliseconds]
- `Put_Block_Delay`: Set put block delay [In milliseconds]
- `Auto_Buy_Delay`: Set buy pack delay [In milliseconds]
- `Join_World_Delay`: Set join world delay [In milliseconds]
- `Reconnect_Delay`: Set reconnect delay [In milliseconds]
- `High_Ping`: Fill with the minimum estimated ping high
- `Max_Reconnect_Cooldown`: Cooldown reconnect [In minutes]
- `Mod_Entered_Cooldown`: Offline time cooldown as long as the estimate expires [In minutes]
- `Move_Interval`: Findpath interval [In milliseconds]
- `Move_Range`: Bot move range (Suggested move range is 3)
- `Show_Animation`: Make a bot to show the punch and place item animation [Options: yes or no]
- `Max_Block_To_Retrieve`: Maximal block taken to break
- `Max_Seed_To_Drop`: Maximal seed taken to plant
- `GMT_Time_Zone`: This just turns the RDP time into your local time
- `Trash_Item_ID`: Fill with the list of item that will be trashed
- `Random_Chat_Status`: Make the bot send random messages [Options: yes or no]
- `Random_Chat_List`: List of random messages to be sent by the bot
- `Chat_Cooldown`: Cooldown of sending messages sent by bot [In Seconds]
