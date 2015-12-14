#Analysis - SLogo

##Project Journal
###Time Review
I spent approximately 20-30 hours a week on this project, anywhere from 4-6 hours a day, 5 days a week, give or take. Overall, I spent around 60-70 hours on the project from start to finish. 
Project start date: 10/3/15
Project end date: 10/27/15

I apportioned my time very well this time. Each time I sat down to work, I would have a single goal in mind, whether it be refactoring the design or incorporating a new feature. I would work until I completed the goal for the night. This worked out very well because I was not at all rushed to complete my contribution to the project on the last day. Because we started out with a very solid design, it was very easy to implement new features given in the third sprint. The hardest things to do was to figure out how to refactor the code when needed. 

###Teamwork
The team worked together pretty well. Joy and I were on frontend together, Austin and Charles were on backend. Joy and I did much of the frontend coding together. We started out pair programming, so much of the setup of the design was done off of Joy's computer. Once we had gotten to a solid design, we started working separately on implementing specific features of the UI. Because we had such a divide between front end and back end, we didn't spend much time together with the backend people designing (maybe a day each for when the sprints were due). Most of the designing for front end was done on the spot while Joy and I were working. 

Joy was the unofficial team leader. He worked on both front end and back end. While I focused on solely front end, I helped implement a lot of the UI components. Austin was responsible for setting up the back end. I'm not too sure what Charles implemented, but he was also back end. 

I was fine with the amount of communication between front end, but I do wish there was more back end communication going on. And back end to front end communication. This is because we were not sure about the status of back end a lot of the time except the day or a few days before each deadline. It's sort of nerve-wracking to not have your project come together until the very last minute. 

We had pretty strong divide in the project, and the plan was just to leave the two sub-teams to complete their parts of the project. While I think it worked out fine in terms of front end, I do think the back end was not as stable. We had very clear images on how the front end and back end would work together from the beginning, and although those images expanded a bit as we kept on programming, we were able to incorporate these expansions in our code. 

The plan and team roles help up pretty well even to the project extensions, at least in the front end. It was very easy to implement the further extensions. I heard the back end had some refactoring to do, but as a solely front end developer this time, I wasn't made very aware of them.

###Commits

We committed a crap ton this time. It makes it look like we did a lot of work. In a way I guess we did do a lot of work. We committed each time we refactored the code, or implemented a new feature. Basically, anytime we changed the code into something better that worked, we would commit it. It made it very easy to separate our work into little chunks of coding to do. Individually, we started out writing tests for all of the classes and structures we made, but by the end we got sort of lazy and stopped writing tests. I did make sure to run my code and look for any bugs manually, and have my partner merge my commits after making sure my code worked. 

Looking back over my commit messages, because each commit was so short, it's pretty easy to follow along the flow. It's also easy to see exactly what I contributed to the project because the messages are very clear in what each commit package contains. There are also not more than three or four messages in each commit package that I made. 

Commit Example 1:
"load/save pen color, language, background colors"
The purpose of my commit (surprise!) was to allow for the loading and saving of pen colors, language options, and background colors. I did not cause any merge conflicts. The commit helped the rest of my team by completing an extension given by the project, and to allow them to save default setting for the turtle and environment.

Commit Example 2:
I don't know the name of this commit, and I can't find it because we had 368 commits overall, but this is the only commit (or non commit) I made that created problems for others. The purpose of this commit was to add a pretty significant feature to the front end, one that would allow the user much more interaction with the turtle. I had originally committed it, but then realized that I hadn't pulled the latest commits before committing my own, so I cancelled my commit, pulled, and committed again. The second time I committed, however, my code ended up getting lost somewhere in the recesses of github. I still have no idea why it happened. We ended up spending a good hour trying to get my commit to show up on github. It sticks in my mind because there was no reason for that bug to occur and had nothing to do with the actual code, and more to do with github and my lack of github skills. 

###Conclusions

I think I contributed in a limited sense, in that I only worked on frontend. Last time I worked on both front end and back end, and had a much better understanding of how each component worked together. This time, I deeply understood how components in front end worked together, but had only a cursory knowledge of back end. I may have over-estimated the size of the front end. It turned out to be much more accomplishable than I expected. In the future, I will be able to estimate better by drawing upon my past experiences. I took as much responsibility as I could. I kept my partner informed about my progress, but not the back end people so much. 

The parts of our code that require the most editing, at least in the front end, would be the structure of the front end, I think. The front end code is pretty solid, but even though many of the components are acting on the same object and changing/using similar variables, it's pretty fractured as to where something is changed. There should be more coherency in where variables are located and stored, and how they update.

To be a better designer, I need to start thinking more about cases and how to design structures and classes to work together. I need to start thinking more holistically about the program, rather than going for the quick and dirty solution each time.

To be a better teammate, I need to work on my communication. I also wish I had more time to spend and figure out how backend works so I could have helped them out with that.

If I could improve one thing about my code right now, it would be how each component is displayed. It's a pretty small thing, but unless you had an intricate knowledge of where everything was located, it can be pretty confusing to navigate the UI. Basically, I would like to make our program more user friendly. Maybe I say this because I don't have much intimate knowledge of how back end works (except that it works, really). 

##Design Review
###Status
The code in the front end is generally consistent in the layout, naming conventions, descriptiveness, and style. The backend is also consistent, but not consistent with the front end. We used all uppercase letters for variables used in the code that were not just temporary, and named each method clearly with what it was meant to accomplish. The code is generally readable, and hopefully don't require comments to understand. However, towards the end of my commits, I may have slipped up a bit and the code would be readable only with knowledge of what the code was trying to accomplish (aka which component I am implementing). We tried to avoid dependencies in the code. The only place that used a static global variable was in a map that was populated once at the beginning of the code, and never changed, only used. Thus, the dependencies in our code are easy to understand. Due to the way that we structured our classes, implemented features were easy to extend. All you had to do was extend the new feature from another, closely resembling class, or from the component class. 

Class Example 1:
UIIndex.java

This class was interesting to me because it is our only instance of using a global static variable. I don't think it's particularly good or bad, it's a design choice that we made, but I do think there were other ways we could have allowed for the accessing of the those variables given by the class. The reason why this class was designed this way was so we wouldn't have to read in the variables every single time, and we would have to write getters and setters (basically does the same thing, just more code). At the same time, I tried to stay away from global static variables this time in coding, so it just stuck out to me when my partner decided on using this. 

Class Example 2:
SLogoController.java

I thought this code was interesting because it connected the front end to the back end. With this class, it's easy to see how independent the two halves of our designs were; it only took 122 lines of code to connect them. In terms of improving the code, the only thing I could say would be to split functions into even smaller portions, to increase readability and make it easier to understand functionality. I learned a lot about program design by looking through this class. It was interesting to see how little of backend was needed to update the front end, which I guess is the whole point of MVC design. I think the fact that we used Observers and Observables helped in lessening the dependencies as well, and in having to write code that checked to see if there was any changes because the Observable/Observer took care of that. Unfortunately, this code is pretty specific to the project, so I don't think it would be reusable in another sense.

###Design
The program is currently organized in MVC fashion. The view contains all components necessary to showcase the turtle and the commands being fed into it, including various variables and options. Turtleview is the controller for the front end. SLogoController is our controller class that connects the front end to the back end, Operator is the controller for the back end. The commands to the turtle is basically read into a tree, and commands are executed in order. There is an instance of the turtle in the front end and the back end, so technically, we are not passing turtles around. This allows us to create as many turtles as we want. Our code is designed in a way to allow for easy extensions, and to try and reduce dependencies of classes on each other. 

To add a new command to the language, one would only have to write up the class for the new command and make sure it exists within the language. To add a new component to the front end, one would have to extend the Components class and implement anything needed, code the required functionalities and add it to the list in the resource file. The implement a feature from the specification that was not implemented, well, that depends on the feature. If it was in front end, then it would most likely go in a components package, coded much like above.

We tried to encapsulate the program as much as possible. As a result of this, the front end is pretty much closed to the back end. There are elements of the back end in the front end, but that was a design choice we made to keep it that way. 

The design of our classes should be easily extensible and understandable. 

###Alternate Designs

I personally like the design that we went for because it was easy to understand what was going on. A design we could have gone for was to have variable checking in each individual class versus as separate classes, however, since the class has to be called upon each update anyways. There's nothing wrong with having the updates as separate classes, because the more we split up functionalities, the easier it is to extend the project. 

The original APIs changed to incorporate a lot more than just the map of string:commands that we thought it would, mostly due to all of the extensions that were required of it. From the beginning, the team was pretty set on using polylines and a turtle object, and we stuck with that the whole way through. 

I think the extendability of our design is commendable. A design choice we made was to not pass the turtle object. Instead, front end and back end would have their own instances of the turtle object and we would just pass commands back and forth. It was a good design decision to make in the sense that it decreased dependability and the possibility that we would screw something up with the turtle in either end. It was bad in the sense that it created more variables and work for us because we had to keep record of where the turtle was supposed to be and the state of the turtle, next state of the turtle, and such. 

Code Masterpiece:
I liked this particular aspect of the coding because of a conversation I had with my TA about the purpose of Java being to write as little redundant code as possible. Since many of our components use a table, we decided to create a tableview class that would create a table given the inputs. The two other classes featured here show how easy it is to create tables, especially in the case TurtleState which goes one step further and takes the table created by Workspace, and places its own inputs and just presents in a different manner. These classes I believe are a representation of that ideal in Java, to write as little redundant code as possible.
> Written with [StackEdit](https://stackedit.io/).