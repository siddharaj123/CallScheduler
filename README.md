This Project contains 2 source code files.

Description: I developed two scripts that integrate the Telegram and Google Sheets API. This tool helps to send all the information in a row of a google sheet to a particular telegram user, who's user ID matches the user ID listed in the google sheet. 

The first one named getMembersInfo.py scrapes the data from a telegram group of the user's choosing and stores it in a CSV file called Members.csv

The second file, named sheets.py, loops through a google sheet which stores the User ID's of the telegram users that the user scraped from the first source file (this part has to be done manually). It loops through the google sheet and sends info to the respective UserID's, as a direct message

To Run:
1. Go to https://my.telegram.org/apps, to set up your Telegram API account
2. Watch this short video to set up your Google APIs: https://www.youtube.com/watch?v=cnPlKLEGR7E&t=272s&ab_channel=TechWithTim
3. Insert your API keys into the source code files.
4. Install Telethon (using pip)
5. Run getMembersInfo.py first to get a scraped file of all telegram users 
6. Run sheets.py (with an active google sheet that has Telegram User IDs in the 2nd column) 
(python3 sheets.py members.csv).

BackStory to the Project (for those interested)
At my temple, we were always looking for ways to increase our weekly attendance for our sermons. One way we decided was through making phone calls every week to remind people to attend our weekly sermons. But our method to doing it was very inefficient. Before, our local admin would create an excel or google sheet that would have all the data for the people that needed to be called, and that spreadsheet was then placed on the volunteers group telegram group. However, as the week went on, the message containing the spreadsheet was lost in the chat, making it hard to go back and find where the spreadsheet was. Furthermore, the spreadsheet was packed with data, and even with proper formatting, it was hard for anyone to be able to really read it, especially from a mobile device. 

To solve this issue, I developed sheets.py, which would take the data from the spreadsheet which had the information about which people to call, and it would message volunteers individually on telegram (which was the main form of communication that everyone used) and notify them very clearly in a readable format about what calls they had to make during the week.

