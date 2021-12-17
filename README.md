# ada-2021-project-ada-venturers

# Please Act ! (Politicians Lie Everytime About Subjects on the Environment, Acknowledge Climate Transformation !)

## Link the the Data Story:
https://arthurgardon.github.io/ada_please_act/#topic=5&lambda=1&term=

## Abstract:
Now more than ever, climate change is a very hotly debated topic which often comes up in the news. This year alone, the Intergovernmental Panel on Climate Change and World Meteorological Organization released very alarming reports stating that we are "way behind" on the objectives of the Paris Agreement. While there will be some individual action involved if we are to tackle the climate crisis, laws and regulations passed by governments will be imperative to avoid the worst case scenario. Using the Quotebank dataset, we were interested to see whether climate change is used as a campaign promise by politicians or if it really is a subject that is constantly talked about. Furthermore, which political groups are the most involved in proposing solutions and spreading awareness about the pressing climate crisis that we are facing. More importantly: do they Act?
## Research questions: 
Who speaks the most about climate change? What is their position on the subject? Do politicians all have the same words and opinions on the subject ? What factors affect this position? What are the periods when the subject is most highlighted, and at the heart of the debates ? Do voting periods have an impact? Does speaking about the problem mean taking action?
## Proposed additional datasets:
•	Informations about the speaker from the Wikidata knowledge base   
•	Dataset of events with dates such as campaign dates or extreme weather events.   
•	Dataset containing environmental index for each state: https://www.governing.com/next/what-is-the-greenest-most-environmentally-friendly-state.html   
•	Dataset containing the CO2 emission of each state: https://www.wri.org/data/climate-watch-historical-emissions-data-countries-us-states-unfccc'  
## Methods:
First, we need to perform filtering of the data. We choose to remove the quotes that do not have a speaker. The first critical task for our project is to identify the quotes about climate change. To this end, we select some specific keywords related to climate change and pick all the quotes containing them. Other methods like Word2Vec or Doc2Vec were not convincing: they were taking a lot of quotes that are not directly related to climate change. 

The first analysis is a temporal analysis. To see if there is any relation between how much people talk and the events happening, we visualize the quotes in time. This shows us if there are moments where this subject appears more. We attempt to correlate it with three categories of events:  political events (campaigns), extreme climate events (eg. wildfires) and governmental events (COPs).

Then, we would like to inspect how people talk about climate change and what words they are using to talk about it. We perform a topic analysis with an LDA (Latent Dirichlet Allocation). The idea is to split these quotes by the stance held and extract different opinions. We obtain categories and try to find the topic, what relates those quotes. For example, there are quotes that are alarmist, some are about actions, some may be pessimistic, some may be about conspiracy… Once we get words into meaningful categories, we want to relate political party and how they talk about climate change, see if there is any trend. 

After that, the idea is to visualize how the quotes about climate change are represented among the parties and then to see which proportion of the quotes contain meaningful words highlighted by the LDA. 

Then, we want to analyze how much each state speaks about climate change and if this can be related to their behaviour and political choices against global warming. By taking representative speakers the different states, we can relate the quotes to a specific state. To get an idea of a state's behavior when it comes to climate change, we use the dataset on the CO2 emissions and the one with environmental scores. This would allow us to see if indeed, states that speak a lot about climate change indeed act as they preach.

## Timeline: (from M2)
•	Optimization of quote selection using techniques from the course not seen yet
•	Distinction of the opinion of speaker also using ML methods
•	Further analysis of the data: occurrence of climate change related quotes for each speaker, analysis according to attributes (gender, political party, country…), make time related analysis, correlate with campaign dates and weather disasters, analyse who uses which meaningful word (ex:‘crisis’), who has which opinion, correlation with environmental indicators of states/countries....
•	Nice visualizations and putting results together in a coherent data story.
## Organization within the team: 
Arthur: Timeline plot, GitHub Website
Adam: LDA, GitHub Website
Elsa: Political analysis, maps and plots
Sandy: Data Cleaning, Preliminary analysis


