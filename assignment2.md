Hockey Time Keeper Database Design 

# Public Interface:
  There are multiple classes that will be used in order to create the user interface. The Menu class will allow the user to navigate around the program,
  the Player class will allow the user to store inputted players and related information while the player list will store previously 
  entered players and allow the user to view or update their information. 

## Classes
 ### Player Class: 
  The player list contains three constructors that are instrumental to adding new players as well as copying and   
  updating existing players 
  
  The first constructor, named Roster, will contain variables storing general information about the player, such as their name and 
  height. Statistical information will be initialized here and declared as zero to signify the status of a newly entered player. There 
  are several variables associated with the Roster constructer that will be accompanied with the
  following accessors. Roster will deal with the creation of new players  
 
  - getName which returns the name of the player, 
  - getBirth which returns the exact date the player was born in 
  - getHomeTown which returns the hometown of the player 
  - getWeight which returns information about the players weight 
  - getHeight which returns information about the players height 
  - getJerseyNum which returns information about the players number
  
  There is an enum used for the position of the player, which will encode the information and give the user a limited range of 
  positions to choose from
   
  - Position enum {LW, RW, C, D}; 
  
  The second constructor, named Recreation, will take in information involving the previously mentioned roster information as well as 
  their play performance, such as their total goals. This constructor, like the first, will bring in additional variables accompanied 
  with accessors. Recreation will deal with existing players in order to update information on them
  
  - All of the getters in the Roster constructer are valid 
  - getGoal which returns the total amount of that players goals 
  - getAssists which returns the total amount of assists that player has done 
  - getPowerPlayGoals which returns the amount of goals the player has scored during a power play 
  - getPowerPlayAssists which returns the amount of assists the player did during a power play.  
  - getShots which returns their total shots 
  
  There are methods involved with obtaining the shot percentage, the regular points and the powerpoints. They use two already
  existing variables in order to be calculated, and once they are calculated the data is converted into a String. toString will be used 
  to format the variables so that the data can be transfered in a proper format to the PlayerList class. 
  
 # PlayerList Class: 
  The player list will output player data onto a file where the name will be stored along with other inputted names for further use. 
  A constructor will be used to set up an object and ArrayLists for storing roster. Additionally, another constructor will be used to 
  set up the file reader.  
  
  It is important to first import the usage of ArrayLists, File outputting/reading and Scanners into the class 
    
  - import java.io.*;
   
  - import java.util.Scanner; 
   
  - import java.util.ArrayList;
  
  The first constructor will initialize an object taking values from the roster class and passing them into the normal and wrapped 
  ArrayList. This is to preserve the order of the data for the new player as the wrapped version will possess a large number of Strings
  and mess up both the index and positional value and make data retrieval from file difficult.
   
  - Player p: The object meant to retrive the data from the player class and into the array lists
  - ArrayList<Player> player: The Arraylist taking in the object form of the data  
  - ArrayList<String> segmentPlayer: The wrapped array list that will segment the object and turn its elements into a string  
  
  The second constructor will initialize the object and the scanner that will be used for reading previous data. The reason I chose this
  method is that I feel it is much more efficient to work within the class for player lists in order to both output and input file data.
  
  - String fNameIn: This string will be used to search for the file name 
  - File in = new File (insertName.txt): Will be used to enter the file 
  - Scanner inFile: Will be used to read the file specified by File in
  
  The methods involved with this class will be used for several things. A batch of methods will be involved in adding values to the 
  player information that was initially declared as zero within the Roster Constructor. Of course, a method will be needed to specify   
  the player whose information is being changed in order for that batch to have meaning. A method will be used for outputting 
  Array List information onto a file, while another method will read created files. The last method will correctly output the 
  information to the user. 
  
  - addGoal allows user to add more goals to a selected player
  - addAssist allows user to add more assists to a selected player 
  - addPowerGoal allows user to add more power play goals to a selected player 
  - addPowerAssist allows user to add more power play assists to a selected player
  - playerStatChange allows user to select a player in order to change their stat information 
  - playerListArchiver would allow user to output ArrayList information onto a file for archival purposes 
  - archiveReader would allow user to pinpoint a file and retrieve the player data contained within it
  - toString which would allow user to print out the information to the user in proper and readable format 
  
# Private interface 
Simply all of the variables that are unaccessable to the user. The instance variables are what will store the information of the player,
and there are several in order to store a different part of the user. The values these variables store are central for the program, so
the user must not be able to access and change them hence their private designation. There are private methods which will be used to 
store information that can be calculated, as they also  

# Classes:
## Player 
  - private String name, stores name of player
  - private String birthDate, stores birthdate of player
  - private String homeTown, stores home town of player
  - private String weight, stores weight of player
  - private String height, stores height of player
  - private String jerseyNum, stores jersey number of player
  - private Position position, is an enum involving 4 different positions.
  - private String goal, stores number of goals
  - private String assist, stores number of assists 
  - private String 
  
  There are methods involved with declaring variables  
  
  - private int goalInt(): Converts string value returned by goal into an int for integer calculation (points, goalPercentage) 
  - private int shotInt(): Converts string value returned by goal into an int for integer calculation (goalPercentage)  
  - private String goalPercentage(): returns goal percentage as a String value by using the int values of goal and points   
  - private String points(): returns points as a String value by using int values of (I forgot) 
  - private String powerPoints(): returns powerpoints as a String value by using int values of 
  
