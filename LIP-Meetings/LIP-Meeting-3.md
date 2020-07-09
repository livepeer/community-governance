# LIP Meeting 3

**Meeting Date/Time**: Thursday July 9th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/4

**Recording**: https://youtu.be/z5xDec0jwlM

**Notes**: Yondon Fu

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [InflationChange Parameter Update](https://github.com/livepeer/LIPs/issues/34)
    - [Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/25)
    - [A more gas efficient earnings calculation approach](https://forum.livepeer.org/t/a-more-gas-efficient-earnings-calculation-approach/1097)
    - [Protocol capability + verification functions](https://forum.livepeer.org/t/abstraction-of-the-livepeer-protocol-to-support-more-capabilities/1086/8)
        - Possible champion handoff and/or decide whether this is a priority
- LIP process
    - Should an implementation be a requirement at a particular stage of the LIP process? If so, what stage should it be required in?
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-25: Extensible Governance Contract

Nico:
- Nearly finished implementation of spec
- Social conventions for delay param for updates vs. bug fixes
- Param provided by Livepeer Inc when doing updates
- Set to 0 when doing bug fix
- Take a look at PR to merge updated draft
- Then will push through Last Call

### Inflation change proposal

Viktor:
- Want quick decisions - timeline not days, but not months
- Extend runway to provide broader adoption
- Some disagreement about negative impact of inflation = 0
- If we think the answer is yes then want to understand appetite for change
- Additional considerations
  - Is this the best we can do right now?
  - Update inflation change or update target bonding rate?
- Want inflation to go to 0 in long term - think that is important for sustainability
- From that POV makes me hesitant about changing target bonding rate

Doug:
- We've been sharing POVs on proposal in GH issue
- Let's acknowledge that in our LIP process Viktor has ability to move the LIP through the process without needing buy in from everyone at the early stage
- To Viktor: What would be most helpful for you to get feedback on?

Viktor:
- Top thing is to get opinion of respected people with expertise in these areas to inform approach

Gavin:
- I see 2 major things
  - Acknowledge something needs to be done
  - How is it done

Viktor:
- Cos like Bison Trails don't have large scale GPU farms
- Fully expect these cos to be left behind if we don't scale up and prepare
- Who is benefiting from this change? Token holders

Doug:
- Does the analysis that inflation benefits everyone that participates and only hurts non-participants affect people's POV?

Nico:
- Concerned about experience of smaller operators vs. larger operators
- Not just about incentivizing GPU providers, but about operators providing value add services

Viktor:
- Either way, attracting demand will be the most important
- More to think about -> not just improve tooling to top performances, but think about as Livepeer evolves how does the community evolve as well

Doug:
- Having nodes call reward without providing transcoding in the early days wasn't all bad -> led to a lot of community building efforts from those early adopters

Viktor:
- Not a developer - need help

Yondon:
- Can help with implementation

### More Gas Efficient Earnings Calculation Approach

Yondon:
- Should finish draft LIP today

Doug:
- FWIW there's been very little user attention to losing reward shares because a delegator moves stake before an orchestrator calls reward

### Protocol capability + verification function

Doug:
- 2 reasons why I think this is important to press on
  - Clear sensible solution to verification problem that makes protocol rules tighter prior to significant research
  - Opens up network to more capabilities
- TODO = lead discussion on this topic before recruiting someone for more design + code

### Should an implementation be a requirement at a particular stage in the LIP process?

A few people had to drop off so we'll continue this discussion next time. But, some people shared initial thoughts

Doug:
- Feel like this can be up to the proposer 

Yondon:
- Do what needs to be done to maximize probability of people voting yes on the LIP whether that means having a finalized implementation or having an audit

### Open Discussion

N/A

### TODOs

- Viktor to get additional feedback on inflation change proposal (maybe couple of days) before pushing forward
- Yondon to help Viktor with inflation change proposal implementation
- Nico to finish implementation for LIP-25 and get it to Last Call
- Yondon to publish draft LIP for earnings claiming
- Doug to push forward discussion on protocol capability + verification function
- We'll follow up on the implementation requirement discussion next time
