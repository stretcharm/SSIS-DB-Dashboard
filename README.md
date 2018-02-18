# SSIS-DB-Dashboard
PowerBI SSIS Catalog DB Dashboard

Intro																																								
This SSIS Catalog DB Dashboard aims to show the progress, performance an problems with any SSIS projects running on your server.
It collects data from a number of the key tables/views in the SSIS Catalog DB as well as current running jobs from msdb.

I bring in and summarise the data is at a variety of levels
	Execution (Execution & Execution Summary)
		The Package that is Executed First which I've named RootPackageName. This includes the Project & Folder
	Package (Executable Package Stats)
		Package Summary. I group Packages by Types e.g. Master/Dimension/Fact/Stage/PostProcess. You can customised these in the PackageTypes Table. Click Advanced Editor to change it.
	Executable (Executable Stats)
	Items inside the Package e.g. Tasks/Data Flows/Containers. I also call this level Package Steps

Data is also shown for Currently Running Packages and SQL jobs. You can refresh this individually to get quick updates.
This dashboard also provides details of any package errors and maps them to the Microsoft IS Error Reference Names.
Individual Executions can be viewed as a text based Gantt chart or as a matrix of executions by time slices.
I also extract row counts from the SSIS data flow messages to complement the duration based dashboards
Finally I extracted the Hierarchy from the execution paths to make a Network diagram and Sankey to visualise the structure and levels in an SSIS project/

I've tried to keep the custom visuals to a minimum  but I have used Sankey/Network Navigator as well as the OKViz Bullet and Sparklines.
The PowerBI is blank with that needs the server parameter setting to your SSIS db server before applying the changes and granting permissions. 

Forum Post																			http://community.powerbi.com/t5/Data-Stories-Gallery/SSIS-Catalog-DB-Dashboard/m-p/244677				
Templates for the package can can be found here.				https://github.com/stretcharm/SSIS-DB-Dashboard


Added a new version that is dedicated to the currently running packages and todays errors.


Thanks to the providers of the following pages that I've used to help in the making of this dashboard.

https://blogs.msdn.microsoft.com/sql_pfe_blog/2017/04/18/ssisdb-reporting-with-power-bi/
Chris Schmidt

https://www.excelguru.ca/blog/2015/01/28/creating-a-vlookup-function-in-power-query/
Ken Puls

Star Ratings Quick Measure
http://community.powerbi.com/t5/Quick-Measures-Gallery/Star-Ratings/m-p/166903#M12
Chris Webb

https://ssisreportingpack.codeplex.com/
Jamie Thomson

Lots of Dax help and great OK Vis PowerBI Visualisations
http://www.sqlbi.com/

SSIS Catalog DB
https://docs.microsoft.com/en-us/sql/integration-services/service/ssis-catalog

Reza Rad's Article on the SSIS Catalog
http://www.rad.pasfu.com/index.php?/archives/75-SSIS-Catalog-Part-3-Folder-Hierarchy;-Folder,-Projec...
DB Diagram
http://www.rad.pasfu.com/ssis/ssiscatalogpart3/5.png

SSIS Error Codes
https://docs.microsoft.com/en-us/sql/integration-services/integration-services-error-and-message-ref...

