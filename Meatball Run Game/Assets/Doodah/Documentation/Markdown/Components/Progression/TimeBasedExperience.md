## Presentation  
  This component will deliver experience on a time basis, 
  perfect to handle progression of growing elements like plants 
  for exemple

----------
  
## Required Components  
 - Progression

## Required Utils  
 - TimeKeeper (singleton)
  
----------
  
## Set Up  
 - 1 : Add the TimeBasedExperience component to your prefab  
 - 2 : Define PointPerSeconds  
 - 3 : On instantiation, set the CreationTimestamp and LastUpdate properties to current timestamp (in seconds).
  
  On Update, the component will compare the current 
  timestamp to the lastUpdate value and deliver any number 
  of experience. Note that if LastUpdate is in the future 
  the amount of experience will be negative. 
  
----------
  
## Properties  
  
  **PointsPerSecond : float**  
  Number of experience points per second.  
  
  **LastUpdate : long**  
  Timestamp in second at which experience has been gain for the 
  last time.  

  **CreationTimestamp : long**  
  Timestamp in second at which the object has been created.  
  
  ----------
## Events  
  
  *This component is listening events from the Progression 
  component to stop the update process once max level is 
  reached.*  




