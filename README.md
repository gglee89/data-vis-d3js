# data-vis-d3js
This is a Data Visualization project using D3.
Below is my notes compiled from the [Udacity's Data Visualization and D3.js](https://classroom.udacity.com/courses/ud507) course

# Good References

- What makes a good data visualization? *(by Cole Nussbaumer, People Analytics Manager @Google)*
> "It depends on the purpose of the DataViz. I tend to draw a disctiction between the **Exploratory** and the **Explanatory** where exploratory you're really trying to get a sense of *What the data is, what it can tell you?* is a process of turning over maybe 100 different rocks to try to find those, one or two interesting nuggets. Then once you found the interesting nuggets you're in the explanatory space of wanting to communicate those things to somebody else. When it comes to effective data visualization on the exploratory size, it's about allowing your users to be able to connect things in interesting ways and look at data frmo different angles in an unbiased and unleading way."
> "...the most successful explanatory data visualizations, make themselves a pivotal point in a story or a narrative that's being told."  - Cole Nussbaumer, [Website](www.storytellingwithdata.com/about/) & [Linkedin](https://www.linkedin.com/in/colenussbaumer)

- Data visualization use cases examples:
  - [http://twitter.com/nytgraphics](http://twitter.com/nytgraphics)
  - [http://smallmeans.com/nwe-york-times-infographics](http://smallmeans.com/nwe-york-times-infographics)
  - [http://flowingdata.com](http://flowingdata.com)
  - [infosthetics.com](infosthetics.com)
  - [http://www.thefunctionalart.com/](http://www.thefunctionalart.com/)
  - [http://visualisingdata.com/](http://visualisingdata.com/)
  - [http://helpmeviz.com/](http://helpmeviz.com/)
  - [http://www.tableausoftware.com/public/](http://www.tableausoftware.com/public/)
  - [http://raw.densitydesign.org/](http://raw.densitydesign.org/)

- Interactive data visualization for the web (by Scott Murray):
  - [Book at Amazon.com](https://www.amazon.com/Interactive-Data-Visualization-Web-Introduction/dp/1449339735/ref=sr_1_1?ie=UTF8&qid=1479540876&sr=8-1&keywords=interactive+data+visualization+for+the+web+by+Scott+Murray)
  
- Alberto Cairo's three steps to become a visualization design (by *Andy Kriebel, Data Viz guru @Facebook*):
  - [http://www.vizwiz.com/2013/01/alberto-cairo-three-steps-to-become.html](http://www.vizwiz.com/2013/01/alberto-cairo-three-steps-to-become.html)
  
- Hand Rosling's 200 Countries, 200 Years, 4 minutes (BBC Four):
  - [Watch the entire video](https://www.youtube.com/watch?v=jbkSRLYSojo)
<a href="https://www.youtube.com/watch?v=jbkSRLYSojo" target="_blank"><img src="https://cloud.githubusercontent.com/assets/16644017/20454019/43bd6c9c-ae78-11e6-926b-fde2d7e4f7c4.png"  alt="Hans Rosling" width="100%" height="100%" border="10" /></a>

- Data Visualization in Data Science
![screen shot 2016-11-19 at 4 05 38 pm](https://cloud.githubusercontent.com/assets/16644017/20453763/5a395b62-ae72-11e6-92ad-3db296c7e2ef.png)
  - acquire & parse:
    - Data ingestion [Web scraping, log collection, database accesses, and et cetera. or ETL];
    - Data wrangling [MongoDB];
  - filter & mine:
    - Modeling, data mining, and exploratory analysis;
    - applying statistical and mathematical theory to discover insights;
    - EDA(Exploratory data analysis) [R, Python];
    - Modeling, statistics and machine learning;
  - represent, refine:
    - Experiment different visual encodings (Color, Shapes, Lines, Axis) to present data in the most effective manner;
    - Data Visualization [D3.js];
  - interact:
    - enable users to potentially discover insights for themselves;


# D3.js (version 3.0)
- Selectors chainable nature:
  - E.g. d3.select('.navbar').select('.navbar-header').styles('background','red');
- Building scales:
  - x-axis [Population life expentancy]
    - (Linear scale) d3.scale.linear().domain([15, 90]).range([250, 0]) *px range inversed to match SVG's plot coordinates*
    - In functional notation: f(15) = 250; f(250) = 0;
  - y-axis [GDP per capita]
    - (Log scale) d3.scale.log().domain([(250, 100000]).range([0, 600]);
    - In functional notation: f(250) = 0; f(100000) = 600;
  - circles [population]
    - (Square root scale) d3.scale.sqrt().domain([52070, 1380000000]).range([40, 10]);
    - In functional notation: f(52070) = 40; f(1380000000) = 10;


### Mini-Project 1: Raw Visualization
- Foreign citizens (non-korean) in Seoul, South Korea
  - Project 001: Scatter plot of foreign citizens (non-koreans) in Seoul South Korea with a student visa (D-2) and job seeking visa (D-10) (aggregated by district).
  - X-axis: Foreign citizens (non-koreans) seeking job in Seoul, South Korea;
  - Y-axis: Foreign citizens (non-koreans) with a student-visa;
  - Circle radius: Foreign citizens (non-koreans) in Seoul, South Korea;
  - Basic conclusion: There's a positive correlation between foreign citizens (non-korean) studying in korea ( are seeking jobs.
![foreign students seeking for a job in seoul 1](https://cloud.githubusercontent.com/assets/16644017/20456083/31a1fc48-aeb0-11e6-9fd4-25e969c655d1.png)

