# SmartObject

Create a park bench smart object which AI and player can claim and sit on.
(Refering to https://www.youtube.com/watch?v=vUy-UIEHqFA)

## Add following plugins
* SmartObjects
* Gameplay Behaviour Smart Objects (Experimental)
* AI Behaviours


## Gameplay Behaviour
This is what the AI actor will do once it reaches the slot

* Create a GameplayBehaviour blueprint class and name it "BP_GB_ParkBench"
* Play a montage animation (sitting in the bench for example) by connecting a `PlayMontage` node to `OnTriggeredCharacter` event using the avatar pin.
* Now `EndBehaviour` both from 'OnCompleted' and 'OnInterrupted' pins.
* Create a GameplayBehaviourConfig blueprint class, name it "BP_GBConfig_ParkBench" and set the above behaviour to it


## Smart Object Definition
* Create a DataAsset (Misc -> DataAsset) and name it "DA_SODefinition_ParkBench"
* Add slots to the asset, position it accordingly
* You can also set the preview actor if available


## Smart Object Actor
* Create a Blueprint class and name it "BP_SO_ParkBench"
* Add StaticMesh component and add the bench mesh to it
* Add SmartObject component and set the definition asset to the one created above ("DA_SODefinition_ParkBench")