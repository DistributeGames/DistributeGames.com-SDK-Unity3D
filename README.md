# DistributeGames.com-SDK WebGL Unity3D
This repository contains the DistributeGames.com SDK for WebGL Unity3D games. This allows you to display advertisements in the games published within the DistributeGames.com network. https://DistributeGames.com


# STEP 1:
<p>Import the .unitypackage into your game. </p>

# STEP 2:
Drag the prefab "DistributeGames" into your scene. 

# STEP 3:
Copy your GAME_ID in your DistributeGames developer's control panel (in the Game Management > My games > Our game), at https://distributegames.com/account/

# STEP 4:
Open the prefab and replace the GAME_ID values with your own keys. 

# STEP 5:
Use DistributeGames.Instance.ShowAd() to show an advertisement. 

# STEP 6:
Make use of the events DistributeGames.OnResumeGame and DistributeGames.OnPauseGame for resuming/pausing your game in between ads.

# Example:
<pre>public class ExampleClass: MonoBehaviour {
	void Awake()
	{
	  DistributeGames.OnResumeGame += ResumeGame;
	  DistributeGames.OnPauseGame += PauseGame;
	}
	
	void OnDestroy()
	{
	  DistributeGames.OnResumeGame -= ResumeGame;
	  DistributeGames.OnPauseGame -= PauseGame;
	}

	public void ResumeGame()
	{
	  // RESUME MY GAME
	}

	public void PauseGame()
	{
	  // PAUSE MY GAME
	}

	public void ShowAd()
	{
	  DistributeGames.Instance.ShowAd();	
	}
}</pre>

If you have any technical questions or comments, please email us at:
info@distributegames.com

Or simply check documentation on:
https://distributegames.com/sdk
