## Presentation  
  This component meets the need to make an asset apearance  
  evolving based on the level of the asset himself.  
  
  Can be used, for exemple, with characters, buildings, cards  
  ships, cars, etc...  
  
----------
  
## Required Components  
- Doodah.Components.Progression.Progression  
  
----------
  
## Set Up  
 - 1 : Add the ProgressionBasedSkin component to your prefab  
 - 2 : Feed the Skins property with game objects  
  
  Notes : the link between this component and Progression is made automagically during the Start() function.
  
----------
  
## Properties  
  
  **Skins : List**  
  List of game objects to use as skins for this asset.  
  
  On Start, skin defined on index 0 is used by default.  
  
  Skin update is ignored if Skins is null or if required index
  is out of range.  

