# FIFA Data Analysis
This project analyzes a dataset containing information about FIFA players. The analysis includes data cleaning, data preprocessing, exploration, and visualization to extract insights into player attributes, club values, player wages, nationality distribution and new features such as Forward, Mid, Back and GK.
## Dataset 
The dataset includes various attributes of FIFA players, such as player ratings, club affiliations, and other characteristics.
## Data Cleaning
Dropped Irrelevant Columns : Columns such as sofifa_id, player_url, long_name, dob, team_jersey_number, nation_jersey_number, weak_foot as there work can be done by other columns

Handling Missing Values: Columns such as loaned_from, player_tags, nation_position and defending_marking were dropped as more than 90% values in these columns were empty and columns such as club_name	and release_clause_eur had less than 5% percent values which were empty so we dropped those rows which had Na values. The columns shooting, pace, passing, dribbling, and defending were filled by taking mean of other columns such as pass_volley, movement_dribbling etc.
## Data preprocessing 
Feature Engineering: New columns Forward, mid, back and GK were created using various player position rating columns for example st,rs,rcm etc. These features can be used to predict player position in football. For this, we first converted the needed columns into strings and then performed replace function on those columns replacing "95 +" with "95+0" which further is solved using eval function,further these columns were stored by talking mean for the evaluated columns in their respective rows.
## Analysis 
### Linear Regression analysis
Forward vs pace,shooting,passing,dribbling and defending : In this section we look at how forward stat changes with various attributes such as pace,shooting,passing,dribbling and defending¶ using scatter plot

  Conclusion : 
  Pace: Positive correlation; pace increases as the forward metric increases.

  Shooting: Strong positive correlation; higher forward metrics are associated with higher shooting metrics.

   Passing: Positive correlation; players with higher forward metrics generally have better passing skills.

   Dribbling: Strong positive correlation; higher forward metrics are associated with higher dribbling metrics.
   
   Defending: Weak positive correlation; data points are more scattered, showing a less consistent relationship.

   Overall, the "Forward" metric shows strong positive relationships with pace, shooting, passing, and dribbling, but a weaker relationship with defending.

Mid vs pace,shooting,passing,dribbling and defending : In this section we look at how Mid stat changes with various attributes such as pace,shooting,passing,dribbling and defending¶ using scatter plot

  Conclusion : 
  Pace: Positive correlation; pace increases as the mid metric increases.

  Shooting: Positive correlation; players with higher mid metrics tend to have higher shooting metrics.

  Passing: Strong positive correlation; players with higher mid metrics generally have better passing skills.

  Dribbling: Strong positive correlation; higher mid metrics are associated with higher dribbling metrics.

  Defending: Positive correlation, but weaker compared to other metrics; data points are more scattered, showing a less consistent relationship.

  Overall, the "Mid" metric shows strong positive relationships with pace, shooting, passing, and dribbling, but a weaker relationship with defending.

Back vs pace,shooting,passing,dribbling and defending : In this section we look at how Back stat changes with various attributes such as pace,shooting,passing,dribbling and defending¶ using scatter plot

  Conclusion :
  Pace: Weak positive correlation; pace shows a slight increase as the back metric increases.

  Shooting: Weak positive correlation; higher back metrics are associated with slightly higher shooting metrics.

  Passing: Positive correlation; players with higher back metrics generally have better passing skills.

  Dribbling: Moderate positive correlation; higher back metrics are associated with higher dribbling metrics.

  Defending: Strong positive correlation; players with higher back metrics tend to have significantly higher defending metrics.

  Overall, the "Back" metric shows the strongest positive relationship with defending, moderate positive relationships with passing and dribbling, and weaker positive relationships with pace and shooting.

GK vs pace,shooting,passing,dribbling and defending : In this section we look at how GK stat changes with various attributes such as pace,shooting,passing,dribbling and defending¶ using scatter plot

  Conclusion :
  Negative Correlation: All plots show a negative correlation between GK rating and each of the other attributes.

  Pace: Higher GK ratings are associated with lower pace ratings.
  
  Shooting: Higher GK ratings correspond to lower shooting ratings.

  Passing: Higher GK ratings are linked with lower passing ratings.

  Dribbling: Higher GK ratings correlate with lower dribbling ratings.

  Defending: Higher GK ratings are related to lower defending ratings.

  Overall, as the GK rating increases, the ratings for pace, shooting, passing, dribbling, and defending decrease, suggesting that players with high goalkeeping skills tend to have lower ratings in these other      attributes.

Player value vs Wage(eur) : In this section we look at how Player value Changes with Wage.

Conclusion : We notice a positive relationship between player value and wage, with higher-valued players generally earning higher wages. However, there is variability in the data, as indicated by the scatter of points and the presence of outliers. This variability suggests that while player value is a strong predictor of wage, other factors may also play a significant role in determining player wages.

### Position analysis
In this analysis we look at how different player position react to forward,mid,back and gk stat using spider plot.

Conclusion : 

Forward Positions (CF, LW, LS, RF, RS, RW): Predominantly strong in the Forward attribute.

Midfield Positions (CAM, CDM, LM, RCM, RAM, RM): Strong in Mid attribute, with some positions also showing strength in Forward.

Defensive Positions (CB, RB, RCB, LWB, RWB): Strong in Back attribute, with some positions also showing strength in Mid.

Goalkeeper (GK): Exclusively strong in the GK attribute.

Balanced Positions (CDM, LWB, RWB, RDM): These positions have a more balanced distribution, strong in Mid and Back attributes.

In conclusion, the data from Forward, Mid, Back and GK can be used to determine a player's position and can also be used for a machine learning model which predicts player's position or suggests a position for a player.

### Club analysis
 Club vs Value(eur) :  In this section we see the top 10 teams who have the most valued players using bar graph.

 Conclusion : 
 From the graph we can see top 10 teams with the most valued players and we can see that Liverpool has the highest total player value amongst the other teams, exceeding €800 million. Real Madrid Manchester City   and Fc Barcelona follow closely with values between €700 million and €800 million. FC Bayern Munchen, Paris Saint-Germain Chelsea, Atlético Madrid, Manchester United, and Tottenham Hotspur have lower values,     indicating a disparity in player market values among these elite teams.

 Clubs vs Wage(eur) : In this we see the top 10 teams who spend the most on player wages.

 Conclusion:
 The graph shows that Real Madrid and FC Barcelona pay the highest total wages to players, each around €5 million. Manchester City and Liverpool also pay substantial wages but less than the top two. Manchester    United and Inter follow with lower total wages. Chelsea, Tottenham Hotspur, Juventus, and Paris Saint-Germain have the lowest total wages among the top 10. There is a significant disparity in wage expenditures   among these elite teams, with Real Madrid and FC Barcelona leading by a large margin.

 ### Nationality analysis
 In this section we will get to know about the top 10 countries with most number of players who are in a club

 Conclusion: 
 England is leading the pack with around 1,600 football players, Germany comes in second with about 1,200 players. Spain and France are almost neck and neck, boasting around 1,000 players, Argentina and Brazil    are also close competitors, with each country having about 800 players.

 Japan has a respectable 400 players, The Netherlands, Italy, and the United States round out the list, each with fewer than 400 players, with Italy and the United States having the lowest numbers among the top  
 10.

 The graph highlights England's dominance in terms of football player numbers, with Germany, Spain, and France also showing strong representation. The remaining countries, while having fewer players, still 
 contribute significantly to the global football community.
