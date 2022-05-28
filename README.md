## Telegram groups Recommender System

### Description 

In this notebooks you can find the implementation of a Recommender System for users and Telegram groups of [Network StudentiUniMi](https://github.com/StudentiUniMi).

### Methods

There are three main notebooks. 

1. [`dataset.ipynb`](https://github.com/StudentiUniMi/recommender-system/tree/master/dataset.ipynb): computation of some statistics that give a better insight into dataset we are working with.
2. [`contentbased.ipynb`](https://github.com/StudentiUniMi/recommender-system/tree/master/contentbased.ipynb): implementation of a Content Based Recommender System, using a vectorial representation of users and groups to compute their similarity.
3. [`graph.ipynb`](https://github.com/StudentiUniMi/recommender-system/tree/master/graph.ipynb): implementation of a Recommender System using random walks on the graph of users and groups, also expanding on the method used in 2.

### Running

The data to run the notebooks cannot be published for privacy reasons (the visible data are personal ones or from people to whom was asked the permission to publish), but to get the same working environment you just have to run:

```bash
$ virtualenv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

### Dataset

The data come from the relational database of Network StudentiUniMi, from which  the following tables (and columns of interests) are extracted.

- Groups database: 

|id|title|
|-|-|
|int|string|

- Groups description database:

|id|year|semester|degree_id|
|-|-|-|-|
|int|(1,2,..,6,7)|(1,2,3)|(1,..,158)|
  
- User database:

|id|first_name|last_name|username|
|-|-|-|-|
|int|string|string|string|

- Groups membership database:

|id|group_id|user_id|messages_count|status|
|-|-|-|-|-|
|int|int|int|int|('left', 'member')|

