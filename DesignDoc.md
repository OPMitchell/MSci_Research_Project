#  Design Documentation

## Premise:
A system for simulation-based, interactive, emergent narrative generation.
- Intended for the creation of video games with non-deterministic storylines, allowing high levels of player agency.
- Aim is to create interactive, dynamic stories that change depending on the player’s actions and the reactions of authored, virtual autonomous agents.
- A key focus of the system is the modelling of the virtual agents’ thoughts, feelings, and state of mind. Agents are modelled intelligently and will respond realistically and appropriately to the player’s actions.

## System Design:
The storytelling system consists of 3 main components:
1. A global event generator (storyteller AI) that intelligently creates new story events for the player and virtual agents in the game world.
2. Intelligent, virtual autonomous agents that have their own personalities, emotions and goals. These agents react realistically to story events whether they are global events, events started by other agents, or events started by the player. Agents can produce their own events consisting of actions that will help them achieve personal goals, or preserve their own interests.
3. An event scheduler, consisting of a priority queue of story events. Events are scheduled depending on their importance. Scheduled events can also be preempted if highly important events are generated that must precede them.

### Component 1 - Global Event Generator (Storyteller AI)
A global, director AI which utilises a metaheuristic genetic algorithm to create, evaluate, and output desirable global events.
- Explore a search space of candidate global events
- Evaluate candidate events using a fitness function
- Perform selection to choose which candidate events to compare with each other
- Perform crossover to share attributes between candidate events and create potentially superior candidates
- Perform mutation to provide a stochastic element to the event generation process
- Eventually choose suitable/near-optimal global events to give to the player and virtual agents in the game world.

### Component 2 - Intelligent Virtual Autonomous Agents:
Intelligent, virtual autonomous agents (the other survivors) that react realistically and appropriately to the global event generator’s, player’s, and other agents’ actions in the gameworld.
- Heavily based on the FAtiMA (FearNot! Affective Mind Architecture) agent architecture used for the FearNot! (Fun with Empathic Agents to Reach Novel Outcomes in Teaching) project.
- Extended with a “multi-layer hierarchical connectionist network model for simulating human autobiographical memory”, proposed by Andrew Kope, Caroline Rose, and Michael Katchabaw in their paper, “Modeling Autobiographical Memory for Believable Agents”.

![Imgur](https://i.imgur.com/Woj66q9.png)

The extended model includes:
- **Psychological state of the agent/character**
    - Emotional personality model
    - Emotion reactions to events
    - Action tendencies (reactive processing) which model “spontaneous character reactions triggered by intense emotions, not part of the planning process”
    - Aim is to create believability of a unique character with the illusion of an independent “inner life”
- **Autobiographical memory**
    - Allows for context-dependent recall of past events
    - Effects of memories used to influence action selection and planning
    - Differs between immediate/short/long term memories
    - Dynamic and non-deterministic
- **Continuous planner**
    - Allows characters to act intelligently based on personality, emotions, goals, and previous events/memories
    - Continuous nature allows for “replanning of actions in the case of unexpected events”
    Includes:
        - **Goals** - world states that the agent desires to maintain
            - **Active Pursuit Goals** - has preconditions, success and failure conditions. Goals that the character is actively trying to achieve. Agent wants to reach a certain world state.
            - **Interest Goals** - used to apply protection constraints over a certain condition. Goals that a character does not actively pursue, e.g. avoiding getting hurt. Agent wants to preserve a current world state. Interest goals can be used to prioritise plans because plans that might possibly damage protection constraints will be less favourable.
            - Goals also have emotions tied to them, e.g, hope and fear. “The emotions represent the importance of the goal to the agent since the goals generating the strongest emotions are the ones that require more attention from the agent.”

        - **Actions** - the action that the character can use to reach a goal. Consist of:
            - **Preconditions** that have to be achieved before the action can be performed
            - **Effects** of the action - especially on the emotional state of characters
                
        - **Plans** - a sequence of specific actions that will result in the accomplishment of a specific goal
            
### Component 3 - Event Scheduler
An event scheduler, consisting of a priority queue of story events. 
- Events are scheduled depending on their importance.
- Scheduled events can be preempted if highly important events are generated that must precede them.
- All events outputted by the player, virtual agents, and the global event generator are added to the event scheduler.
- When an event reaches the front of the queue, it is executed and removed from the queue.
- As a result of executed events, new events are likely to be created by agent reactions and added to the back of the queue.

## Role of the Author:
