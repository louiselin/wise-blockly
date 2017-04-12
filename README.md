# Wise-Dips GUI
Dips-Blockly GUI update without connect mqtt. 
* [Simple demo](http://140.119.164.152/wise-blockly/demos/blockfactory/demomqtt.html "Simple demo")

## Environment Setting
Need to download project "[closure-library](https://github.com/google/closure-library "closure-library")".

### Blockly Factory
Define block properties, like character(eg, BirdMan>WingUp), trigger(eg, LeftHandUp, RightHandUp), StageEffect, Backgournd, and so on. After creating the block, pressing the 'save' button. It will use mqtt to send json form to unity. 
* Create Trigger
![Create Characters](http://i.imgur.com/DyP9JgT.png "Create Trigger")
* Create Characters
![Create Characters](http://i.imgur.com/8RjSHcg.png "Create Characters")

### Workspace
The Workspace Factory makes it easy to configure a toolbox and the default set of blocks in a workspace.
* Workspace-Create Rule
![Create Rule](http://i.imgur.com/SLjOlZF.png "Create Rule")

---

## Demo ##
### released for March 2017 ###
[![Demo wise-blockly](http://i.imgur.com/MLeTe0X.jpg)](https://youtu.be/xHZ0boMbIKI)

## Procedure ##
1. 接受 WISE Performer 模組資訊
    * 打開Unity－mac os執行檔（WISE Director外操作）
    * WISE Director上，連線（UnityToDips）
2. WISE Director腳本建立（場景 3為例）
    * 創建背景 （DipsToUnity）
        ```
            {
            	"action" : "create-background",
            	"createBackground" : "bg-mountain",
            	"objectId" : "bg-001",
            	"initStatus" : "true"
            }
    * 創建角色
        ```
                {
                	"action" : "create-character",
                	"createCharacter" : "ExampleCharacter",
                	"objectId" : "char-01",
                	"topicName" : "mocap-data-01",
                	"createPosition" : {
                		"x" : "0.0",
                		"y" : "0.5",
                		"z" : "2.0"
                	}
                }
    * 規則建立
        ```
                {
                	"action": "create-rule",
                	"id": "rule-wings",
                	"event": "LeftHandUp",
                	"effectType": "characterEffect",
                	"effectName": "WingsUp",
                	"targetId": "birdman-01"
                }
