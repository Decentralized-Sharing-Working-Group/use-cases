# Services sharing - device2device - system sharing

## I can use my personal server to *synchronize files* between my devices

## I can use my personal server to *synchronize domain-specific files*

For instance: synchronize addressbooks, calendars, todo lists, photo
albums. This requires compatible data formats and probably also smarter
conflict resolution.

## Context adaptation

From my laptop I shared photos on a desktop client, synchronized with
my personal server. My photos are quite heavy with a high resolution.
My smartphone is synchronized as well with the photos, but I only
receive the shared photo in a smaller resolution, to save disk space
and bandwith.

# Person sharing - Person2Person

## Write

### Public - Share something publicly with one or more contacts

 - Create some public content (e.g. a file or a blog post)
 - Select one or more people to share the content with, e.g. from my
address book
 - Each person gets a notification that the content has been shared with
them on their own system

### Private - Share something privately with one or more contacts

 - Create some private content (e.g. a file or a blog post)
 - Select one or more people to share the content with, e.g. from my
address book
 - Each person gets a notification that the content has been shared with
them on their own system
 - Each person may see the content securely without having to create an
account on the content owner's system or log in again
 - Nobody else can see the content

## Interaction

### Interact with third-party content

 - Everyone who can see the content can comment on it and participate in
   a discussion with each other
 - Their identity (name and avatar) is drawn from their own self-hosted
   profiles
 - They receive notifications on their own systems when the conversation
   is added to
 - Content can also be marked as *starred* or *reshared *by a user
 - Custom annotations like *vote-up* and *vote-down* could be possible

### User tagging

I can include a reference to a user in a post. If I syndicate that
post to Twitter, the reference will be turned into a Twitter handle.
 - If I syndicate that post to Facebook, the reference will be turned
into a username reference.

## real-time

### personal server context

If two people both have a personal server, then there are probably
several options for this. Sometimes the medium you choose signals the
urgency.

### See if someone is online / what they're up to.

### Messaging/Voice sharing

Instant messaging or VoIP are a kind of sharing, and would be
definitively interesting : start a chat in an unhosted app and receive
it in your Cozy, or get notifications for a missed call.

## Read - Stream

### Get the latest updates

 - See all my friends' updates in a single, unified stream of content on
my site
 - Some of those updates may be privacy-restricted and shown only to me
or a limited audience - but they display in-line like the other content
posts
 - I can interact with all of them right there from my stream

### Cure content

 - By Importance: Important, Mentionned, Broadcast news, Hotness based
on comment, reshare, likes...
 - Aggregate By author: if you follow on different medium, should be merged
 - By News: When there is a news, I want to know it one time. People I
follow will comment on this news. And the more comment, the hotter the
news is
 - to prioritize: your reader shows you content, and notifies you about
content, in a way that depends on the importance of that content.
 - to manage: to store in an organized way for future reference, so you
can easily find it back.

# UX - Person2system

## Global search

I own several decentralized instances (remote storage, known, cozy...),
and I want to find a data, wherever it is.
From a search bar, I type my keywords, and a distributed query will
search for results and return it.
With this global search, I will be able to use all my personal data
without asking to myself "where is this file? On unhosted or cozy.. ?".
And this will be a true interoperable system.

## Share content from another system

 - A piece of content (e.g. a file) may be selected from a content
stream or file folder that the user has access to
 - It may be shared and/or interacted with as described above
 - Those interactions may be displayed next to the content on its
   original platform

## Contact management

### Add someone to a contact list

 - add a public profil to a centralized address book
 - Their various profile URLs and other details are automatically read
and saved to my address book
 - It is synchronised

### discovery - Contact someone with whom I'm not friends yet

When I want to share something with someone I don't have in my contact,
I would like to be able to perform a global search to find his personal
page, wherever it is hosted. For example, if I want to share documents
with Ben but I don't have any reference (url, uuid, ...). A global
search would give me an info (URL, email...) to easily ask Ben to be one
of my contact. If he accepts, I then can send him the documents (request
and sending of docs can be a single step).

Usually: search engine + contact details on their home page. This UX
could be made a lot better, faster to use, and more productive. Unless
you know someone's domain name, then finding someone on facebook is
easier than finding someone who has a personal server, because its
search box can use bias to location, and to friends-in-common. This is
one I definitely want to work on myself at some point. (Michiel)

## Calendar

### ID

When a meeting is organised people participating in the meeting can be
identified using their WebID. This WebID allows software agents to fetch
information from their profile - whatever organisation this belongs to -
and display a small info box containing picture, name, blog, telephone
number, email, skype address etc… (whatever is relevant) to someone who
wishes to know more about who is attending. This allows one to organise
cross institutional meetings as if they were intra-organisational ones.

### Sharing

Each actor’s calendaring information could be made available without
divulging the details of what is taking place to specific groups of
actors in order to facilitate automatic meeting organisation. (Instead
of Doodling suitable times and several reminders, it can be deducted
half automatically from participants’ calendars or from the available
time slots they have indicated.)

### Event id

Note that each meeting has its own global group identifier  (as a
URL)  which lists the members attending the meeting (see next story):

# Solutions

## Sharing with data sync : 

+ #### WebDAV/CalDAV/CardDAV 
 Web standard, used by ownCloud for its sharing system.
 Heavy and quite slow. A different protocol for files (WebDAV), calendar (CalDAV) and contacts (CardDAV).
 
+ #### SyncThing 
 Still in active development, aim to provide p2p sharing between the syncthings clients with native encryption.
 Folder oriented, it is still young but promising. An ind.ie fork exists, named Pulse.
 
+ #### XDI 
 Pushed by Respect Network, XDI is an open protocol for p2p semantic sharing. 
 Not compatible for the RDF syntax, it is now more focused on secure messaging; but the future of XDI is not very clear for now. 
 
+ #### CouchDB replication 
  Based on versioning, the couchDB replication works extremely well to sync data between 2 remote server. 
  It would be possible to use only the replication protocol with a different backend (MongoDB, filesystem...), as long   as the same versioning system is the same. 
  
## Torrent sharing

+ #### BTSync
Extremely popular, it is not open and so not usable at all.  But I quote it for the record

+ #### MaidSafe 
A growing project, very promising. The idea is to allocate some hard drive space and computational resources to the SAFE network, and use it to have data replicated and hashed through several remote nodes on the network. 
Use bitcoin-like, safecoin, to retribute participating users.
  
## Communication

+ #### XMPP
Essentialy used for instant messaging, it was originally developed by Jabber before its standardization by the IETF. It is also possible to use it to transfer files, but it is not designed for it. 

+ #### Matrix 
Aim to be the new standard for instant messaging through HTTP, easier to use and lighter than XMPP, with a better identity system.
 
**TODO - document those : **
IndieWeb, multi-protocol, remotestorage, webintents, email, irc, rss,
 webmention, smtp,
  Camlistore, linked data protocol,
caliopen, indiereader
