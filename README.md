<img src="https://avatars2.githubusercontent.com/u/48458546?s=460&v=4" width="100" alt="" data-canonical-src="https://avatars2.githubusercontent.com/u/48458546?s=460&v=4g">  &nbsp;&nbsp;
<img src="https://distributegames.com/images/unity3d-logo.png" width="100" alt="" data-canonical-src="https://distributegames.com/images/unity3d-logo.png">


# DistributeGames.com-SDK WebGL Unity3D
This repository contains the DistributeGames.com SDK for WebGL Unity3D games. This allows you to display advertisements in the games published within the DistributeGames.com network. https://DistributeGames.com


# STEP 1:
<p>Import the .unitypackage into your game. </p>
<p><img src="https://distributegames.com/images/unity/unity_2.png"  width="800" alt=""></p>

# STEP 2:
Drag the prefab "DistributeGames" into your scene. 

# STEP 3:
Copy your GAME_ID in your DistributeGames developer's control panel (in the Game Management > My games > Our game), at https://distributegames.com/account/

# STEP 4:
Open the prefab and replace the GAME_ID values with your own keys. 
<p><img src="https://distributegames.com/images/unity/unity_1.png"  width="800" alt=""></p>

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
