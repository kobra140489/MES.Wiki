ScT-CreateGPS
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