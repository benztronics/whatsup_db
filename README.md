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
  gps_n : Northern GPS boundary
  gps_s : Southern GPS boundary
  gps_e : Eastern GPS boundary
  gps_w : Western GPS boundary
  {This will be used to control expansion sites}

type : agegroup
  name : input

type : crawler    #for adding new sites to seach and tags to search on
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
  media : {link}  #maybe a photo of event poster... it'd be cool if we could auto populate from the poster

type : Approver
  name : input
  email : input
  pushID : input  #some kind of device address that pings for approvals
  region : (regionID, list,)
