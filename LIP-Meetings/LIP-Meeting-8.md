# LIP Meeting 8

**Meeting Date/Time**: Thursday September 17th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/11

**Recording**: https://youtu.be/lU2u3uaXoYA

**Notes**: Yondon

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/35)
        - Champion: @yondonfu 
    - [Earnings Snapshot Proposal](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-52.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/52)
        - Champion: @dob 
    - [LIP-56: Reward Period](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-56.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/56)
        - Champion: @yondonfu 
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-36

Expected timeline described in https://medium.com/livepeer-blog/earnings-claiming-gas-cost-reductions-lip-36-and-lip-52-timeline-70d4e6da4f7

Scheduled security audit with Quantstamp because the changes involved are quite complex.

Next steps
- Complete security audit tomorrow
- Start poll on Monday assuming any necessary changes from the audit are made by then

### LIP-52

Expected timeline described in https://medium.com/livepeer-blog/earnings-claiming-gas-cost-reductions-lip-36-and-lip-52-timeline-70d4e6da4f7

Worthwhile implication of LIP-36 + LIP-52 worth emphasizing: Earnings claiming will no longer need to be an action that users need to be aware of. It will still be a technical concept in the contracts, but users do not need to do anything extra - they can just perform staking actions and all this happens under the hood.

Nico: Could be worthwhile to communicate the removal of earnings claiming as a user action so that people don't wonder why applications like the explorer no longer support it - don't want users to think that something is wrong and that they're missing out on anything.

Next steps
- Finalize contract code
- Complete client tooling (CLI tool and explorer)
- Start poll soon after the LIP-36 poll finishes

### LIP-56

Big points from feedback thus far
- If we mint LPT each round but only distribute during reward round, what should we do about unaccounted for LPT i.e. an O misses a reward call?
- If we mint LPT each round but only distribute during reward round, is LPT minted staked or unstaked? Unstaked = decreasing participation rate if no additional LPT is staked. Staked = more complexity in implementation

Yondon: Haven't had time to push forward on this proposal all that much. But have been toying around with some ideas based on feedback thus far. We need to know how much LPT can be minted in the reward round based on a per round inflation rate. Would need to upgrade Minter to support this. But what if the Minter was upgraded to separate bank functionality from inflation rate management functionality. This would support the reward period changes, but also makes upgrading inflation rate details in the future easier such that you don't need to upgrade the Minter and migrate LPT/ETH every time like we had to do for LIP-40.

Doug: Seems like this would add nice future flexiblity, but should make sure we prioritize gas cost relief.

Yondon: Suspect that this idea could be easier/faster to implement than the current design in the LIP. Need to validate of course.

Next steps
- Follow up on the idea of moving inflation rate management functionality out of Minter and writeup more detailed overview in discussion thread. If it makes sense/there is confidence around it, incorporate it into the LIP

### Open Discussion

Nothing this time. Focused on trying to rollout the current candidates and only then revisiting other interesting ideas.