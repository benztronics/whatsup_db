couchdb -c for local.ini location
To change database location add the following under [couchdb]

database_dir = /home/b/whatsup_db/
view_index_dir = /home/b/whatsup_db/

obviously change to your directory

Ideas for DB:

type : venue
  name : input
  address1 : input
  address2 : input
  city : input
  state : input
  hashtag : input
  website : input

type : artist
  name : input
  info : input
  website : input
  hashtag : input

type : region
  name : input
  {This will be used to control expansion sites}

type : agegroup
  name : input

type : crawler
  site : input
  tag : (list input)

type : event    #brings it all together
  venue : {venue ID}
  artist : {artist ID}
  agegroup : {agegroupID}
  region : {region ID}
  startTime : DTIME
  endtime : DTIME
  price : input
  hashtag : input


