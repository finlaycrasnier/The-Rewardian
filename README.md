# The-Rewardian

'The-Rewardian' is a Power Automate bot that utilises VBA to remove select spreadsheet data, speeding up part of the wage budgeting process.

The context of the 'The-Rewardian' revolves around the annual wage budgeting process. The budgeting process begins with a master file spreadsheet (MS Excel) containing wage information regarding employees across all departments within the business. The file has to be sent to each department for financial budgeting, but first removed of any confidential information not relating to that line of business (e.g. HR recieving Sales employee information). Before the project, this process was performed entirely by hand, consuming ≈80 hours of employee resources. In addition to this, mistakes from manual human labour resulted in an increased risk of data breaches. We aimed to create a bot that could perform the required modifications in a faster and more secure manor.

The process was split in 2 sections - file handling and file cutting. The file handler used data fed by the user into a data directory to duplicate the budget master file and rename them according to an assigned department. The cutter was then utilised to enter each of these files and remove any employee information not relating to that department (based on the name).

The first version of the bot did not utilise VBA and was not dynamic. This version was very slow, taking approximately 20 hours to run for the 100+ files needed. It involved a loop of the 'Delete Row' function in Power Automate depending on information found in each cell. As each file had 11 sheets with 1000s of rows for each employee, the processing time was very slow. We tested multiple alternative methods, and eventually found the use of VBA, in conjunction with Power Automate, to be the quickest. 

We decided later that we wanted to make the bot fully dynamic so it could 'cut' any sheet based on user input. This allows the bot to be utilised for additional tasks outside of the budgeting process, saving time on other projects.
