# ada-2021-project-ada-venturers

# Please Act ! (Politicians Lie Everytime About Subjects on the Environment, Acknowledge Climate Transformation !)

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
First, we need to perform filtering of the data. We chose to remove the quotes that do not have a speaker. The first critical task for our project is to identify the quotes about climate change. To this end, we selected some specific keywords related to climate change and picked all the quotes containing them. Other methods like Word2Vec or Doc2Vec were not convincing: they were taking a lot of quotes that are not directly related to climate change.
The first analysis is a temporal analysis. Is there any relation between how much people talk and the events happening? We will visualize the quotes in time. This would show us if there are moments where this subject appears more. We will attempt to correlate it with campaign dates and extreme climate events (wildfires) to see if there are any trends.
Then, we want to find how people talk about climate change, what words are they using to talk about it. We perform a topic analysis with an LDA (Latent Dirichlet Allocation). The idea is to split these quotes by the stance held and extract different opinions. We obtain categories and try to find the topic, what relates those quotes. For example, there are quotes that are alarmist, some are about actions, some may be pessimistic, some may be about conspiracy… Once we get words into meaningful categories, we want to relate political party and how they talk about climate change, see if there is any trend.
Also, we want to see how much these words were used in quotes about global warming. For example, we could see how many times the word ‘crisis’ is used in the quotes previously selected about global warming. We can then see if a political party uses it more than the other.
Since we have the dataset with information about the speakers, we would use it to perform a crossed analysis with the quotes extracted. We could see who the most active speakers on the subject are. 
Finally, we will see if words go with actions taken against global warming. By taking the governors and the senators of the different states, we can then relate the quotes to a specific state. We use here the dataset on the CO2 emissions and the environmental index. This allow us to see if indeed, politicians that are in the action/alarmist mode indeed act as they preach.
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

