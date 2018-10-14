<center>
  <h1> Project Proposal </h1>
  <h3> A System for Emergent, Simulation-based, Interactive Narrative Generation </h3>
  <h5> Oliver Mitchell </h5>
  <p> psyom1@nottingham.ac.uk / 4246437 </p>
</center>

## Background and Motivation

#### Defining Interactive Storytelling:

Interactive storytelling is a unique form of narrative design seen in digital entertainment mediums where no pre-determined storyline exists. Instead, the user can change the story and influence the characters themselves. Bostan and Marsh define interactive  storytelling as an approach to computer game narrative design where "real-time feedback collected from the players is used by the game engine to continuously modify the content as it is being delivered." [1]. The key aspect of interactive storytelling is that the player is an active participant and their in-game actions have a direct effect on the narrative that is told. This differs from traditional computer game narratives which typically consist of an unchanging linear story with a pre-defined outcome.

#### Criteria for an Interactive Storytelling System:

Riedl identifies 3 criteria for interactive storytelling systems [2]:
1. The user actively participates, playing the role of a character and controlling a virtual avatar, or acting as an observer who has the power to make changes to the story-world and influence characters.
2. The user:
    - is told a story by a pre-defined story artifact conveyed through the medium
    - leaves the experience feeling like they have been told a story
3. The story changes as a result of a user's actions.

#### Problems with the Integration of Interactivity into Game Narratives:

Louchart et al. explain that in most computer games, attempts at complex, dynamic storylines are usually "confined to simple branching tree structures" [3]. Furthermore, as the scope of games increases and development effort is focused on assets such as textures, 3D-modelling and other gameplay content, a greater number of narrative possibilities arise. Yet the "static nature of these [tree] structures affects the range of options covered [and] reduces the framework for player interaction", an integral part of interactive storytelling. Louchart et al. go on to argue that "the integration of interactivity into game narratives requires a rethinking of the design process" because these tree-like structures either expand exponentially with the inclusion of more narrative elements (such as additional characters added to the game) or have to remain so simple and rigid that the player's immersion in the game world is threatened.

In short, with a greater amount of gameplay content comes infeasible exponential growth in the number of branches of a narrative tree structure. If the amount of potential story branches is too high, developers are forced to simplify the story, resulting in less (or no) player interactivity. This reduces player agency and can prevent the player from being immersed in a believable game-world, violating no. 3 of Riedl's criteria for an ISS [2].

#### The Narrative Paradox:

It is common for narrative design in computer games to follow the Aristotelian plot-based approach, meaning that complete control over every aspect of the story is required by the author, leaving little room for interaction by the player. Louchart and Aylett recognised that the "authoring of interactive narrative presents the paradox that ... the author requires control over the unfolding narrative whilst ... the user expects freedom over their decisions." [3][4]. These two goals clearly conflict. The greater the level of interactivity provided to the player, the less control the author has over the story's events. Equally, the more control the author has over the story, the less room there is for the player to interact with characters and change the course of the narrative. This concept has been dubbed the "Narrative Paradox" [5]. Louchart and Aylett suggest that a solution to this paradox should divert from the branching plot-based approaches implemented in current computer games, hence also solving the problem of an exponentially increasing number of diverging storylines.

#### Emergent Narrative:

Aylett proposed Emergent Narrative (EN) as an alternative. EN is an approach to designing interactive narratives where, instead of a fixed, authored plot, the "narrative weight of the application is shared by authors and players." [3][5][6]. This is typically achieved through simulating a virtual world, including virtual characters with different behaviours created by the author. The storyline then "emerges" at run-time from the interactions between these autonomous agents, and the player [2]. The advantage of an EN approach is that the narrative is non-linear and allows for a greater level of player interactivity. Despite this, ENs are unpredictable at authoring time. Kriegel and Aylett explain how authors are forced to "let go of specific story lines altogether and ... focus on creating the elements from
which the story will emerge." [7]. In this way, ENs work as a sort of 'sandbox'; the author defines the limits of the story world and creates the characters and behaviours that fill it, then sits back and watches whatever story is created by the simulation.

ENs benefit from having no rigid structure to their story; there is no branching tree structure to restrict the range of potential storylines. This solves the problem of infeasible exponential growth and allows for a potentially limitless number of possible storylines (should the simulation be complex enough). However, the narrative paradox remains. In fact, emergent narratives are the opposite of the plot-based approach;
where plot-based approaches require high levels of authorship and direction, restricting player interactivity, emergent narratives implicitly prevent the author from giving any direction at all, making them highly unpredictable.

Yet another disadvantage of emergent narrative approaches is their reliance on well implemented virtual agents and their control logic. If the AI controlling each agent is too simple, then the story is unlikely to be very compelling or complex enough to satisfy the player. Similarly, if the AI has too limited a set of possible responses to stimuli in its environment then the player may see the same storylines again and again, threatening their immersion in the game.

#### Motivation

The motivation for this research project is to evaluate the effectiveness of pre-existing methods and develop a novel approach to interactive storytelling that comes closer to mitigating the problems of the narrative paradox. Part of the project includes the implementation of a prototype IS system, intended to generate compelling narratives that are truly interactive and give players a real sense of agency.

## Aims and Objectives

The aim for this project is to research the field of interactive storytelling and explore ways of answering the open research question of the "narrative paradox", focusing on a simulation-based approach which exploits the usefulness of emergent narratives. The desired end result would include an externally published research manuscript, and a prototype interactive storytelling system.

Key Objectives:
1. Identify and evaluate the effectiveness of pre-existing techniques for the generation of interactive narratives in computer games.
2. Document a novel approach to interactive storytelling based on the combination of multiple, successful pre-existing techniques that exploit the pros of emergent narratives.
3. Create a working prototype interactive storytelling system (based on the results of objective 2), taking the form of a simulation-based computer game written in Unity.
4. Evaluate the effectiveness of the prototype by studying human participants using it and acquiring their thoughts and opinions.
5. Analyse the gathered data and conclude how successful the new system is.

## External Aspect

Presenting an interesting narrative to the player has always been a focus of video games. However, successful approaches to narrative design outside of linear/branching structures is very rarely seen in commericially successful AAA games. By conducting research into the field of interactive storytelling and exploiting the advantages of emergent narratives, the author hopes to publish a research manuscript of his findings (to be presented at the GAMER Research Collaboration Event at De Montfort University, 2019), and produce a playable prototype computer game which exhibits a novel approach to interactive storytelling.

## Work Plan:
The Gantt chart below shows the proposed division of tasks for every week until the project deadline:

| Task ID | Task Description |
|---------|------------------|
| A | Write proposal |
| B | Write interim report |
| C | Write final submission / research manuscript |
| D | Research and evaluate existing games that are products of IS research (e.g. Façade) |
| E | Research and evaluate the success of existing IS methods, particularly EN methods |
| F | Research ways of creating believable and effective AI agents |
| G | Implement a simple framework for the prototype system in Unity where different IS methods can be easily tested |
| H | Use the prototype system to test various existing IS methods and identify pros and cons of each  |
| I | Develop a novel hybrid approach to IS by combining parts of the successful, tested approaches |
| J | Test the novel IS method by implementing it in the prototype system |
| K | Conduct user testing with the finished prototype system |
| L | Analyse the results of the user tests and come to a conclusion regarding the success of the system and the project as a whole  |

![Imgur](https://i.imgur.com/j7L7IPB.png)

## Bibliography

| Reference ID  | Citation |
| ----------- | ----------- |
| 1 | Bostan B., Marsh T. (2012), "Fundamentals Of Interactive Storytelling", *Academic Journal of Information Technology*, **3**(8), pp. 20-42  |
| 2 | Riedl M. O. (2010), "A Comparison of Interactive Narrative System Approaches using Human Improvisational Actors", *Georgia Institute of Technology, College of Computing* |
| 3  | Louchart S., Aylett R., Kriegel M., Dias J., Figueiredo R., Paiva A. (2008), "Authoring Emergent Narrative-Based Games", *Journal of Game Development*, **3**(1), pp. 19–37 |
| 4  | Louchart S., Aylett R. (2003), "Solving the Narrative Paradox in VEs - Lessons from RPGs", *In: Rist T., Aylett R.S., Ballin D., Rickel J. (eds) Intelligent Virtual Agents. IVA 2003. Lecture Notes in Computer Science, Vol. 2792.*, pp. 244-248 |
| 5  | Aylett R. (2000), "Emergent Narrative, Social Immersion and "Storification"", *Proceedings Narrative and Learning Environments Conference*, Edinburgh, Scotland  |
| 6   | Aylett R. (1999), "Narrative in Virtual Environment - Towards Emergent Narrative", *In: Proceedings of the AAAI Fall Symposium on Narrative Intelligence, 1999*  |
| 7  | Kriegel M., Aylett R. (2008), "Emergent Narrative As A Novel Framework For Massively Collaborative Authoring", *In: Prendinger H., Lester J., Ishizuka M. (eds) Intelligent Virtual Agents. IVA 2008. Lecture Notes in Computer Science, vol 5208.* |
