# Progress made during [IndieWebCamp Germany 2015](https://indiewebcamp.com/2015/Germany)

Decentralized sharing is something which currently doesn't exist on the web. There is ownCloud-to-ownCloud sharing, and our fetch-and-deliver proxy will help other projects to become compatible with that, but it is not clear if we can make OC-style sharing into a standard.

On the saturday we had a session about "folder sharing on the indie web", with a very interesting discussion. Halfway through we renamed the session to "Limited audience", because sharing a folder publically is as easy as defining a post type called "folder", and the real hard issues are in the area of sharing a folder with a limited audience.

There is already quite some existing work documented on the [indieweb-messaging](https://indiewebcamp.com/indieweb-messaging) wiki page:

* how to specify the recipients of a post
* how to make the recipients log in to view the post on your site
* how to notify the recipients
* how to retrieve a limited-audience post server-to-server without intervention of a human.

I (Michiel) added two extensions to this during IWC-Germany:

* how to publish and consume personalized [feeds](https://indiewebcamp.com/feed) with indiereaders as well as with simple feedreaders
* how to extend [micropub](https://indiewebcamp.com/feed) to support the concept of audiences

This approach is a much more natural integration with existing indieweb protocols and practices, so this opens up promising avenues to explore. For instance, the idea we had of a FilePicker plugin for Known, allowing to post files from your ownCloud or Cozy, can be implemented much more naturally if ownCloud and Cozy start supporting the micropub protocol for posting a given file to your blog.

If we add the audiences support to micropub, then it does everything we need.

One open issue is how to represent a folder or document in a [h-entry](https://indiewebcamp.com/h-entry), and how a file server can receive these in such a way that the folders look like normal folders on the recipient's storage.
