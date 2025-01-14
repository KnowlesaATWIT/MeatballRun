## Presentation  
  This component is handling experience based progression  
  one of the most common progression system in video games.  
  
  You can defined Experience floors, once a floor is  
  reached a Level is won and the experience bar goes  
  back to 0.  
  
----------
  
## Required Components  
 - None
  
----------
  
## Set Up  
 - 1 : Add the Progression component to your prefab  
 - 2 : Define Level min / max  
 - 3 : Define Experience Floors.
  
  Notes : this system is 0 based. As a result, if  
  Experience Floors are defined like this :  
  
  **[100,
     200,
     350]**
  
  The asset will need to accumulate at least 100  
  Experience point before reaching Level 1.  
  
  Based on the same exemple, considering experience  
  points are set back to 0 as soon as a floor is  
  reached, asset will need to accumulate  
  100 + 200 + 350 = 650 Experience point  
  to go from Level 0 to Level 2.  
  
----------
  
## Properties  
  
  **Min : int**  
  Minimum level value accepted.  
  
  **Max : int**  
  Maximum level value accepted.  
  
  **Floors : uint list**
  Quantity of Experience points to be accumulated,  
  before reaching next level.  
  
  Note that experience points are reset every time a  
  level is reached. In the case asset win more  
  experience points than needed to reach next level,  
  no point will be lost.  
  
  ----------
## Events  
  
  *This component is casting events to notify  
  Experience and Level values modifications.*  

  *This is useful if you want to plug additional  
  components using theses informations like some  
  experience UI, or some graphicals effects.*  
  
  **EventLevelUpdated(int previous, int current)**  
  This event is casted every time the Level value is  
  updated. **Previous** parameter gives the value  
  before the change, while **current** gives  
  the value stored once modification is done.  
  
  **EventExperienceUpdated(int previous, int current)**  
  This event is casted every time the Experience value is  
  updated. **Previous** parameter gives the value  
  before the change, while **current** gives  
  the value once modification is done.  



