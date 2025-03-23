Structure of the newly created csv files :-

	1) player_stats.csv - 
		a) General Player Info :
			player: Name of the player (e.g., "MS Dhoni," "V Kohli").
			match_count: Total number of matches played by the player in IPL.
		
		b) Batting Performance Metrics :
			total_run_bat: Total runs scored by the player across all matches.
			balls_faced: Total number of balls faced by the player while batting.
			6_count: Number of sixes hit by the player.
			4_count: Number of fours hit by the player.
			2_count: Number of doubles hit by the player.
			1_count: Number of singles taken by the player.
			batting_average: Average runs scored per innings (total_run_bat / total_innings). Reflects consistency in scoring.
			strike_rate: Runs scored per 100 balls faced ((total_run_bat / balls_faced) * 100). Indicates scoring speed and efficiency.
			highest_run: Highest score achieved by the player in a single innings.
		
		c) Bowling Performance Metrics
			total_wicket: Total number of wickets taken by the player across all matches.
			total_run_bowl: Total runs conceded by the player while bowling.
			balling_over: Total overs bowled by the player (balls_bowled / 6).
			bowling_economy: Average runs conceded per over (total_run_bowl / balling_over). Lower values indicate better bowling efficiency.
	
	2) team_stat.csv - 
		a) General Team Info
			team_name: Name of the IPL team (e.g., "Royal Challengers Bengaluru").
			match_played: Total number of matches played by the team.
			matches_won: Number of matches won by the team.
			win_percentage: Percentage of matches won by the team (calculated as (matches_won / match_played) * 100).
		
		b) Batting Performance Metrics
			total_batting_run: Total runs scored by the team in all matches.
			total_balls_faced: Total balls faced by the team while batting.
			run_rate: Average runs scored per over while batting (total_batting_run / (total_balls_faced / 6)).
			total_4s: Number of fours hit by the team.
			Total_6s: No. of sixes hit by the team.
			highest_score: The highest and lowest scores achieved by the team in a match.
			lowest_score: The lowest scores achieved by the team in a match.
		
		c) Bowling Performance Metrics
			total_bowling_run: Total runs conceded by the team while bowling.
			total_overs_bowled: Total overs bowled by the team (total balls bowled / 6).
			economy_rate: Average runs conceded per over while bowling (total_bowling_run / total_overs_bowled).
		
		d) Powerplay Metrics
			powerplay_batting_run: Total runs scored during powerplay overs.
			powerplay_count: Number of powerplay innings played.
			powerplay_wickets: Number of wickets lost during powerplay overs.
			powerplay_bowling_run: Total runs conceded during powerplay overs while bowling.
			powerplay_boundary_count: Number of boundaries (fours and sixes) hit during powerplay overs.
			powerplay_dot_count: Number of dot balls bowled during powerplay overs while bowling. Indicates pressure created on opposing batsmen.
			average_powerplay_score: Average score during powerplay overs (powerplay_batting_run / powerplay_count). Shows scoring efficiency in this phase.
		
		e) Death Overs Metrics
			death_runs: Total runs scored during death overs.
			death_count: Number of death innings played.
			average_death_score: Average score during death overs (death_runs / death_count). Shows finishing ability in this phase.
	
	3) seasonal_stat.csv -
		a) General Season Info
			Season no: Unique identifier for each IPL season (e.g., "1" for the inaugural season in 2007/08).
			Year: The year in which the IPL season was held (e.g., "2007/08," "2009").
		
		b) Season-Wide Stats
			total_run_in_season: Total runs scored in all matches by all teams combined in the season.
			total_number_of_innings: Total number of innings played during the season. Generally, 2 per match
			average_run_per_match: Average runs scored per match in the season (total_run_in_season / total_number_of_innings). Shows the scoring trends and batting conditions during that season.
			targets_200+: Number of times a team set a target of 200 or more runs during the season.
		
		c) Individual Achievements
			orange_cap_holder: Name of the player who scored the most runs in the season (e.g., "SE Marsh," "V Kohli").
			orange_cap_run: Total runs scored by the Orange Cap winner during that season.
			
			purple_cap_holder: Name of the player who took the most wickets in the season (e.g., "SL Malinga," "B Kumar").
			purple_cap_wicket: Total wickets taken by the Purple Cap winner during that season.
	
	4) team_season_stats.csv -
		a) General Info
			team_name: Name of the IPL team (e.g., "Mumbai Indians," "Chennai Super Kings").
			season_no: The season number in which the statistics were recorded (e.g., "1" for the inaugural season in 2008).
		
		b) Performance Metrics
			total_runs: Total runs scored by the team during the season.
			total_matches: Total number of matches played by the team in that season.
			average_score: Average score per match for the team during the season. Calculated as (total_runs / total_matches). It reflects the team scoring consistency in that particular season.
		
	5) top_bowlers_stats.csv -
		a) General Info
			season_no: Unique identifier for each IPL season
		
		b) Bowling Performance Metrics
			bowler: Name of the bowler (e.g., "Sohail Tanvir," "SL Malinga").
			wickets: Total number of wickets taken by the bowler during the season.
			economy_rate: Average runs conceded per over by the bowler during the season (total_runs_conceded / total_overs_bowled).
