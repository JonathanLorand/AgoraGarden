
What are some of the takeaways from the reading group experience and from interacting with the work of Christopher Alexander? 


Here is a quick sort of description of the works that we read. They 
- concieve of form-making processes in a conceptual and systems-theoretic light, analalyzing the role of causal interdependences of "misfit variables" and design choices, and how these interact with the context as it changes
- attempt to understand why many traditional form-making processes seem to make "good forms" in a consistent manner which is adaptive over time ("homeostatic")
- posits an answer to the previous question and proposes a systematic method of design which aims to be homeostatic while at the same time being "selfconscious"
- aim to answer the question of what it means for a space to be "beautiful and alive" and what it means to have a "high quality of life" in terms of architecture
- propose a methodological framework for creating spaces which are alive, beautiful, and offer a high quality of life. This framework has aspects which are
	- structured sytemically in a fractal-like language of patterns which are ordered roughly by scale and by dependencies with respect to form and function
	- has a sequential and compositional mode of design and deployment
	- guided by principles (such as: ...)
	- participatory
	- specific to the site, users, and culture
	- extendable and adaptable over time

Below, I've started trying to write a sort of report on some of the idea and arguments that stood out for me. So far, this is quite incomplete still!

## Good Fit

In [[Notes on the synthesis of form]], Alexander introduces the notion of "good fit" as a property that might be achieved, or not, by an ensemble consisting of two abstract parts: a form and a context. The form is the part which the designer(s) choose to actively conceive, shape, and realize, and the context is essentially everything else that is relevant to the design task/problem/question at hand. In other words, with respect to a given design question, the abstract distinction between form and context is a distinction between those things that designers will exert agency upon and change, and those things that will be assumed to stay fixed for the duration of the design process. A key point for making this form/context distinction is that the form-making process and the changing of the context (which realistically is usually also happening) are assumed to proceed at different enough speeds so that, in approximation, we can think of the context as temporarily fixed. Another, but seperate, aspect of the form/context distinction is the question of which variables are under the designers control at all, and which not. 

A comment that Alexander makes and which I enjoyed is that, for a single given design question, there are often a large multitude of different ways to split the question into a part that is "the form" and a part that is "the context". 

## Homeostatic design processes

Alexander makes a distinction in [[Notes on the synthesis of form]] between "unselfconscious" and "conscious" cultures. In place of "culture", I will use "design processes". As I understand, the former are processes and techniques that develop gradually over generations. They were historically carried by traditions and consist of knowledge that is disctributed in society culturally and is passed down to next generations in a hands-on and experience-based manner. Selfconscious processes, on the other hand, describe processes of design typical in western indivualist and capitalist societies, such as the USA, since the mid 20th century. 

[ describe further what characteristics here are noteworthy / relevant ]


Alexaner takes the position that traditional "unselfconscious" design processes produced, historically, much better forms, and asks: why is this the case? He mentions that some might answer by citing a notion of "architectural Darwinism", which he however criticizes as insufficient in its explanatory power or its usefulness towards understanding how to improve contemporary design practice. Beginning on page 37, he says that this position 
	
	"... says roughly, that primitive forms are good as a result of a process of gradual adaptation -- that over many centuries such forms have gradually been fitted to their cultures by an intermittent though persistent series of corrections. But this explanation is vague hand-waiving. It doesn't tell us what it is that prevents adaptation from taking place in the selfconcious culture, which is what we want to know most urgently. And even as an explanation of good fit in the unselfconscious culture, the raw concept of adaptation is something less than satsifactory. If forms in an unselfconcsious culture fit now, the chances are that they always did. We know of no oustanding differences between the present state and past states of unselfconscious cultures; and this assumption, that the fit of forms in such cultures it the result of gradual adjustment (that is, improvement) over time, does not illuminate what must actually be a dynamic process in which both form and context change continuously, and yet say mutually well adjusted all the time.
	
	To understand the nature of the form-making process, it is not enough to give a quick one-word account of unselfconscious form-making: adaptation. We shall have to compare the detailed inner working of the unselfconscious form-making process with that the selfconscious process, asking why one works and the other fails. Roughly speaking, I shall argue that the unselfconscious process has a structure that makes it homeostatic (self-organizing), and that it therefore consistently produces well-fitting forms, even in the face of change. And I shall argue that in a selfconscious culture the homeostatic structure of the process is broken down, so that the production of forms which fail to fit their context is not only possible, but likely."
	
Alexander then goes on to make a conceptual and mathematical toy model for thinking about how a system, or a form-making process, might be able to behave homeostatically. 

## A toy model

The set-up and interpretation is as follows. We consider a system of 100 lightbulbs (let's imagine a 10x10 grid), and each one can be either in a state of being "on" or a state of being "off" at any given moment. To simplify our thinking about time, we work with discrete time steps, e.g. let us use steps that are 1 second long, and we assume that the state of any light bulb stays constant in any one time step, but may change from one time step to the next. Whether a lightbulb changes its state will depend on a number of rules, which we formulate now. For this, we imagine that some lightbulbs are directly connected to each other and some are not (we can think of some sort of wires as representing connections, or we can just think in terms of abstract labels which denote which bulbs are connected). The rules are:
1. If a bulb is on, it has a 50% chance that it will turn off in the next time step.
2. If a bulb is off, it has a 50% chance of turning on in the next time step *if* it is directly connected to a bulb which is currently on; otherwise it stays off in the next time step. 

The interpretation of this model is that lightbulbs represent misfit variables for a form that should solve a design problem, with the "off state" corresponding to "fit" and the "on state" corresponding to "misfit". So, ideally, the designers wish to bring the system to a state where all the lights are off (all variables are in the "fit" state). The connections between lightbulbs represent (mutual) interdependencies between the misfit variables. 

The rationale for rule (1.): it represents the fact that misfits will be attempted to be corrected over time. So, in the model, misfit variables are assumed to have a 50% chance of being corrected in each time step. 

The rationale for rule (2.): it represents the fact that, if a misfit variable is in a "fit" state, but a variable that it is interdependent with is in a "misfit" state, then there is a chance that this (or rather the changing around done by the designers) will "disturb" the one that was in a "fit" state. 

Alexander next goes on to do a rough analysis of the behavior of such a system over time. He claims that such a system will eventually arrive in a state where all the the lights are in the "off" state, as desired, and he observes that the time it takes, on average, to reach this state of "all off" will depend only on the pattern of interconnection that the system exhibits. (I wonder if there is a mathematical proof written somewhere that the system will eventually reach an "all off" state; I'm guessing that Alexander did consider this as a rigorous mathematical statement and I wonder how it was formalized precisely). He then analyzes the following three simple special cases. 

Case 1: We assume here that there are *no* connections between any of the lights. In this case, once a light goes off, there is nothing that would cause it to go on again. And, each light will eventually turn off. The average time for the whole system to go off is the same (or of a similar order?) as the average time for a single light to go off; that average time is $\sum_{k=0}^\infty \frac{1}{2}^k = 2$ seconds. 

Case 2: We assume now that all the lights are directly connected to all the other ones. Approximately speaking, the only way that all the lights will ever go off is if they all go off at once. This will happen eventually, but the average time until this happens is of the order of $2^{100}$ seconds (since we are considering rule 1, for which the 100 lights behave independently). This amount of time is roughly $10^22$ years, which is longer than the estimated age of the universe. 

Case 3: We assume that the 100 lights are grouped into 10 subsystems, each consisting of 10 lights each, and such that within each subsystem all lights are connected to each other, and such that lights in differing subsystems are never connected to each other. In this sense, the subsystems are inpendent of one another. Now the average time for the whole syste to reach an "all off" state will be the same as the average time for a subsystem to reach an "all off" state, and that time is $2^10$ seconds, or roughly 15 minutes. 

The striking fact is that the average time in Case 3 is much much closer to the average time in Case 1, while average time in Case 2 is impossibly long. The conclusion that Alexander draws from this:

	"No complex adaptive system will succeed in adapting in a reasonable amount of time unless the adaptation can proceed subsystem by subsystem, each subsystem relatively independent of the others." (p41)

Given a form-making process, or any system represented by the toy model above, it is often the case that we cannot see "inside" it in the sense of being able to know explicitly the (conceptual and causal) interdependencies between the relevant mistfit variable. However, Alexander observes, we can infer knowledge of the interdependency structure of the system by seeing how the system reacts to change. In terms of the toy model, if we imagine that an external agent would occasionally flip on a single light, we can observe how the system reacts to this disturbance. From this, Alexander argues, we can infer qualitative features of system: whether there are many interdependencies or not, and whether these structure the system into a number of relatively independent subsystems. (I wonder here again, to what degree this statement hase been rigorosouly analyzed). 

[include more from page 45 here]

## The reality of patterns

A significant part of the philosophical core of [[The Timeless Way of Building]] seemed to me to be in chapter 15, titled "The reality of patterns". The idea here seems to be that one can "empirically test" architectural patterns by observing how they make us feel.  

For lack of time to formulate things well in my own words, here is copy-pasted the cursive text in the chapter (i.e. its short version). I'd like to analyze and reflect on this content more, and integrate it with the discussion of the other aspects of what we read. 

***

*We have seen in the last chapter that there is a process by which a person can formulate a pattern; and make it explicit, so that other people can use it. Many such patterns have been writien down, in volume 2. 
But so far, there is no guarantee at all that any one of these patterns will actually work. Each one is intended to be a source of life, a generative, self-sustaining pattern. But is it actually? How can we distinguish patterns which work, which are deep and worth copying, from those which are simply pipe dreams, mad imaginings ... *


*One test says that a pattern is alive if its individual statements are empirically true.* 

We know that every pattern is an instruction of the general form: 

context —> conflicting forces > configuration
 
So we say that a pattern is good, whenever we can show that it meets the following two empirical conditions: 

1. The problem is real. This means that we can express the problem as a conflict among forces which really do occur within the stated context, and cannot normally be resolved within that context. This is an empirical question.
2. The configuration solves the problem. This means that when the stated arrangement of parts is present in the stated context, the conflict can be resolved, without any side effects. This is an empirical question. 

*But a pattern is not alive just because its component statements are true, one by one.*

*The fact is that even though its individual component statements are true, the pattern has no empirical reality as a whole. *

*Even the fact that a pattern seems sensible, and has clear reasoning behind it, does not mean at all that the pattern is necessarily capable of generating life.* 

*A pattern only works, fully, when it deals with all the forces that are actually present in the situation.*


*The difficulty is that we have no reliable way of knowing just exactly what the forces in a situation are. *

*What we need is away of understanding the forces which cuts through this intellectual difficulty and goes closer to the empirical core.* 

*To do this, we must rely on feelings more than intellect. *

*The pattern ALCOVE feels good to us, because we feel the wholeness of the system there.* 

*The pattern T-JUNCTIONS makes us feel good, because we feel the wholeness of the system there. *

*And MOSAIC OF SUBCULTURES makes us feel good, because, again, we feel the whaleness of the system there.* 
 
*By contrast, patterns made from thought, without feeling, lack empirical reality entirely.* 

*We see then, that there is a fundamental inner conne tion between the balance of a system of forces, and our feelings about the pattern which resolves these forces. *

*This makes it easter to test any given pattern. *

*We can always ask ourselves just how a patiern makes us feel.And we can always ask the same of someone else.* 

*It is not the same, at all, as asking someone his opinion.*

*It is also not the same as asking for a person’s taste.* 

*And it is also not the same as asking what a person thinks of an idea.* 

*It semply asks for feelings, and for nothing else. *

*The success of this test hinges on a fact which I have not said enough about so far — the extraordinary degree of agreement in people’s feelings about patterns.*

*There are few experiments, im science, where a phenomenon is capable of generating this extraordinary level of agreement. *

*But for fear of repeating myself, I must say once again that the agreement lies only in peoples’ actual feelings, not in their opinions.* 

*These feeling which are in touch with reality are sometimes very hard to reach.*

*Yet it is only this true feeling, this feeling that requires attention, this feeling that requires effort, which is reliable enough to generate agreement.*

*We see then that the concept of a balanced pattern is deeply rooted in the concept of feeling.* 

*But even so, feelings themselves are not the essence of the matter.* 

*In short, what is at stake at last, is nothing but the guality without a name itself.*

*It is, in the end, the presence of this quality in a pattern which makes the difference between one which lives and one which doesn't ... *

*It is reality itself which makes the difference.* 

*And it is in the end only when our feelings are perfectly in touch with ihe reality of forces, that we begin to see the patterns which are capable of generating life.*

*Yet it is hard to give up preconceptions of what things “ought to be,” and recognize things as they really are.*

*In this respect attention to reality goes far beyond the realm of values.* 

*By seeming to be unethical, by making no judgments about individual opinions, or goals, or values, the pattern rises to another level of morality.* 

*Then it becomes a piece of nature. 
When we see the patiern of the ripples in a pond, we know that this patiern is simply in equilibrium with the forces which exist: without any menial in- ter ference which is clouding them.
And, when we succeed, finally, in seeing so deep imto a man-made pattern, that it is no longer clouded by opinions or by images, then we have discovered a piece of nature as valid, as eternal, as the ripples im the surface of a pond.*>)



***
IGNORE BELOW HERE
(its the rough copy-past of chapter 15 of TTWoB)
*** 

*We have seen in the last chapter that there is a process by which a person can formulate a pattern; and make it explicit, so that other people can use it. Many such patterns have been writien down, in volume 2. 
But so far, there is no guarantee at all that any one of these patterns will actually work. Each one is intended to be a source of life, a generative, self-sustaining pattern. But is it actually? How can we distinguish patterns which work, which are deep and worth copying, from those which are simply pipe dreams, mad imaginings ... *

Suppose that we are trying to agree about a pattern. How can we agree whether it lives or not? Or, suppose that you are reading a pattern which someone has written down. 
How can you decide whether to make it part of your language or not? 

*One test says that a pattern is alive if its individual statements are empirically true.* 

We know that every pattern is an instruction of the general form: 

context —> conflicting forces > configuration
 
So we say that a pattern is good, whenever we can show that it meets the following two empirical conditions: 

1. The problem is real. This means that we can ex- press the problem as a conflict among forces which really do occur within the stated context, and cannot normally be resolved within that context. This is an empirical question, 
2. The configuration solves the problem. This means that when the stated arrangeinent of parts is present in the stated context, the conflict can be resolved, without any side effects. This is an empirical question. 

*But a pattern is not alive just because its component statements are true, one by one.*

One of the funniest examples of a pattern I have ever eard of is the “‘madhouse balcony.” 
This is a pattern which a student once invented. It says that the balcony of any mental patient’s room should have a chest-high railing on it. The argument is this: on the one hand, people want to be able to enjoy the view— and this applies as much to mental patients as anyone else. On the other hand, mental patients “have a tendency to jump off buildings.” In order to resolve this conflict between forces, the railing on the balcony must be high enough to prevent a patient from jumping over, but low enough so that he can enjoy the view.
We laughed for hours when we first saw this. And yet, absurd as it is, it seems to follow the format of a pattern. It has a context, problem and solution: and the problem is expressed as a system of conflicting forces. 
What is it that makes it absurd? 

*The fact is that even though its individual component statements are true, the pattern has no empirical reality as a whole. *

A balcony of this kind will not allow a mad person to heal himself: it will not help to make the world more whole. It 1s absurd because we can feel in our bones that it would make no difference at all whether such a balcony was built into the world or not. We know that the problem cannot really be solved in this or any related way. 

*Even the fact that a pattern seems sensible, and has clear reasoning behind it, does not mean at all that the pattern is necessarily capable of generating life.* 

For example, the famous radiant city pattern of high towers, freestanding in the landscape, was “invented” by Le Corbusier with great devotion and seriousness. He believed that it would be possible to give every family light, and air, and access to green, within this pattern: and he spent many years developing this pattern, in theory and practice. 

However, he forgot, or did not realize, that there was one additional essential force at work in the system—the human instinct for protection and territoriality. The huge, abstractly beautiful green spaces around his high buildings are not used, because they are too public, they belong to too many people at the same time, and they are under the eyes of too many hundreds of apartments hovering above them. Under these circumstances, this one force—-a kind of animal territorial instinct-—destroys this patttern’s capacity to generate life... 

*A pattern only works, fully, when it deals with all the forces that are actually present in the situation.*

On the face of it this is a simple intellectual concept. When we find a pattern which does bring forces inte balance, then this pattern will of course begin to generate the quality without a name which is described in chapter 2 —because it will contribute to that process in which the forces of the world run free. On the other hand, a pattern always lacks this quality if it resolves some forces at the expense of others which it leaves unresolved. 
It should be reasonably easy to identify these patterns which are alive, in these terms, and to distinguish them from those patterns which aren’t alive. In practice, though, it turns out to be very difficult. 

*The difficulty is that we have no reliable way of knowing just exactly what the forces in a situation are. *

The pattern is merely a mental image, which can help to predict those situations where forces will be in har- mony, and those in which they won’t. 
But the actual forces which will cccur in a real situation, although objectively present there, are, in the end unpredictable, because each situation is so complex, and forces may grow, or die, according to subtle variations of circumstance. If we formulate a pattern in terms of some system of forces, which we think describes a situation, and our de- scription of the system happens to be incomplete, then the pattern can easily become absurd, Yet we have no analytical way of being sure just what the forces are. 

*What we need is away of understanding the forces which cuts through this intellectual difficulty and goes closer to the empirical core.* 

We need a way of knowing which patterns will really help to bring the world to life and which cnes won’t. And we need a way of doing it which is more reliable than analytical formulation. Above all, need a way of doing it, which is anchored in the cmpirical reality of what wil] actually happen, without necessarily requiring com- plex and extensive experiments which are too expensive to do. 

*To do this, we must rely on feelings more than intellect. *

For although the system of forces in a situation is ver} hard to define analytically, it is possible to tell, in a holistic way, whether the pattern is alive or not. 
The fact is that we feel good in the presence of a pattern which resolves its forces
And we feel ill at ease, uncomfortable, when a pattern leaves its forces unresolved. 

*The pattern ALCOVE feels good to us, because we feel the wholeness of the system there.* 

There is an intellectual formulation of the forces which alcoves resolve. For instance, they allow us to be private at the edge of a communal gathering, and, at the same time, remain in touch with whatever is communal there. But what clinches it, what makes us certain that this formulation has some substance to it, is the fact that al- coves make us fee] good, The conflict is real, because the alcove makes us feel alive; and we know the pattern is complete, because we can feel no residual tension there. 

*The pattern T-JUNCTIONS makes us feel good, because NOS. 2. we feel the wholeness of the system there. *

There is an intellectual formulation of the forces which ‘T-junctions resolve. A T-junction creates less crossing movements, and less conflicts for the drivers, and this puts the = pattern on a firm empirical foundation, But what clinches it, and makes us certain that the problem is a real one, and complete, is that we feel nrore comfortable, more relaxed, when we are driving in a street whose junctio are all [-junctions. We know, then, that there are no hidden crossing movements which we don’t expect; there is no possibility of unexpected cars shooting across our path-——in short we feel good there; and we feel good because the system of conflicting forces which T-junctions resolves is real, and complete. 

*And MOSAIC OF SUBCULTURES makes us feel good, because, again, we feel the whaleness of the system there.* 

Again there is an intellectual argument, which shows that when subcultures are separated from one another b communal land, each one can grow in its own way. In this case the system of forces is immensely intricate, and we must wonder, indeed, if we have managed to identify a complete balanced system of forces in this pattern. in, the certainty comes from the fact that we feel good in places where this pattern does exist. In places like S the Chinatown of San Francisco, or in Sausalito, which are vivid) with their own life because they are a little separate from the nearby communities, we feel good. We feel good because we can feel, in our bones, the lack of inhibition, the spontaneous growth, which follows its own course in these communities, because they are uninhibited by pressure from surrounding communities which have a different way of life. 

*By contrast, patterns made from thought, without feeling, lack empirical reality entirely.* 

The madhouse balcony makes us feel nothing. Certainly, we know at once, when we first hear it, that a balcony like this will not make us feel wonderful. There is no feeling in it: and this lack of feeling is the way our know!l- edge of its emptiness presents itself to us. And Le Corbusier’s radiant city makes us feel worse it actively makes us feel bad. It may excite our intellect, or our imagination; but when we ask ourselves how we shall feel in a place which is really built lke this, we know again, that it will not make us feel wonderful. Again, our feeling is the way our knowledge of its functional emptiness presents itself to us. 

*We see then, that there is a fundamental inner conne tion between the balance of a system of forces, and our feelings about the pattern which resolves these forces. *

It comes about because our feelings always deal with the totality of any system. If there are hidden forces, hidden conflicts, lurking in a pattern, we can feel them there. And when a pattern feels good to us, it is because it is a genuinely wholesome thing, and we know that there are no hidden forces lurking there. 

*This makes it easter to test any given pattern. *

When you first see a pattern, you will be able to tell al- most at once, by intuition, whether it makes you feel good or not: whether, you want to live in a world which has that pattern in it, because it helps you to feel more alive, if a pattern does make you feel good, there is a very good chance that it is a good pattern. If a pattern does not help you to feel good, there is very Jittle chance that itis a good pattern. 

*We can always ask ourselves just how a patiern makes us feel.And we can always ask the same of someone else.* 

Imagine someone who proposes that modular aluminum wall panels are of great importance in the construction of houses. Simply ask him how he feels in rooms built out of them. He will be able to do dozens of critical experiments which “prove” that they are better, and that they make the environment better, cleaner, healthier... . But the one thing he will not be able to do, if he is honest with himself, is to claim that the presence of modular panels is a distinguishing feature of the places in which he feels good. His feeling is direct, and unequivocal. 

*It is not the same, at all, as asking someone his opinion.*

If I ask someone whether he approves of “parking garages” say—~he may give a variety of answers. He may say, “Well it all depends what you mean.” Or he may say, “There is no avoiding them”; or he may say, “It is the best available solution to a difficult problem” . . . on and on. 

None of this has anything to do with his feelings. 

*It is also not the same as asking for a person’s taste.* 

If I ask a person whether he likes hexagonal buildings, say, or buildings in which apartments made like shoe boxes are piled on top of one another, he may treat the question as a question about his taste. In this case he may say, “It is very inventive,” or, wishing to prove that he has good taste, “Yes, this modern architecture is fascinat- ing, isn’t it?” StH, none of this has anything to do with his feeling. 

*And it is also not the same as asking what a person thinks of an idea.* 

Again, suppose I formulate a certain pattern, and it describes, in the problem statement, a variety of problems which a person can connect up with his philosophical leanings, his attitudes, his intellect, his ideas about the world—then he may again give me a variety of con- fusing answers. He may say, “Well, I don’t agree with your formula- tion of this or this facts or he may say, “The evidence you cited on such and such a point has been debated by the best authorities’; or again, “Well, I can’t take seriously, because if you consider its long term implica- tions you can see that it would never do” . . All this again, has nothing to do with his feelings.

*It semply asks for feelings, and for nothing else. *

Go to places where the pattern exists, and see how you feel there. Compare this with the way you feel in places where the pattern is missing. If you feel better in the places where the pattern exists, then the pattern is a good one If you feel better in the places where the pattern does not exist, or you can honestly detect no difference, be- tween the two groups of cases, then the pattern is no good. 

*The success of this test hinges on a fact which I have not said enough about so far — the extraordinary degree of agreement in people’s feelings about patterns. *

I have found that whereas people can get into the most amazing and complex kinds of disagreement about the “Gdeas”’ in a pattern, or about the philosophy expressed in the pattern, or about the “taste” or “style” which seems to be imphed in a pattern, people who come from the same culture do to a remarkable extent agree about the way that different patterns make them feel. ‘Take, for instance, the need that children have for water. A few years ago I was at a meeting in San Fran- cisco where two hundred people met, for an sermon to try to identify things that they wanted in their aty. They met in groups of eight, around small tables, vad spent the afternoon discussing what they wanted. At the end 1e afternoon, a spokesman from each group sum- marized the things they wanted most

Several different groups, quite independently, mentioned the fact that they wanted an opportunity for their children to play in, and with, mud and water—especially water—instead of the hard asphalt playing grounds which parks and schools provide. This fascinated me. It happened that one of the pat- terns in the language we had been developing, POOLS AND STREAMS, goes into great detail about the fact that children especially, and all of us, need the opportunity to play with water—because it liberates essential subconscious processes. And here, unasked for, was tenfold spontaneous confirmation of the pattern, born directly out of people’s feelings. Or take the question of the size of hospitals. Officials in Sao Paulo have recently begun construction of the largest hospital in the world—a hospital with 10,000 beds. Now g out of ten people—probably 95 out of too—will agree that a 16,000 bed hospital fills them with fear and appre- hension, Contemplate that simply as an empirical fact. It is an empirical fact of an order of magnitude far vaster than any piddling experiments and surveys which the experts can muster. 

*There are few experiments, im science, where a phenomenon is capable of generating this extraordinary level of agreement. *

And, yet, for some strange reason we are not yet will- ing to recognize the depth, and power and centered- 293

THE GATE ess of just these feelings. If the fact that Brazilian people do not feel good when they think about this hospital were mentioned in the legislature as a means of shedding doubt on the experts’ opinions, the legislators would smile politely; it would even be embarrassing to \ mention feelings in this situation. And yet this ocean of shared feeling is the place where we become one with one another—this is the source, in the end, of our agreement about pattern languages. is easy to dismiss feelings as “subtecti D> and 6 tis easy to dismiss feelings as “subjective” and “unre- iable,” and therefore not a reasonable basis for any form — of scientific agreement. And of course, in private matters, where people’s feelings vary greatly from one person to the next, their feelings cannot be used as a basis for agree- ment. However, in the domain of patterns, where people seem to agree gO, 95, even 99 percent of the time, we may treat this agreement as an extraordinary, almost shat- tering, discovery, about the solidity of human feelings, and we may certainly use it as scientific. 

*But for fear of repeating myself, I must say once again that the agreement lies only in peoples’ actual feelings, not in their opinions.* 

For example, if I take people to window places (window seats, glazed alcoves, a chair by a low windowsill looking out onto some flowers, a bay window ... ) and ask them to compare these window places with those windows in rooms where the windows are flat inserts inte the wall, 294

THE REALITY QF PATTERNS almost no ene will say that the flat windows actually feel more comfortable than the window places—so we shal] have a3 much as 95 percent agreement. And if I take the same group of people to a variety of places which have modular wall panels in them, and com- pare these places with places where walls are built up from brick, and plaster, wood, paper, stone . . . almost none of them will say that the modular panels make them feet better, so long as [ insist that I only want to know hew they feel. Again, 95 percent agreement. But the moment I allow people to express their opin- ions, or mix their ideas and opinions with their feelings, then the agreement vanishes. Suddenly the staunch ad- herents of modular components, and the industries which produce them, will find ali kinds ef arguments to explain why modular panels are better, why they are eco- nomically necessary. And in the same way, once opinion takes over, the window places will be dismissed as im- practical, the need for prefabricated windows discussed as so important .. . all these arguments in fact falla- cious, but nevertheless presented in a way which makes them seem compelling. In short, the scientific accuracy of the patterns can only come from direct assessment of people’s feelings, not from arguments or discussions. 

*These feeling which are in touch with reality are sometimes very hard to reach.*

Suppose, for instance, that a person proposes a pattern in N oO ia

THE GATE which water flows in four directions from a fountain. If f say to this person—does that make you feel good, he says yes, of course, that is exactly why I do it—it makes me feel good. Jt needs enormous discipline, to say, no, no, wait a minute, Tam not interested In that kind of glib stuff. If you compare the situation where the water comes cut in one substantial flow from the pool, and can irrigate an orchard, with the situation where the water trickles out in four directions---and ask yourself, honestly now, honestly——which of the two makes you feel better-—then you know that it makes you feel better when the fow is more substantial—it makes more sense, the world be- comes more whole. But it 1s hard to admit this, because it takes so much hard work to concentrate attention on the feelings. ft is not hard because the feeling is not there, or be- cause the feeling is unreliable. Tt is hard, because it takes an enormous and unusual amount of attention, to pay attention for long enough to find out which does actually feel better. 

*Yet it is only this true feeling, this feeling that requires attention, this feeling that requires effort, which is reliable enough to generate agreement.*

And it is only this much deeper feeling, which is con- nected directly to the balance of forces, and to the emergence of reality. Once a person is willing to take his feelings as seriously as this, and pay attention to them and ideas--then his perception of a pattern can approach the quality without a name. 

*We see then that the concept of a balanced pattern is deeply rooted in the concept of feeling.* 

And that our feelings, when they are real feelings, pro- vide us with a powerful way of finding out just which patterns are balanced and which ones are not. 

*But even so, feelings themselves are not the essence of the matter.*

For what is at stake, in a pattern which lives, is not merely the fact that it makes us feel good, but, much more than that, the fact that it does actually liberate a portion of the world, allow the forces to run free: and liberate the world from the imprisoning effect of concepts and opinions. 

*In short, what is at stake at last, is nothing but the guality without a name itself.*

Some patterns have this quality; and others don’t. Those which do make us feel good, because they help to make us whole, and we feel more at one with ourselves in their presence: but still it is the quality itself which matters most; not the effect which it has on us.

*It is, in the end, the presence of this quality in a pattern which makes the difference between one which lives and one which doesn't ... *

Take as an example the relationship between pedestrians and cars. Conventional wisdom has it that pedestrians ought to be separated from cars because it is quiet, and safe for them. But nagging reality shows us that even in towns where they are kept completely separate, the children still run out to play in parking lots, and people still walk casually along the roads reserved for cars. The fact is that people take the shortest paths, and that cars are where the action iS, There is no doubt that pedestrians do need some measure of protection from cars, for peace and quiet, and for safety. But also, paths need to pass where the action is, where pedestrians can meet the cars. It is possible to deal with both of these forces at the same time. If we put pedestrian paths at nght angles to roads, crossing them, but not entirely separate from them, we create peace and safety, but also create places where people on foot and cars can meet, hubs where th action 1s, where the two systems cross. And this pattern, which does in fact resolve the con- flict in the forces, also corresponds, of course, to just the places where we feel most comfortable about the relation between cars and people. Isn’t it true that in the busy part of a city, a system of paths which is entirely separate from 298

THE REALITY OF PATTERNS cars is too quiet, artificial, almost unreal? Isn’t it, instead, those paths which are quiet, beautiful, pedestrian paths but which do lead up to a road, which make us feel per- fectly in balance with these forces? Ask yourself, if you don’t know a path like this in a city, where the road with cars on it is in sight, crossing the path, but at one end— and ask yourself, when you are there, if you don’t feel fust riphe, ‘Yo this extent, this pattern, NETWORK OF PATHS AND CARS, is based on reality. So long as the context remains in which we have cars in the world, this is the pattern which takes the forces as they are and resolves them, without bias, by treating them exactly as they really are. 2 ye 

*It is reality itself which makes the difference.* 


Take another example: In the houses we built in Peru, we based our patterns on the underlying forces we could detect in people’s lives. Since many of these forces are ages old, we were led to create houses which have many features In common with the ancient and colonial Peru- vian traditions. For example, we gave each house a “Sala’’—a special formal living room, right inside the front door, for receiving formal guests, and a family room, where the family themselves might hve, further back into the house (see the pattern INTIMACY GRA- DIENT}. And we gave the houses leaning niches, cutside the front doors, where people could stand, half in, half utside the house, watching the street (see the pattern FRONT DOOR RECESSES). These patterns are both com- 299

THE GATE mon In traditional Peru. People criticized us strongly for trying to go back to the past, when they said, the Peruvian families themselves were struggling to catch up with the future, and wanted houses just like American houses, so they could have a modern way of life. The issue here is not one of past or present or future. It is a simple fact, that a Peruvian family with a single hving room, will experience conflict whenever a stranger visits them-—-they try to keep their family around the dinner table, talking and wate hing TV, yet, at the same time, they try to present the visitor with a formal way of entering the house, not mixed up with the family. And again, 1f it is not possible to stand in the front door, watching the street, many of the women will experience a conflict between the fact that, being women, they are expected to retire, not te be toc forward, or to sit openly on the street—and yet, being shut inside the house, they want to experience some connection with the street and the street lie. Ido not judge these facts, They are simply facts about the dynamics of being Peruvian in 1969. So long as these farces exist, people will experience unresolvable conflicts, unless the patterns are present and will, to this extent, be 1.1. 7 ess able to become whol 

*And it is in the end only when our feelings are perfectly in touch with ihe reality of forces, that we begin to see the patterns which are capable of generating life.*

THE REALITY OF PATTERNS That is what is hard——because so often people choose to put their own opinions forward, in place of reahty. In many cases, people react to the description of these forces by saying “‘it should be otherwise.” For instance, ENTRANCE TRANSITION is based, in part, on the fact that in a city street, people have a mask of street behavior, which needs to be wiped off by a transition, before a person car relax in a private or secluded place. One person’s comment on this pattern was: This fact is bad; people should learn to be the same in the street as they are in private places, so that we can all love one another. The comment is nice in its intent. But human beings are not so malleable. The street mask is created by us, in spite of our own volition: the fact that it comes into being is a fundamental fact about human nature in urban situations. There is little purpose, then, in saying: It would be better if this force did not exist. For if it does exist any- way, designs based on such wishful thinking will fail. ‘The beauty of an ENTRANCE TRANSITION, and the fact that it is capable of making us feel at one with our- selves, is based on thoroughgoing acceptance of these forces as they really are. 

*Yet it is hard to give up preconceptions of what things “ought to be,” and recognize things as they really are.*

For instance, the other day a radio advertisement for the

THE GATE boy scouts said: “When your hoy is sitting on the street corner with other boys, this is unhealthy—give him the chance to do what all boys are yearning to do—going on jong hikes, fishing, and swimming.” This statement was presented with religious fervor--and is, of course, a deliberate attempt, by believers in the puritan ethic, to impose their conception of what a boy ought to be like, on what a boy is actually like. Of course, a real boy some- times wants tc go swimming—but sometimes he wants to 1 hang cut on the street corner with his friends, and some- times he wants to look for girls. A person who believes that these pursuits are “unhealthy” will never be able to see the forces which are actually at work in the boy’s life with any sense of reality. and will never be able to use a pattern language How could such a person recognize the reality of the hattern TEENAGE COTTAGE which says that a teenager needs a cottage slightly remote from his parents, so as to nurture the beginnings of his independence; or how could he recognize the reality of PUBLIC OUTDOOR ROOM, which specifically pays attention to the needs which teen- agers have to gather, in urban public places, away from their houses, A person who believes in slum clearance will be blind to the real facts about the lives of people living in slums. A person who is convinced that skid row ought to be cleaned up will be oblivious to the real forces at work in a c hobo’s life, because he can’t accept the existence of a hobo. A person who is convinced that offices ought to be ‘flexi-

THE REALITY OF PATTERNS ble? will be oblivious to the real forces at work in groups of people who are trying to work, Any preconception about the way things “ought to be” always interferes with your sense of reality; it pre- vents you from seeing what is actually going on—and this will always prevent you from making the environ- ment alive. It will prevent you from inventing or dis- ost of covering new patterns when you see ther all---it will prevent you from using such patterns properly, to create a whole environment. 

*In this respect attention to reality goes far beyond the realm of values.* 

Usually people say that the choice of patterns depends on your opinions about what is important. One person thinks high buildings are best; another person likes low ones; one person likes plenty of space for cars, because he likes driving fast; another one hikes the emphasis to be given to pedestrians, because he doesn’t like driving. When we try to resolve disagreements like this, we are led back to people’s fundamental aims in Hfe: te their fundamental goals, or values. But people do not agree about their values. So this kind of discussion still leaves us in a position where patterns seem only te depend on opinions—the best you can say, according te this view, is that a certain pattern does or doesn’t help to satisfy certain goal or value. Or that some “forces” are “goad? and others “bad.”

THE GATE But a pattern which is real makes no judgments about the legitimacy of the forces in the situation. 

*By seeming to be unethical, by making no judgments about individual opinions, or goals, or values, the pattern rises to another level of morality.* 

4 Its result is to allow things to be ahv hig is 2 higher good than the victory of any one artificial system of values. The 2 attempt to have a victory for a one-sided view of the world cannot work anyway, even for the people who seem to win their point of view. The forces which are ignored do not go away just because they are ignored. They lurk, frustrated, underground. Sooner or later they erupt in violence: and the system which seems to win is then exposed to far more catastrophic dangers. The only way that a pattern can actually help to make a situation genuinely more alive is by recognizing all the forces which actually exist, and then finding a world in which these forces can slide past each other. 

*Then it becomes a piece of nature. 
When we see the patiern of the ripples in a pond, we know that this patiern is simply in equilibrium with the forces which exist: without any menial in- ter ference which is clouding them.
And, when we succeed, finally, in seeing so deep imto a man-made pattern, that it is no longer clouded by opinions or by images, then we have discovered a piece of nature as valid, as eternal, as the ripples im the surface of a pond.*