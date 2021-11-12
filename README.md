# ada-2021-project-ada-venturers

# Please Act ! (Politicians Lie Everytime About Subjects on the Environment, Acknowledge Climate Transformation !)

Now more than ever, climate change is a very hotly debated topic which often comes up in the news. This year alone, the Intergovernmental Panel on Climate Change and World Meteorological Organization released very alarming reports stating that we are "way behind" on the objectives of the Paris Agreement. While there will be some individual action involved if we are to tackle the climate crisis, laws and regulations passed by governments will be imperative to avoid the worst case scenario. Using the Quotebank dataset, we were interested to see whether climate change is used as a campaign promise by politicians or if it really is a subject that is constantly talked about. Furthermore, which political groups are the most involved in proposing solutions and spreading awareness about the pressing climate crisis that we are facing. More importantly: do they Act?


Research questions:
Who speaks the most about climate change? 
What is their position on the subject? Do politicians all have the same words and opinions on the subject ?
What factors affect this position? 
What are the periods when the subject is most highlighted, and at the heart of the debates ? Do voting periods have an impact?
Does speaking about the problem mean taking action?

Proposed additional datasets:
- speaker_attributes.parquetdataset 
- Dataset of events with dates such as campaign dates or extreme weather events. 
- Environmental indicators for countries: ‘Environmental Perfomance Index 2020 release’ https://sedac.ciesin.columbia.edu/data/collection/epi/sets/browse
- Environmental indicators for USA : https://www.governing.com/next/what-is-the-greenest-most-environmentally-friendly-state.html
https://247wallst.com/special-report/2020/04/22/americas-least-and-most-environmentally-friendly-states/11/

Methods:
First, we need to perform filtering of the data. We chose to remove the quotes that do not have a speaker. Then, we will remove those with less than 5 words once we dig into the analysis of their meaning.

The first critical task for our project is to identify the quotes about climate change. For the moment, we only use specific keywords to filter the data. The idea would be to optimize this task, and get an extended higher quality set of climate change related quotes. 

We first tried to use Word2Vec to create a corpus of the most similar words to our target, in order to enrich the keywords we search for. 
The corpus returned was incomplete and noisy. Moreover, we got words that were not strictly specific to climate change like 'crisis'. These weren't descriptive enough for our retrieval task. Also, 'climate change' counts for two words so we either need to only take 'climate' word as the query or choose to aggregate the two vectors of 'climate' and 'change'.

We then tried another method using Doc2Vec, which is based on Word2Vec. This gives us the quotes that have the similar meaning with the query input. We get results that seem more conclusive but we still get some incoherent quotes in the results. Furthermore, we didn't find a way to scale it for our very large data set. When chunking the data, we had to train it for every chunk which takes too long.
For now, we chose to stick with the naive retrieval method.

Once this is done, the idea would be to split these quotes by the stance held and extract different opinions. For example, there are quotes that are alarmist, some are about actions, some may be pessimistic, some may be about conspiracy… For this part we are still thinking about a way to categorize the stances. For example, the words ‘urgent’, ‘crisis’ and ‘emergency’ belong to the same lexical field and display a specific opinion on the topic. However, they were arbitrarily chosen by us. We should try to find a way to extract these words automatically. We could probably use the word2vec model. Another idea could be to use a topic model applied to global warming related quotes or perform sentiment analysis.

Once we get words into meaningful categories, we could also see how much these words were used in quotes about global warming. For example, we could see how many times the word ‘crisis’ is used in the quotes previously selected about global warming. We could then make statistics on specific words. For example, which political parties use which words the most... 

Since we have the dataset with information about the speakers, we would use it to perform a crossed analysis with the quotes extracted. We could see who are the most active speakers on the subject. We would then try to identify factors that affect the position of the speaker about climate change such as political party, gender, age, country, running for the elections, academic degree… and identify trends.

Then we will visualize the quotes in time. This would show us if there are moments where this subject appears more. We will attempt to correlate it with campaign dates and extreme climate events (wildfires) to see if there are any trends.

Finally, we will see if words go with actions taken against global warming. For that we may use a data set of "green" index for certain states/countries. This would allow us to see if indeed, politicians that are in the action/alarmist mode indeed act as they preach. 

Timeline:
- Optimization of quote selection using techniques from the course not seen yet
- Distinction of the opinion of speaker also using ML methods 
- Further analysis of the data: occurrence of climate change related quotes for each speaker, analysis according to attributes (gender, political party, country…), make time related analysis, correlate with campaign dates and weather disasters, analyse who uses which meaningful word (ex:‘crisis’), who has which opinion, correlation with environmental indicators of states/countries....
- Nice visualizations and putting results together in a coherent data story.


Organization within the team:
Arthur and Adam will continue to work onto the ML models: one to enrich our list of keywords and find more climate related quotes and another one to distinguish the opinions of the speakers. Elsa and Sandy will dig into the analysis and visualization.
