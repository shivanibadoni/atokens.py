# atokens.py
#q1
#answer 1 : Access tokens are the thing that applications use to make API requests
#on behalf of a user.The access token represents the authorization of a specific
# application to access specific parts of a user's data.
#An access token is a unique string of letters and numbers that we pass with every
#API call.Each access token is associated with:
#-API application.
#-The user we are acting on behalf of(for merchants,etc).
#-The permissions our app has for that user.

#Q2
import socket
addr1=socket.gethostbyname('www.google.com')
addr2=socket.gethostbyname('www.facebook.com')
print("IP Address of google.com:%s\nIP Address of facebook.com:%s"%(addr1,addr2))

#Q3
import tweepy
import textblob
#The actual keys and secrets aren't shared for the obvious reasons here
consumer_key="tRON4gxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
consumer_secret="8qvl96Rkvxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
access_key="861540811514xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
access_secret="1BtebIELkbxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
auth=tweepy.OAuthHandler(consumer_key,consumer_secret)
api=tweepy.API(auth)

#Q4
#Library
#-A library is a collection of code built to perform common tasks |
#-API is a part of library which defines how an application communicates with external code|
#-Library is written in same language which in which it is used |
#-API can be written in any language
#-Library code tends to be relatively stable and bug free.|
#-APIs should be defined before the code implementing them is implemented.
#-Use of appropriate libraries can reduce the amount of code the need to be |
#-APIs should be stable ,although portions of the API can be deprecated written.It
#will tend to reduce line of code counts for an application|
#-The more broadly used the API the more difficult it is to change it.will
#increasing the rate at which functionality is delievered . |
#-e.g. Google Maps API for Spotify -e.g. Numpy is a library of Python for matrices
#-&mathematical handling, |
#-math is a library to handle numberal operations |


#Q5

import spotify
katyperry_uri='spotify:artist:6jJOs89eD6GaHleKKya26X'
spotify=spotify.Spotify()
results=spotify.artist_albums(katyperry_uri,album_type='album')
albums=results['items']
while results['next']:results=spotify.next(results)
albums.extend(results['items'])
for album in albums:print((album['name']))
