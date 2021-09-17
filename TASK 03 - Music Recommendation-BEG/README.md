## Data Description

In this task, you will be asked to predict the chances of a user listening to a song repetitively after the first observable listening event within a time window was triggered. If there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, its target is marked 1, and 0 otherwise in the training set. The same rule applies to the testing set.KKBOX provides a training data set consists of information of the first observable listening event for each unique user-song pair within a specific time duration. Metadata of each unique user and song pair is also provided. The use of public data to increase the level of accuracy of your prediction is encouraged.
The train and the test data are selected from users listening history in a given time period. Note that this time period is chosen to be before the WSDM-KKBox Churn Prediction time period. The train and test sets are split based on time, and the split of public/private are based on unique user/song pairs.

### train.csv

msno: user id
song_id: song id
source_system_tab: the name of the tab where the event was triggered. System tabs are used to categorize KKBOX mobile apps functions. For example, tab my library contains functions to manipulate the local storage, and tab search contains functions relating to search.
source_screen_name: name of the layout a user sees.
source_type: an entry point a user first plays music on mobile apps. An entry point could be album, online-playlist, song .. etc.
target: this is the target variable. target=1 means there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, target=0 otherwise .

### test.csv

id: row id (will be used for submission)
msno: user id
song_id: song id
source_system_tab: the name of the tab where the event was triggered. System tabs are used to categorize KKBOX mobile apps functions. For example, tab my library contains functions to manipulate the local storage, and tab search contains functions relating to search.
source_screen_name: name of the layout a user sees.
source_type: an entry point a user first plays music on mobile apps. An entry point could be album, online-playlist, song .. etc.

### sample_submission.csv
sample submission file in the format that we expect you to submit

id: same as id in test.csv

### target: this is the target variable. target=1 means there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, target=0 otherwise .

### songs.csv
The songs. Note that data is in unicode.

song_id
song_length: in ms
genre_ids: genre category. Some songs have multiple genres and they are separated by |
artist_name
composer
lyricist
language
members.csv
user information.

msno
city
bd: age. Note: this column has outlier values, please use your judgement.
gender
registered_via: registration method
registration_init_time: format %Y%m%d
expiration_date: format %Y%m%d
song_extra_info.csv
song_id
song name - the name of the song.
