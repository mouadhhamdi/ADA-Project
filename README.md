## Title: Study of the Biggest Leak in History
#### Abstract:

The Panama Papers involved hundred thousands of offshore accounts, millions of documents detailing top secret financial information were leaked in 2015 by an anonymous source. It is estimated that tax havens cost poor countries at least $170 billion in lost tax revenues each year making poorest people lose out and the inequality gap grow. Holding money in an offshore company is generally not illegal but it can be used to launder money, dodge sanctions, avoid taxes. Many people listed in the panama papers claimed being innocent. There is a huge amount of data, our work will be to provide a detailed analysis of the dataset. We will not focus our analysis on individuals but we will instead  be getting a closer view about the involved countries and the distribution of the papers  around the world and trying to find any correlation between the implication of each country in the panama papers with other finacial studies such as Financial secrecy index, Corruption ...... and with any other interesting information we could get about those countries. As a second part we will be able to see how this can be related to wold inequalities and its affect on (Seect a country? or two most linked countries?)...?.  

#### Researchs questions: 
- What are the top countries that have the most number of relations with suspicous intermediaries? 
- what is the distribution of different of officers, entities and intermediaries around the world?
- Can we relate our rankings to other world known statistics? 
- What is the effect of those claimed to be legal investments on some countries? (Top 1 Tax havens and top 1 country with suspicous investmens?)
- Does Mossack Fonseca have connections with entities (intermediary companies, clients, beneficiaries and shareholders) based in countries which had a high degree of illicit outflows?
#### Dataset:
- Panama papers

Unfortunately, we don't have access to big part of the data and metadata from the original leaks so we decided to enrich our data with other similar datasets:
    - Paradise papers
    - Offshore leaks
    - Bahamas leaks
    
The hybrid dataset is composed of four parts: 

    * Entities: is a company, trust or fund created in a low tax offshore jurisdiction.
    * Officers: a person or a company who plays role in an offshore entity.
    * Intermediairies: the link between someone seeking an offshore and an offshore service provider.
    * Addresses: description of the addresses contained in the dataset.
    * Edges: they connect nodes from the above parts and describe the nature of the relation between them, 
      it's has three important features 'registered address', 'beneficiary of' and 'intermediary of'.
     
#### Internal milestones up until milestone 2:
- Data collection:
    We will add to Panama papers Bahamas Papers, Paradise papers and offshore papers to have more entries.                         Searching for other datasets related to financial statistics and corruption around the world: CPI- Courrption perception index
    FSI : Financial secrecy index, AML: Anti Money Laundring. 
- Cleaning data: 
    - We concatinated entries from above datasets, to do so we modified some feature names in order to to have the same
      columns names 
      
    - We also added new columns to identify the natures of each node {entity, addresse, intermediary, officer}
    
    - Since our analysis will focus on countries, we matched node id's to the their country name 
    
    - Country names needed to be cleaned, some rows contains multiple names of countries so we have an expansion of rows
        according to ';' character. From this, we alsoo created a Json file that will be used for follium visualisation.
      
    - Finally, we saved our cleaned dataframes in a new folder to use them later for data wrangling.
    
- Data wrangling: 
    At this point of the project we needed to get more familiar with our data so we decided to do some plots:
    - We plotted the counts of entities, officers and intermediairies per each country in a stacked format.
    - We where also interrested in the number of active intermediaries which will help us to understand how the 
      network was connected at the last time snapshot.
    - The evolution over time of the entities was important to be visualised. We could've seen that this suspicious 
     activity has grown exponentially at the end of nineties.
  
- Network Analysis: 
  model our dataset in a graph format and learn about the nodes connections(example: connected components) 
At the end of this milestone we should find those statistics:
- Ranks countries accourding to several number of classes e.g:
  - The top countries that have the most number of links with Mossacka Fonseca and other suspicous law firms.
  - The top countries that are considered as tax havens.
  - The most connected countries in the graph.
  -
- Visualize the distribution of those numbers around the world 
#### Internal milestones up until milestone 3:

- Try to see if the rankings we could provide up to milestone 2 are coherent with world statistics.
- Collect other usefull data about the situation of some countries. Growth index,income gini index, financial situation, Education ..
- Select Top 1 Tax havens and top 1 country with suspicous investmens and highlight the effect on both side of the story.

#### Resources:
ADD links
www.gfintegrity.org illicit financial flows from developing countries.
