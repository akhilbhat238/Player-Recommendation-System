# Player-Recommendation-System
A football based AI solution to recommend the right signings to the right football clubs.


Build a player recommendation system for clubs to invest their transfer budget on. 

1. The system will classify what level a club is at, and identify the next level for a club to reach.
	a. This is based on current position and average position over the last 5 years
	b. Winning a champions league, national league, national cups will be considered.
	c. Each competition(leagues) will have a weightage.
		i. How many CL winners/finalists are in the competition --25 years. Each 5 year set has it's own weightage.
		ii. How many Euro winners/finalists are in the competition --25 years. Each 5 year set has it's own weightage.
		iii. How many WC/Euro/Copa winners are present?	
	d. Cumulative club score will be used to identify club level
2. The system will assess the strengths of the club in each position, average the value and compare it against the average attributes of the clubs at the next level.
3. The system will assess the area where the club is most lacking and prioritise.
4. Once an area of the field is decided, system will identify a specific position where an upgrade can be made.
5. The attributes to be considered, have to be derived as follows:
	a. Consider the top 5 leagues
	b. Classify different players into their positions using Preferred Position
	c. Pick 25 players with top Overall value in each position
	d. Average out all values, to identify what the highest performing attributes are.
	e. Prepare attribute list for each position
	f. Create a cumulative desired score for each position
6. Identify weakest position:
	a. Preapre cumulative score of each player in the area to be upgraded. 
	b. Dervive the average cumulative score. 
	c. Derive the difference between desired score and current average score.
	d. Top difference value is considered as position to replace.
	e. Prepare a list of positions to be replaced with descending order of necessity
7. Identify position to consider across all areas:
	a. These are then considered and run through a weighted multiplier. i.e Position disparity vs area of need is calculated
	b. Order the positions in the descending order for biggest disparity
	c. Rows corresponding to top 3 cumulative scores is then considered.
