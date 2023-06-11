This repository consists of the code and datasets used for writing "Language-Agnostic Detection of Current Events across Wikipedia" work.

The datasets for English, German, and Polish are located in the "data" folder.
Final models in pickle format are stored in the "models" folder. 

All models are created and evaluated in the "modeling" folder (using data from "data" and models from the "models" folders).
Data analysis is stored in the "analysis" folder (using data from the "data" folder).

Queries used to collect data from Quarry (https://quarry.wmcloud.org/) are stored in "quarry.docx".

The data collection code can be found in the "data_colection" folder. There we present all functions used for the data collection.
The events collection can be reproduced by notebooks "get_events_{lang}.ipynb".
For the full dataset generation, one should collect events as described in "get_events_{lang}.ipynb", and request data about pages from Quarry (query is in "quarry.docx"). Then, for events follow the logic in "get_events_features_ge.ipynb"; for pages follow "get_pages_features_ge.ipynb". The way to merge datasets is described in "join_dfs_ge.ipynb".
Several remarks here:
- we share the data collection for the German language only, but for others, the process is the same (make sure to change a language parameter, if API uses one)
- we shared data for pages without and with events separately, following the same process, with the only difference being that for pages we requested revisions features from Quarry to speed up the process. We additionally checked that data from Quarry and MediaWiki REST API "Get page history counts" is the same.

Additional data, such as more events features (that we did not use, but collected, train/test split) can be found at https://drive.google.com/drive/folders/118klLVhF-mWtjLsFODzpZhnATHtUxnth?usp=sharing.
Additional information can be requested via email [antypovaalice@gmail.com].
