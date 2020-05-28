# LIP Meeting 0

**Meeting Date/Time**: Thursday May 28th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/1 

**Recording**: https://www.youtube.com/watch?v=jdt-ty7cllA&feature=youtu.be

**Notes**: Yondon Fu

## Agenda
<!-- Meeting agenda -->

- The purpose of LIP meetings
- LIP candidates
    - [Extensible Governance Contract](https://github.com/livepeer/LIPs/issues/25)
- Sentiment polls
    - How would someone run a sentiment poll?
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### Purpose of LIP Meetings

LIP calls are more targeted toward participants in the LIP process as opposed to a more general community call
Small, but meant to be smaller because it is more relevant for active participants in the process

### Extensible Governance Contract

Nico presents slides (see recording).

We're still continually working on milestone 1 i.e. decentralization of knowledge, LIPs and polling

This proposal is relevant for milestone 2
We do not define the binding voting system to be used in the future, but we create the interface that makes any binding voting system possible in the future
Want a clear path for upgrading the governance system to give stakeholders more control of the system and to phase out the Livepeer multisig

Main features
- ACL
- Batched execution
- Delayed updates

Upgrade path
1. Deploy extensible governance contract with Livepeer multisig as sole actor
2. Delayed updates for the multisig
3. First binding voting system becomes an actor for protocol params
4. Allow binding voting system to execute contract upgrades
5. Remove Livpeeer multisig as actor

Doug: How do we determine what the delay for an update is?
Nico: Considered different delays for different updates. Then we would establish initial values for this. Maybe inflation changes need 7 days, but other updates can have shorter delays.
Adam: For time sensitive updates, how do you envision those updates happening?
Nico: Assume that initially Livepeer multisig still has control and would not be subject to a time delay.

Yondon: Maybe delay for param updates, but not for code updates initially to allow for time sensitive bug fixes.

Doug: What is the point of delays in the first place?
Nico: One example is ability to unbond and exit before the update happens. I like to think about it as similar to rage quitting with MolochDAO - you can quit from a regime you don't want to participate in.

Gavin: Not sure if anyone is doing this, but recall network where you can't vote yes and exit, but if you vote no you can exit sooner.
Yondon: Would be good candidate for design of binding voting system.

Nico: Spec defines actors. An actor could be a multisig. Could be controlled by a technical council. Strength of spec is that it is quite generic.

Yondon: What is in scope of the proposal w.r.t the upgrade path?
Nico: Steps are pretty clear for 1 & 2, but not so much afterwords.
Yondon: Maybe we should make more clear which steps are in scope of this proposal.

Yondon: Maybe we should separate the initial parameter values from the design of the system itself.
Nico: Agreed.
Gavin: The initial values can help inform the design. Can make it less abstract.
Doug: Describing the genesis state of this proposal would be helpful.
Nico: We could use a sentiment poll about initial parameter values.

Doug: Nico, what do you think the current state of this proposal?
Nico: Think of it as a draft LIP at this point. Still some details to be fleshed out. Not code complete.
Yondon: So next steps seem to be checking it in as draft LIP.

### Sentiment Polls

What does sentiment poll mean?
Gauging community opinion about a potential change
Not necessarily code, full design, etc.

Doug: Should there be social conventions? Is there a workflow where they can use existing polling system?
Nico: Poll creation cost could be a problem? Gas costs for voting when its just for sentiment might be a barrier?
Doug: Don't have reaction that those are blockers. They set a bar that this is an important issue.

Yondon: Two possible paths for sentiment poll participation. Path 1 = expose those polls in explorer. Path 2 = use existing UI components to create a new app dedicated to sentiment polls
Adam: Better expectations with voting in explorer - if you use the explorer the expectation is that accepted poll lead to team execution. Want to make it VERY clear that no action happens after sentiment poll is over

Doug: How do we avoid a huge rebuild for a separate experience?
Yondon: Re-use explorer UI components?
Adam: Would just want to make sure that things are clearly labeled i.e. sentiment poll vs. execution poll

Doug: Gavin, you've had some thoughts about taking a cut of inflation for a community fund. Would sentiment poll be useful here?
Gavin: Could see that being used to determine if this idea is even worthwhile to iterate on.
Doug: Would you pay 100 LPT for the poll to show up in the explorer and have it labeled sentiment?
Gavin: Depends on what the price of LPT is. Will whatever I propose benefit me? Maybe ask for a grant to fund the poll.
Doug: Are there lighterweight experiments we can do before heavy weight solutions like adding to explorer or separate app? 

Adam: Each LIP links to discussion. Was under impression that discussion is how to seek sentiment around an issue.

Yondon: Maybe a lightweight experiment is surfacing when discussions happen and have digests that are understandable for people to be aware of.

Yondon: For next time, let's think about how we can make info more digestible/legible before considering different ways to aggregate inputs.

### Open Discussion

Eric: Does it make sense to have a more specific goal for the call?
Nico: I like the idea of keeping up with the progress of LIPs and having clearer objectives.
Yondon: Since we already have the assumption that LIPs are only on the agenda if there is a champion for it we can use the call as a way to set deliverables for the LIP brought forward by the champion and do progress updates.

An example of the above:
- Nico is championing the governance contract LIP
    - For next time, we want to have a draft LIP PR opened and we want the spec design details to be fully fleshsed out.

### TODOs

- Create a formal draft LIP for https://github.com/livepeer/LIPs/issues/25
- Flesh out the rest of the design details for https://github.com/livepeer/LIPs/issues/25
- Describe the initial state of the system proposed in https://github.com/livepeer/LIPs/issues/25
- Create a separate discussion thread around lighterweight experiments for sentiment polls (this can be added to the next agenda if there is a champion for the topic)
