# Power-BI-Cleaner-MS
Power BI Cleaner - Manga Solutions Edition

[Power BI Cleaner](https://www.thebiccountant.com/tools-power-bi-cleaner/) was a tool developed up to 2022 by [Imke Feldmann](https://www.linkedin.com/in/imkefeldmann), as a solution for exploring the used and unused objects within a Power BI Report.

Power BI Cleaner itself was released as a Power BI Template, which made it effectively open for anyone to customise.

To help solve problems for the clients of my [Manga Solutions](www.mangasolutions.com) consulting practice, we made a few enhancements and added a new **Usage** page. 

The intended use of the **Usage** page is to quickly scan the connections between pages, visuals, tables, fields and measures, in any direction. Selecting any entry of any type will cross-filter all the other objects.  For example selecting a Page object will cross filter to show all the visuals on that page, and the tables, fields and measures that they reference. By contrast, selecting a Field  object will cross-filter to show the pages and visuals where it is used, and it's home table.

The format is intended for "business analyst" types and other non-technical users. As the solution is a Power BI report, it can be published or shared via SharePoint or OneDrive, for instant access without even needing to open the source PBIX/PBIP file.  If you need to extend it further, the existing page can offer a guide to 

There are several other tools around now to help with similar tasks, and some of them have more features. But they are mostly specific apps that must be installed, and they require some preparation work using Power BI Desktop. Most are quite technical in style, not aimed at a "business analyst" / non-technical audience. So I believe there is still a niche for this solution.

The sample PBIX provided was pointed at my favourite demo file, the 

The Power BI Cleaner blog post goes through the instructions in detail, but I can offer this condensed "how to" guide to use this solution against your own PBIX file:

1. Open the target file in [Power BI Desktop](https://www.microsoft.com/en-au/power-platform/products/power-bi/desktop)
2. Make a copy of the Power BI Cleaner PBIX file in this solution. I use a file name prefix that matches the target file, to avoid confusion.
3. To get the value for the **PortNumber** parameter, open the target PBIX file using Power BI Desktop and navigate to **Model View / Data / Model** and choose the **Semantic model** node.  Then look in the **Properties** pane for the **Server** property, and hit the **Copy value** button. After pasting into this parameter, edit to remove "localhost:"
4. To get the value for the **ReportFile** parameter in quoted form, use Windows Explorer to navigate to the target PBIX file, then right-click and choose **Copy as path**.
