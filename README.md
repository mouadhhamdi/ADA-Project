## Title: Study of the Biggest Leak in History
#### Abstract:

The Panama Papers involved hundred thousands of offshore accounts, millions of documents detailing top secret financial information were leaked in 2015 by an anonymous source. It is estimated that tax havens cost poor countries at least $170 billion in lost tax revenues each year making poorest people lose out and the inequality gap grow. Holding money in an offshore company is generally not illegal but it can be used to launder money, dodge sanctions, avoid taxes. Many people listed in the panama papers claimed being innocent. There is a huge amount of data, our work will be to provide a detailed analysis of the dataset. We will not focus our analysis on individuals but we will instead  be getting a closer view about the involved countries and the distribution of the papers  around the world and trying to find any correlation between the implication of each country in the panama papers with other finacial studies such as Financial secrecy index, Corruption ... and with any other interesting information we could get about those countries. 


#### Researchs questions: 
- What are the top countries that have the most number of relationship with suspicous intermediaries? 
- what is the distribution of officers, entities and intermediaries around the world? It is based in specified countries or it is overspreaded? 
- Can we relate our rankings to other world known indicators? 
- What is the effect of suspecious investments on some countries? (Espcially top Tax havens)
- Does Mossack Fonseca have connections with entities (intermediary companies, clients, beneficiaries and shareholders) based in countries which had a high degree of illicit outflows?
#### Dataset:
- Panama papers

Unfortunately, we don't have access to big part of the data and metadata from the original leaks so we decided to enrich our data with other similar datasets found in ICIJ (The International Consortium of Investigative Journalists):
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
    We will add to Panama papers Bahamas Papers, Paradise papers and offshore papers to have more entries.                         Searching for other datasets related to financial statistics and corruption around the world: 
    - CPI: Courrption Perception Index
    - FSI: Financial Secrecy Index
    - AML: Anti Money Laundring 
- Cleaning data: 
    - Concatenate entries from Panama papers, Bahamas Papers, Paradise papers and offshore papers and try to have 4 clean datasets related to entities, officers, intermediaires and edges. 
      
    - Add new columns, if needed, to identify the natures of each node {entity, addresse, intermediary, officer}.
    
    - Since our analysis will focus on countries, match node id's to the their country name. 
    
    - Country names needed to be cleaned, some rows contains multiple names of countries. An expansion of rows would be a good idea. 
      
    - Finally, save the cleaned dataframes in a new folder to use them for data wrangling and exploitation.
    
- Data wrangling: 
    To get more familiar with our data, some plots should be used to have an idea about the different aspects of our datasets: 
    - Plot the counts of entities, officers and intermediairies per each country in a stacked format.
    
    - Active intermediaries are also interresting. A plot may help us understand how the network was connected at the last time snapshot.
      
    - The evolution over time of the entities is also important to be visualised. It shows us when does this suspicious 
     activity has grown in time.
     
     - A folluim map with entities, intermediares and officers country counts is shows to highlight the distribution of the network on a world map.

  
- Network Analysis: 
  - A graph created with the name of the country as the indentifiant of the node.
  
  - The Degree Centrality algorithm is employed to see the importance of the nodes of the graph which in our case
  are countries.
  
  - The Page Rank algorith is also used to check the importance of countries based on the incoming link which will 
  help identify the countries with most important numbers of entities, intermediaries and officers.
  
  - A second graph is created, this time with the node_id as the identifiant of the node. This graph will be used to 
  help us discover hidden links between countries for example: if there is a country that do suspicious activities using an     other entity that it controles in an other country.
  

At the end of this milestone we have found those statistics:
  - Ranks countries accourding to several number of classes e.g:
  - The top countries that have the most number of links with Mossacka Fonseca and other suspicous law firms.
  - The top countries that are considered as tax havens.
  - The most connected countries in the graph.
  
#### Internal milestones up until milestone 3:

- Try to see if the rankings we could provide up to milestone 2 are coherent with world statistics.
- Collect other usefull data about the situation of some countries. Growth index,income gini index, financial situation, Education ..
- Select Top Tax havens and top countries with bank secrecy and highlight the effect on both side of the story.

#### Run the code:

To be able to run the code you need to unzip the compressed files:
    - big_data_to_compress.tar.gz
    - data_cleaned.tar.gz
    - data_follium.tar.gz

#### Resources:
www.gfintegrity.org illicit financial flows from developing countries.
https://www.financialsecrecyindex.com/ financial secrecy index
https://www.transparency.org/research/cpi/overview corruption perception index
