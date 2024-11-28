# Telegram_data_collection_and_analysis
Combination of tools a ready-made tools and solutions for collecting your own data from telegram and some functions for their further analysis

## Structure
### Instructions for data collection
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

##### 3_eda.ipynb
You can use functions from this notebook to visualize your own data

##### 3_eda.pdf
Compilation of 3_eda.ipynb to PDF
