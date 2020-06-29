# LIP Meeting 2

**Meeting Date/Time**: Thursday June 25th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/3

**Recording**: https://youtu.be/rHnpEFqZ9Fc

**Notes**: Yondon Fu

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
        - [Design discussion](https://github.com/livepeer/LIPs/issues/25)
        - [Parameter discussion](https://github.com/livepeer/LIPs/issues/30)
        - Formalizing the security committee role that is responsible for safeguarding user value
    - Inflation change proposal
    - [A more gas efficient earnings calculation approach](https://forum.livepeer.org/t/a-more-gas-efficient-earnings-calculation-approach/1097)
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-25: Extensible Governance Contract

Updated LIP-25 to remove ACL
ACL/RBAC can be considered later as long as governance contract itself can be upgraded
Reduces complexity & scope of implementation

Feel like proposal is in good state for final discussion before moving forward with implementation

Doug: What if we use social convention around what is a bug fix and what is a contract upgrade?

There could be one function used for a bug fix and another that is used for an upgrade
The only difference would be that the bug fix function is subject to shorter delay or even no delay while the upgrade function is subject to a delay
The same address can call both functions, but having a clear distinction between a bug fix function execution and an upgrade function execution creates more transparency - everyone can see that the bug fix function was called without a delay and can verify for themselves whether they believe calling that function was actually warranted or not

Important that community knows the rules of the game

An alternative is to not have 2 functions and instead pass in the delay as a parameter to the function. Would accomplish the same thing. Having 2 functions with different names might be clearer though.

We don't need to schedule engineering/implementation around LIP calls

We should shoot to have an implementation ready before moving this into Last Call

### Inflation change proposal

Victor (Bison Trails) is working on an inflation change proposal
Just wrote something up and is getting some feedback on it
Not sure if this will be the thing that will be submitted yet

Change how slowly the inflation is decreasing
Something like .0003% -> .0001%
Slow down rate of decrease by about 2/3rds
Seems to be minimal viable change - stays true to original policy while still extending runway of subsidy by 2 years
Prob not right move to implement longer term solution right now
People that are going to use network aren't here yet and those are the people that we should optimize monetary policy for
66% instead of 33% because would rather not have this discussion again in a few months

Will finish getting feedback on proposal and then share more broadly

### More Gas Efficient Earnings Calculation Approach

Other benefits:
- Avoid confusion around claiming
- Easier to index because reward shares/fee shares won't change when claims happen

Yondon: Something to note is that the status quo is that if a delegator delegates away from an orchestrator before rewards/fees come in for the round, the delegator loses those shares and those shares are distributed amongst the remaining delegators. The current design in the forum post does not take this into account - instead those shares are just permanently lost and they don't go to anyone. This is the easiest implementation wise, but it does represent a change from the current behavior.

Gavin: Anyway to distribute rewards/fees in another direction besides to just stakers?

Could the extra rewards/fees go to:
- Rest of delegators
- Orchestrators
- Community pool

Depends. We should evaluate the implementation cost of each option and take that into consideration when evaluating what to do with extra rewards/fees. Worth noting that this situation with unaccounted for reward/fee shares can be reduced in frequency with better UI as well and it should be a relatively infrequence occurance. We should take that into account when evaluating what option to take - if the implementation cost is high then it may not be worth it given that there won't be a substantial amount of value accumulated from these situations.

### Open Discussion

- Nico: When should there be an implementation for an LIP? Should the implementation be made mandatory at a particular stage of the LIP process?
- Doug: Interested in formalizing proposal on capability/verification function within the protocol, but not sure if I am the best person to champion it. Interested in seeing if a handoff to someone else so they can champion it makes sense.
    - Yondon: Don't think everyone on this call has reviewed that forum post - we could plan on reviewing it first and then considering whether a handoff makes sense afte rthat 

### TODOs

- Review capability/verification function forum post so a decision on whether to handoff to another champion makes sens
- Create complete proposal for more gas efficient earnings calculation that also considers the implementation costs of handling unaccounted for reward/fee shares in different ways
- Update LIP-25 spec based on feedback of clearer distinction between bug fix vs. upgrade
- Work on LIP-25 implementation
