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
