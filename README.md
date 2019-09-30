# pkl
Pro kabaddi League

Task	                                                                                         Prediction
Predict the winner of the tournament	                                                        Dabang Delhi
Predict the the top team in the points table after the completion of league matches	          Dabang Delhi
Predict the team with the highest points for successful raids	                                Dabang Delhi
Predict the team with the highest points for successful tackles	                              Puneri Paltan
Predict the team with the highest super-performance total	                                    Bengal Warriors
Predict the player with the highest SUCCESSFUL RAID percentage	                              Pawan Kumar Sherawat
Predict the player with the highest SUCCESSFUL TACKLE percentage	                            Vishal Bharadwaj

Task 1: Predict the winner of the tournament .

Data : The data for predicting the overall winner of the tournament was primarily scrapped from https://en.wikipedia.org/wiki/Pro_Kabaddi_League .

Of all the available data , season wise data was collected for each individual match played so far in league stages.

The Data Frame for each season was made separately , containing columns like Team 1 name , Team 2 name , Team 21 score , Team 2 score , Winner and Venue .

Then All the Data frames of All the seasons are concatenated together to form a master dataframe .
This data frame is then cleaned to make sure that the 12 team names appear consistent through out the dataframe columns and that scores columns are integer only .
Further the Venue column is cleaned to make sure only city names appear instead of complete venue names.

For all the remaining matches of season 7 based on schedule obtained from the official site , another data frame is created of all upcoming .

Based on this , each upcoming match teams are stored in variables like Team 1 and team 2 and venue of upcoming match . Then these values are tested against past behaviour . Below mentioned 7 conditions are tested for Team 1 Vs Team 2 appearing in master dataframe . Based on results of these conditions points are awarded to each team , and in the end , the team with higher points is declared the winner of that upcoming match .

Based on this , the top 6 qualifires are chosen at the end of the league seasons and then a schedule is made about which team will face whom in elimination, semifinals and final. These matches are again considered as upcoming matches and predictions are made based on same master data frame .

The 7 conditions are. :

If the team is in top 3 standings currently , it has better chance then next 3 , then next 3 and then lowest 3 . So based on this , the teams are awarded -2 points if they lie in lowest 10-12 , -1 point if they life from 7-9 position. +1 point of they lie in 4-6 and +2 if they lie in 1-3 position of current standinds.
Which team among the two has won more number of times in Head to Head competitions at all venues?
Which team among the two has scored more points against the other team in Head to Head competitions at all venues?
Which Team has won more matches at this venue in head to head competition.?
which team has scored more in head to head competiion at current venue?
Which Team has won more matches against all oppositions at current venue?
Which Team has scored more points against all oppositions at current venue?
Based on the these 7 conditions a winner is chosen of that match and similarly for all upcoming matches including the finals .

Task 2 : Predict the top team in the points table after the completion of the league matches.

The same dataframe as mentioned in task one , upto league stages is used to predict the winner of upcoming league matches and +5 points are awarded to each win , based on this final poiints tally is made and the top team is predicted.

Task 3 , 4, 5 ,6 ,7 : Visualisations and pattern are used to identify the winner using linear regression.
