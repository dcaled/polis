# PoliS dataset
This project provides the metadata and the crawlers to download the PoliS dataset's texts. 

Danielle Caled and Mário J. Silva. 2021. A transfer learning analysis of political leaning classification in cross-domain content. In Proceedings of the International Conference on Computational Processing of Portuguese, 2022.


## Dataset content

### Congressional Speeches
The congressional speeches dataset contains the transcripts of political speeches held in the [Brazilian Chamber of Deputies](https://www2.camara.leg.br/atividade-legislativa/) from January 1, 2018 to February 2, 2020.

#### Political party labels
- 25 Political parties, including `AVANTE`, `CIDADANIA`, `DEM`, `MDB`, `NOVO`, `PATRIOTA`, `PCDOB`, `PDT`, `PL`, `PMN`, `PODE`, `PP`, `PROS`, `PSB`, `PSC`, `PSD`, `PSDB`, `PSL`, `PSOL`, `PT`, `PTB`, `PV`, `REDE`, `REPUBLICANOS`, `SOLIDARIEDADE`.
- Number of speeches: 31,101.

#### Political leaning labels:

| Leaning    | Political Parties | # Speeches |
| ---------- | ----------------- |----------- |
| Right (R)  | 11                | 11,238     |
| Left (L)   | 8                 | 15,731     |
| Unlabeled  | 6                 | 4,132      |


### Social media messages

The social media dataset was assembled by scraping a set of Twitter posts published by Brazilian political figures whose political leaning is known. To this end, we crawled
posts from 389 Twitter profiles (144 left-aligned and 245 right-aligned) belonging to federal deputies active during 2020. The collection period ranged from January 1, 2018 to December 31, 2020.


| Leaning   | Federal deputies | # Posts  |
| ----------| ---------------- |--------- |
| Right (R) | 69               | 212,539  |
| Left (L)  | 88               | 334,312  |

**Disclaimer** PoliS's social media posts are provided through Twitter URLs. To obtain the tweets comprising this dataset, please use Twitter scraper tools.
Since Twitter profiles and posts are dynamic, their content may not be available or may be updated at the time of download.


## Dataset structure description:

- `federal_deputies_twitter.xslx`: The list of Twitter accounts compiled by the non-profit organization [Auditoria Cidadã da Dívida](https://auditoriacidada.org.br/contato-dos-deputados-federais-2020-twitter/).
- `political_party_leaning_decision_matrix.xlsx`: Matrix comparing [sources](#sources) labeling for estimating the political leaning of Brazilian parties.
- `congressional_speeches` folder: Contains all the transcribed speeches and their corresponding metadata (i.e., speaker name, political party, federated state of the speaker,
date, plenary session, summary, and URL).
- `twitter_metadata` folder: Contains the social media metadata for each message published by the selected Federal Deputies active in Twitter, i.e., username, political party, political leaning, message timestamp, and message URL.


## <a name="sources"></a>Sources used to infer the political leaning of Brazilian parties:
- [O Globo](https://blogs.oglobo.globo.com/na-base-dos-dados/post/maioria-dos-partidos-se-posiciona-como-de-centro-veja-quem-sobra-no-campo-da-direita-e-da-esquerda.html)
- [BBC](https://www.bbc.com/portuguese/brasil-41058120)
- [Congresso em Foco](https://congressoemfoco.uol.com.br/legislativo/direita-cresce-e-engole-o-centro-no-congresso-mais-fragmentado-da-historia/)
- [Wikipedia](https://en.wikipedia.org/wiki/List_of_political_parties_in_Brazil)
