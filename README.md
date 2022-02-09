# Python-AmongUsProblem
Project in which we modelise an Among Us problem using graph theories.


![map](https://user-images.githubusercontent.com/59508102/153099073-278e991f-c237-46a6-9243-a198a5868512.jpg)

The rules are as following:

    Total of 100 players
    10 players per game
    3 random games then
    each game regroups the players by a batch of ten following their ranking.
        The last 10 players (in the ranking) are ejected to the tournament.
        Do it until it remains only 10 players
    For the last 10 players, play 5 games with reinitiated ranking. Update and check the ranking of the 10 players and give the podium.

Here is the ranking model:

    Impostor: 1pts per kill, 3pts per undiscovered murder, 10pts if win
    Crewmate: 3pts if the argument unmasks an imposter, 1pts if all solo tasks are made, 5pts if win

Each time a game ended, the score of each player is the mean of all its games.

# We were asked two things : 
By knowing information such as : 
Player 0 has seen player 1, 4 and 5
Player 1 has seen player 0, 2 and 6

We need to find who could be the killer using graphs.

Considering that a player can only walk through the map, but an impostor can also travel with vent, it is important to compute the time to travel between each room for crewmates and impostors.
We compare the time to travel between any pair of room in two cases: if you are a crewmate; if you are an impostor.

![impostor map](https://user-images.githubusercontent.com/59508102/153099063-f3732c58-7362-4354-b050-e1b92a954c5e.jpg)

