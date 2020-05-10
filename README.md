# Always September

_If you scream into the void long enough, the void starts screaming back._

It appears that humans are having a little difficultly adapting to a world where communication methods have changed dramatically in less than a human life-time.

There are two fundamental problems:

* human brains are not designed to communicate with that many people at once. 

* what one person think is nice behaviour, can be at the same time be aggravating behaviour to another person. And vice-versa.

Neither of those are purely technology problems, they are problems that arise from humans using the internet to communicate with each other.

Rather than trying to solve those problems, we need to design systems that either naturally avoid those problems, or have the tools in place to quickly handle them.

## Assumptions

This is my working set of assumptions that I think communication systems need to be designed around. 

### Human communication scales poorly

Problems naturally occur when too many people try to communicate with each other in a single place.  

Those problems cannot be solved with technology, instead at best we can try to avoid them, by avoiding large numbers of people trying to communicate in the same place.

Rather than just having a single place for PHP core discussions, we should have separate comms channels for as many topics as are useful.

### Disagreement is normal

People make decisions based on the values they have learned from their own personal experiences.

Each person's experiences are different.

Two people who have had different experiences can make logical decisions based on their own experiences and come to different conclusions.

Because of that it is not always possible to come to consensus, and instead we need a way of moving past disagreement. The voting method works reasonably okay for PHP.
 
 
### Some voices are more useful than others

For any group of people, for any given topic, there will be some people who provide more value when they speak.

For PHP internals, the things the core contributors say are more important than random userland people who have never contributed any core code.

Although it would be wonderful if everyone could have their voice heard, there is a limit on how many people can take part in a conversation before the quality of the conversation is reduced.

### Moderation must be easier than walking away

The number of core contributors that have walked away from the PHP project is quite depressing.

Attempts at moderating people's behaviour on the PHP project have either all failed, or even worse resulted in blow-back for the people attempting to make the project not be a shithole.

The tools setup for moderation must be easy and powerful enough that people who are 

### Small moderation is more useful than drastic moderation

There are some behaviours that nearly everyone would agree are taboo. Things like racism, sexism and making threats of violence result in an easy decision to boot that person.

There are other behaviours that are not as noticeably bad. A lot of borderline acceptable behaviour depends on the context, and the background story.

Performing the small moderation actions are the thing that needs to be done to keep communities healthy and productive.


### There is no real difference between Dumb and Evil

Some people think they are being helpful when they are distracting core contributors with useless messages. See all of the 'helpful' suggestions of syntax for short closure, even after the RFC author did a full analysis of all the possibilities.

See also: https://www.youtube.com/watch?v=Q52kFL8zVoM&feature=youtu.be&t=2410
 
Some people think they are being helpful when they being annoying twats. 

Spending a large amount of time trying to figure out what the motivation of a person who is disrupting useful conversations is not a great use of time.

The choice of whether to allow someone to take part in a conversation should be based on how much utility they either are or could provide to a group, rather than the motivations of the person.


### Chat model is a series of rooms

Communication systems that are designed around 'rooms', where each room has it's own topic of discussion, is a useful model of what a good communication system would look like.

If you have a loud drunk person try to join the conversation, you should block them from entering the room.

If someone is talking over all the other people in the room, you should ask them to modify their behaviour.

If someone performs some useful work, you can give them a round of applause.

### Text file based communication scales better than 'verbal' communication 

Documents such as RFC texts are much easier to collaborate on if they are in a repository that accepts pull requests.

### Communication systems need to be composed of small replaceable parts

Any of the components of a communication channel may be found to be either inadequate, or become compromised.

For example, if we were using Github as the sole authentication method, and then the US decided to block access to Github from France, that would mean that any users in France would be unable to authenticate.

Additionally, some components just won't be fit for purpose, and will need to be replaced. 

### Communication systems need to be forkable

Sometimes it is appropriate to fork projects. Code can be forked by a press of a button. Forking the communication methods is really hard. That means that forks are not occurring when they should be, which leads to projects dying and general unhappiness.

## Required pieces

### Authentication

A component that allows authentication of people using external auth systems.

### Data feeds

Allow data to be move between rooms or to/from other places on the web e.g. bugs.php.net or twitter.

### Moderation

A system that allows moderation of messages in a room, and blocking some people from joining in a room.

### Room

A place on the internet where messages actually get sent for a particular topic, owner by a particular set of people. Technology wise, the are something between https://matrix.org/ and room11 with the ability to addin functionality, and pull/push data from external sources. 

### Voting

A defined format for proposing and then carrying out a vote in a room.


## Things that are not needed

### Knowledge base

Although most communities could do with a knowledge base, and a way to run query against that knowledge base, this not something I currently think is a requirement. Working on all the other stuff would make it much easier for other people to work on tools like this.




## Notes

### Approach to problem solving

The thinking behind this project is heavily influenced by the book ["Systemantics" aka "The systems bible"](https://www.amazon.co.uk/Systems-Bible-Beginners-Guide-Large/dp/0961825170/ref=). I strongly recommend that book to anyone who wants to be better at coping with problems.

### Name of project

The name of this project is a direct reference to the [Eternal September](https://en.wikipedia.org/wiki/Eternal_September) phenomenon. But changed slightly to avoid a clash in search engines.

 


