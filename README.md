# ada-2021-project-ada-venturers

# Please act ! (Politicians Lie Everytime About Subjects on the Environment, Acknowledge Climate Transformation !)

Now more than ever, climate change is a very hotly debated topic which often comes up in the news. This year alone, the Intergovernmental Panel on Climate Change and World Meteorological Organization released very alarming reports stating that we are "way behind" on the objectives of the Paris Agreement. While there will be some individual action involved if we are to tackle the climate crisis, laws and regulations passed by governments will be imperative to avoid the worst case scenario. Using the Quotebank dataset, we were interested to see whether climate change is used as a campaign promise by politicians or if it really is a subject that is constantly talked about. Furthermore, which political groups are the most involved in proposing solutions and spreading awareness about the pressing climate crisis that we are facing?


Research questions:
Who speaks the most about climate change? 
What is their position on the subject? Do politicians all have the same words and opinions on the subject ?
What factors affect this position? 
What are the periods when the subject is most highlighted, and at most at the heart of the debates ? Do voting periods have an impact?
Does speaking about the problem mean taking action?

Proposed additional datasets:
- speaker_attributes.parquetdataset 
- Data set of events with dates such as campaign dates or extreme weather events dates. 
- Environmental indicators for countries: ‘Environmental Perfomance Index 2020 release’ https://sedac.ciesin.columbia.edu/data/collection/epi/sets/browse
- Environmental indicators for USA : https://www.governing.com/next/what-is-the-greenest-most-environmentally-friendly-state.html
https://247wallst.com/special-report/2020/04/22/americas-least-and-most-environmentally-friendly-states/11/

Methods:
First, we need to perform filtering of the data. We chose to remove the quotes that do not have a speaker and quotes smaller than x words as these do not carry enough meaning for our analysis (last part not done yet).

The first task that is critical for our project is to identify the quotes about climate change. For the moment, we just use specific keywords to filter the data. The idea would be to optimize this task and get an extended high quality of climate change related quotes. 

Once this is done, the idea would be to split these quotes into positions and extract different opinions. For example, there are quotes that are alarmist, some are about actions, some could be pessimistic, some could be about conspiracy… For this part we are still thinking about a way to categorize the positions. For example, the words ‘urgent’, ‘crisis’, ‘emergency’ belong to the same category and show a specific opinion on the topic. However, they were arbitrarily enunciated by us. We should try to find a way to extract these words by ourselves. We could maybe use the word2vec model for that. Another idea could be to use a topic model applied to the dataframe of global warming related quotes or perform sentiment analysis.

Once we get meaningful words by categories, we could also see how much these specific words were used in the quotes about global warming. For example, we could see how many times the word ‘crisis’ is used in the quotes selected previously (it will only refer to quotes that we agreed to be related to global warming). We could then make statistics on these specific words, for example, which political parties use which words the most...

Since we have the dataset with information about the speakers, we would use it to perform a crossed analysis with the quotes extracted. We could see who are the most active speakers on the subject. We would then try to identify factors that affect the position of the speeches about climate change such as political party, gender, age, country, candidacy, academic degree… and identify trends.

Then we should visualize the quotes in time. This would show us if there are moments where this subject appears more. We would need to correlate it with campaign dates and extreme climate events (wildfire)  and see if there are any trends.

Finally, we could see if the words used go with the actions that are taken against global warming. For that we could use a data set of index of durability of a certain state/country. This would allow us to see if indeed, politicians that are in the action/alarmist mode indeed act as they say. 


