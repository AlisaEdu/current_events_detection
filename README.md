# current_events_detection

This repository consist of the code and datasets used for writing "Language-Agnostic detection of Current Events across Wikipedia" work.

The datasets for English, German and Polish are located in the "data" folder.
Final models in pickle format are stored in the "models" folder. 

All models are created and evaluated in "modeling" folder (using data from "data" and models from "models" folders).
Data analysis is stored in "analysis" folder (using data from "data" folder).

Querries used to collect data from Quarry (https://quarry.wmcloud.org/) are stored in "quarry.docx".

The data colletion code can be found in "data_colection" folder. There we present all functions used for the data colection.
The events collection can be reproduced by notebooks "get_events_{lang}.ipynb".
For the full dataset generation, one should collect events as described in "get_events_{lang}.ipynb", and request data about pages from Quarry (querries are in "quarry.docx"), then append pages from those two sources, adding labels if a page is an event, or not. Then add revisions data (described in "get_revisions_features.ipynb"), views data (described in "get_views_features.ipynb") and topics data (described in "topic_features.ipynb"). An example of merging it all together is in "general dataset.ipynb".

Additional data, such as more events features (that we did not use, but collected, train/test split) can be found at https://drive.google.com/drive/folders/118klLVhF-mWtjLsFODzpZhnATHtUxnth?usp=sharing.
Additional code that was used for putting the whole dataset together and for analysis that we did not cover at "Language-Agnostic detection of Current Events across Wikipedia" can be requested via email [antypovaalice@gmail.com].



