slack notifications for icinga2
===============================

This is my perl implemenation of a slack service notification handler 
for icinga2. It was heavily inspired by
<https://github.com/jjethwa/icinga2-slack-notification/blob/master/slack-service-notification.sh>.

Installation and configuration
------------------------------

Drop slack-notification and slack-notification.ini into /etc/icinga2/scripts. 
Then get yourself an API token at <http://api.slack.com/web> and add into the
configuration file.

You also have to insert the hostname of your icingaweb2 installation into
General/WebHostname. 

You can also adjust the channel used by the notification handler
(General/Channel).

`slack.conf` contains example user/group/command/notification objects, drop it
into conf.d and adapt it to your needs.  

Message formatting
------------------

You can add your own emojis to the various servicestates. Just Edit
Format/SERVICESTATE. See <https://github.com/iamcal/emoji-data> for a 
list of supported emojis.

TODO
----

If someone really uses that, the following things would be nice:

- make message configurable via template
- add proper host notification
- some error handling
 
