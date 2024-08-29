# Neural-Network-Final-Project

Baseball is a sport of precision and anticipation. Every game is a battle between the pitcher at the mound and the batter at the plate. The goal of a pitcher in baseball is to throw the ball into a “strike zone” in a way that does not allow the batter at the plate to hit the ball. Major League Baseball (MLB) defines the “strike zone” as “the area over home plate from the midpoint between a batter's shoulders and the top of the uniform pants -- when the batter is in his stance and prepared to swing at a pitched ball -- and a point just below the kneecap.” 1 The strike zone is rectangular shaped with 9 zones within the rectangle and 4 zones outside the rectangle resulting in 14 different parts depending on where the ball was thrown. For a pitch to be considered strike either: 

Part of the ball must cross over part of home plate while in the strike zone. (Called Strike) 

The ball made contact with the batter's bat. 

The batter started swinging the bat, decided to stop, but the bat broke the plane at the bottom of the plate according to the 1st or 3rd base umpire. (Check Swing) 

Every game there is an umpire behind home plate opposite the pitcher that determines whether a given pitch is determined to be a strike. With batters changing every at bat, the umpire must change the strike zone to match the height of the batter at the plate. However, this constant shift in the strike zone has resulted in inconsistent pitch calls which can favor the batter or the pitcher depending on the umpire. Not only does the strike zone shift during the game, but the strike zone also shifts depending on the umpire behind the plate.  

With Pitchers and Batters frustrated by inconsistent pitch calls, Major League Baseball decided to introduce a new pitch system called the “Automatic Balls and Strikes System” (ABS). This system created a new “electronic strike zone” that can be overlayed on live camera footage for pitch confirmation. “In 2019, the independent Atlantic League used the electronic strike zone in an all-star game, and that same year, the Arizona Fall League was played with the ABS. In 2021, the ABS was deployed in some Class A parks." (Olney)   

In 2023, it was announced that the electronic strike zone will be used in all 30 Triple AAA (One level below the Major Leagues) parks in 2 ways. “Half of the Class AAA games will be played with all of the calls determined by an electronic strike zone, and the other half will be played with an ABS challenge system similar to that used in professional tennis. Each team will be allowed three challenges per game, with teams retaining challenges in cases when they are proved correct. MLB's intention is to use the data and feedback from both systems, over the full slate of games, to inform future choices.” (Olney) 

 

Goal of this Project: 

Before this new ABS system, it was impossible to have a standard strike zone that could be compared to each other. However, that is no longer the case. This electronic system now allows teams to challenge the pitch in a way that can correct umpire mistakes and make the game fair for batters and pitchers alike.  

The goal of this project is to utilize Deep Learning Methods in a way that helps predict pitch call (Ball or Strike), pitch type, and strike zone area based on the metrics of the pitch thrown. By understanding the pitch metrics and whether that pitch is considered a strike or a ball, pitchers will be able to be more precise in their pitches, so they get the strike call that they want. Thus, our goal is to create a basic framework for future Deep Learning models related to this issue.  

 

Dataset: 

The data that we will be using comes from the MLB’s advanced tracking technology that collects and analyses a massive amount of baseball data. From 2015-2019, Statcast consisted of a combination of cameras and radar systems to collect the data. However, in 2020 this changed with the introduction of the Hawk-Eye. (Same camera used for instant replay at all major tennis tournaments) This new camera increased the tracking ability, and now every team in the league has 12 Hawk-Eye cameras set up strategically around the stadium. For our study's purposes, there are 5 key cameras, which have higher frames per second, focusing on pitch tracking.  

The specific data that we will be using has been downloaded using pybaseball. This is a python package built for baseball data analysis as it allows for easy scraping of Statcast data and a few other key baseball stat-keeping sources. Using this package, we set a date range for all the pitches we wanted to include in our dataset. We selected March 30, 2023, to October 1, 2023. This date range encapsulates the entire 2023 MLB regular season. After downloading this data, we ended up with 92 columns of pitch-by-pitch data for 717,504 individual pitches. Many of the columns were unrelated to the goal of this project (described above) so they were deleted from the dataset, but a comprehensive list of the columns in original dataset can be found here: Statcast Search CSV Documentation | baseballsavant.com (mlb.com).  
