# Telegram_data_collection_and_analysis
Combination of tools a ready-made tools and solutions for collecting your own data from telegram and some functions for their further analysis

## Structure
### Instructions for data collection
#### Installation instructions:
Clone this repo to your folder:
```git clone https://github.com/Antony925/Telegram_data_collection_and_analysis```

#### Function descriptions:
##### 0_download_dialogs_list.py
Downloads dialogs meta data for account.

`--dialogs_limit` - means number of dialogs (-1 means all of your dialogs)

`-h` - show this help message and exit

`--config_path` - path to your config file ()

`--debug_mode` - Debug mode


##### 0_download_dialogs_list_by_folder.py
Downloads dialogs meta data for account 

`-1` - skips all chats, groups and channels, which had been archived in your telegram


##### 1_download_dialogs_data.py
Downloads all messages from the dialogs.

`--dialog_msg_limit` means number of messages in dialogs (-1 means all of your dialogs)

Use flags `--skip_private`, `--skip_groups`, and `--skip_channels`
to skip private chats, groups, and channels respectively.


### Requirements
Python 3.8.13


### How to run
0. Open your command prompt as administrator and input furher commands
1. create virtual env
```python -m venv .venv```
2. activate virtual env
```. "path_to_dir"/venv/Scripts/activate```
3. install dependencies 
```pip install -r requirements.txt```
4. get your credentials https://my.telegram.org/apps
5. set credentials (api_id, api_hash) in *config/example.json* (and rename to *config.json*)

### How to start
0. Download dialogs meta data ```python 0_download_dialogs_list.py --dialogs_limit -1```
1. Download messages from dialogs ```python 1_download_dialogs_data.py --dialogs_ids -1 --dialog_msg_limit -1```


### Instructions for data analysis
To run the notebook please install following libraries:

```%pip install pandas matplotlib numpy seaborn plotly scikit-learn networkx nltk```

And launch jupyter notebook:

```jupyter notebook```

Import all libraries and dependensis:

Merge all data in one .csv file:
![image](https://github.com/user-attachments/assets/64dcb1de-9ad0-4992-add7-5b687711b18c)

Set your own path to file with merged data and read it:
![image](https://github.com/user-attachments/assets/159945bf-0033-454a-a7e5-00b9e17df958)


### My own final CSS report
The goal was to analyze russian propaganda dataset from different sides
##### Morhun_final_report.ipynb
Functions and visualisations of graphs (You can reuse this notebook to visualize your own data)

##### Morhun_final_report.pdf
Compilation of 3_eda.ipynb to PDF
