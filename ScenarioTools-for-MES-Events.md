ScT-CreateGPS

https://steamcommunity.com/sharedfiles/filedetails/?id=2998575759





### Tags 
<!--ActivateCustomAction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ActivateCustomAction|
|:----|:----|
|Tag Format:|`[ActivateCustomAction:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--CustomActionName  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionName|
|:----|:----|
|Tag Format:|`[CustomActionName:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|no|
<!--CustomActionArgumentsString  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsString|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsString:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsBool  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsBool|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsBool:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsInt  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsInt|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsInt:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsFloat  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsFloat|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsFloat:Value]`|
|Description:|nan|
|Allowed Values:|Any float equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsLong  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsLong|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsLong:Value]`|
|Description:|nan|
|Allowed Values:|Any long equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsDouble  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsDouble|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsDouble:Value]`|
|Description:|nan|
|Allowed Values:|Any double equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--CustomActionArgumentsVector3D  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArgumentsVector3D|
|:----|:----|
|Tag Format:|`[CustomActionArgumentsVector3D:Value]`|
|Description:|nan|
|Allowed Values:|Any Vector3D equal or greater than 0|
|Multiple Tag Allowed:|yes|








Description: This custom action creates a new GPS marker with specified parameters.

Parameters:

string name: The name of the GPS marker.
string desc: The description of the GPS marker.
int time: The time (in seconds) the GPS marker will be active.
Vector3D coord: The coordinates of the GPS marker.
Usage:

csharp
Copy code
MESApi.RegisterCustomAction(true, "ScT-CreateGPS", CustomActions.CreateGPS);
ScT-RemoveGPS
Description: This custom action removes GPS markers with names containing a specified string.

Parameters:

string name: The string used to filter GPS markers for removal.
Usage:

csharp
Copy code
MESApi.RegisterCustomAction(true, "ScT-RemoveGPS", CustomActions.RemoveGPS);
ScT-AddNews
Description: This custom action adds a news item to the system, broadcasting it to all players.

Parameters:

string text: The text of the news item.
Usage:

csharp
Copy code
MESApi.RegisterCustomAction(true, "ScT-AddNews", CustomActions.AddNews);
ScT-SpawnPlanetaryInstallation
Description: This custom action spawns a planetary installation at a specified location.

Parameters:

string spawnGroup: The group name for the planetary installation.
Vector3D coord: The coordinates where the installation should be spawned.
Usage:

csharp
Copy code
MESApi.RegisterCustomAction(true, "ScT-SpawnPlanetaryInstallation", CustomActions.SpawnPlanetaryInstallation);
ScT-SpawnPlanetaryBlockade
Description: This custom action spawns a planetary blockade near players within a specified radius.

Parameters:



string spawnGroup: The group name for the spawned blockade.
int MinRadius: The minimum radius from players for spawning.
int MaxRadius: The maximum radius from players for spawning.
int SpawnDistance: The distance from players where the blockade should be spawned.
Vector3D PlanetCentercoord: The coordinates of the center of the planet.
Usage:

csharp
Copy code
MESApi.RegisterCustomAction(true, "ScT-SpawnPlanetaryBlockade", CustomActions.SpawnPlanetaryBlockade);
Additional Notes:
Ensure that you have the necessary permissions and prerequisites for each custom action.
Custom actions are registered with the MESApi for execution in the game environment.
Adjust parameters as needed for your specific use case.
Refer to individual method documentation for more details on parameter usage and functionality