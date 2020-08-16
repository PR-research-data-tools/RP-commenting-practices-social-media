# RP-commenting-practices-social-media
Replication package for the paper "What do Developers Discuss about Code Comment Conventions on Social Media?"

## Structure
```
Paper-presenation.pdf

Makar_tool/
    Data/
    	stackoverfow_questions_with_answers_by_tags.csv
    	stackoverfow_tags_metrics.csv
    	apache_mailing_list.csv
    	mailing_lists_ASF_@dev_@users_1.csv
    	mailing_lists_ASF_@dev_@users_2.csv
    	quora.csv
    	sample_stackoverfow_questions_with_answers_by_tags.csv
    Schemas/
    	apache_mailing_lists.json
    	quora.json
    	stackoverfow_questions_answers_by_tag.json
    	stackoverfow_tag_count.json
    	stackoverfow_tag_metrics.json

RQ1/
    LDA_input/
        stackoverfow_raw_dataset.csv

    LDA_output/
    	Mallet/
    		output_csv/
    			docs-in-topics.csv
    			topic-words.csv
    			topics-in-docs.csv
    			topics-metadata.csv
    		output_html/
    			all_topics.html
    			Docs/
    			Topics/

RQ2/
   datasource_rawdata/
   		mailing_lists_selection_criteria.csv
    	quora.csv
    	stackoverflow.csv
    manual_analysis_output/
    	stackoverflow_quora_taxonomy.xlsx
```

## Contents of the Replication Package
---
**Paper-presenation.pdf** presents the highlights of the work in a presenation. 

**Makar_tool/** contains the data processed using the tool for the study
- **Data/**
     - `stackoverfow_questions_with_answers_by_tags.csv` - all stackoverflow questions used in the study as stored in Makar
    - `stackoverfow_tags_metrics.csv` - all data containing the calculations done for stackoverflow tag selection
    - `apache_mailing_list.csv` - statistically significant sample of `mailing_lists_ASF_@dev_@users_1.csv` and `mailing_lists_ASF_@dev_@users_2.csv` used in the study
    - `mailing_lists_ASF_@dev_@users_1.csv` - mailing list data used in the study as stored in Makar (part 1)
    - `mailing_lists_ASF_@dev_@users_2.csv` - mailing list data used in the study as stored in Makar (part 2)
    - `quora.csv` - all quora questions used in the study as stored in Makar
    - `sample_stackoverfow_questions_with_answers_by_tags` - statistically significant sample of `stackoverfow_questions_with_answers_by_tags.csv` used in the study

- **Schemas/**
    - `apache_mailing_lists.json` - data schema used in Makar to store mailing list data
    - `quora.json` - data schema used in Makar to store quora data
    - `stackoverfow_questions_answers_by_tag.json` - data schema used in Makar to store stackoverflow questions data
    - `stackoverfow_tag_count.json` - data schema used in Makar to lookup number of questions per tag available in stackoverflow
    - `stackoverfow_tag_metrics.json` - data schema used in Makar to stackoverflow tag metrics data

- **RQ1/** - contains the data used to answer RQ1
 - **LDA_input/** - input data used for LDA analysis
    - `stackoverfow_raw_dataset.csv` - stackoverflow questions used to perform LDA analysis
 - **LDA_output/**
    - **Mallet/**
         - **output_csv/**
            - `docs-in-topics.csv` - documents per topic
            - `topic-words.csv` - most relevant topic words
            - `topics-in-docs.csv` - topic probability per document
            - `topics-metadata.csv` - metadata per document and topic probability
        - **output_html/** - Browsable results of mallet output
            - `all_topics.html`
            - `Docs/`
            - `Topics/`

- **RQ2/** - contains the data used to answer RQ2
  - **datasource_rawdata/** - contains the raw data for each source
    - `mailing_lists_selection_criteria.csv` - criteria used to select mailing_lists.
    - `quora.csv` - contains the processed dataset
    - `stackoverflow.csv` - contains the processed stackoverflow dataset
  - **manual_analysis_output/**
    - `stackoverflow_quora_taxonomy.xlsx` - contains the classified dataset of stackoverflow and quora and description of taxonomy.
        - `Taxonomy` - contains the description of the first dimension and second dimension categories. Second dimension categories are further divided into levels, separated by `|` symbol. 
        - `stackoverflow-posts` - the questions are labelled relevant or irrelevant and categorized into the first dimension and second dimension categories.
         - `quota-posts` - the questions are labelled relevant or irrelevant and categorized into the first dimension and second dimension categories.         
---
