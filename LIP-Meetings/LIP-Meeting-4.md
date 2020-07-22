# LIP Meeting 4

**Meeting Date/Time**: Wednesday July 22nd 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/5

**Recording**:

**Notes**: Adam Soffer

## Agenda

<!-- Meeting agenda -->

- LIP candidates
  - [InflationChange Parameter Update](https://github.com/livepeer/LIPs/issues/34)
    - Champion: @viktorbunin
  - [LIP-25: Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
    - [Discussion](https://github.com/livepeer/LIPs/issues/25)
    - Champion: @kyriediculous
  - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
    - [Discussion](https://github.com/livepeer/LIPs/issues/35)
    - Champion: @yondonfu
- LIP process
  - Should an implementation be a requirement at a particular stage of the LIP process? If so, what stage should it be required in?
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### Inflation Change proposal

Viktor:

- Received lots of feedback from infra providers and community members and Incorporated as much feedback as he could
- Biggest change was that the proposal has been split proposal in two due to technical constraints
  - LIP-34 - change to the inflation =parameter
  - LIP-40 - change minter contract to support greater degree of precision
- Bundled into LIP-35
- Ready to move into last call

Yondon

- Support Easier to reason about individual LIPs individually by bundling
- Important that the LIP is as tightly scoped as possible given time constraint caused by inflation. Hitting zero within the next 6-8 months

### LIP-25: Extensible Governance Contract

Nico:

- There’s been a few changes since the last LIP call. There’s no delay parameter. Allows Livepeer Inc to patch bugs in the case of a vulnerabitliy
- There’s an implementation of this LIP open for review.
- Looking into using a new solidity compiler. Not a blocker for moving forward
- Ready to move into last call. Additional smaller changes can happen during last call.
- Might make sense to push this LIP first since it would make implementing other LIPs easier.
- Even though the change is not big, it would be good to have a third party security audit

Yondon:

- Depending on timing, if this LIP were to be voted on and accepted and deployed it would likely make the deployment of other lips easier. INp articular, the inflation change parameter update LIP.
- Would prefer a security audit for this LIP, but feels okay not having one given that it’s small in scope. We can make a formal decision in the coming weeks
- Will assess the timing on LIPs and based on that we can decide whether to do a batch security audit on all of them
- Would prefer an audit happens before a vote

### Cumulative Earnings Claiming

Yondon:

- A draft was created last week that describes a new algorithm for clamining earnings that seeks to drastically reduce the end transaction cost of claiming earnings.
- We’ve started an implementation for the spec.
- Feels like an uncontroversial change given that it’s an absolute positive for all participants on the network. Just need to make sure everything is transparent.
- Will likely receive less community feedback.

Nico:

- We found some edge cases while writing tests
- Feels like we’re making good progress
- The implementation will be finished before the next LIP call
- The changes are bigger in scope than the other LIPs so we want to make sure there are no errors in the new calculation approach.

- LIP process
  - Should an implementation be a requirement at a particular stage of the LIP process? If so, what stage should it be required in?

### Should an implementation be a requirement at a particular stage in the LIP process?

Yondon:

- Should not be explicitly required. Should be thought of as a tool to help increase the likelihood that people will react favorabley to the proposal.

Gavin:

- One of the things we do in Cosmos is provide a two step process:
  - 1. an overview in human language form
  - 2. An implementation and a final vote on whether implementation is acceptable

### Open Discussion

#### How to encourage more proposals

Viktor:

- Not sure who it benefits to burn the tokens when putting up a vote
- Would rather have too many proposals than too few
- Don’t need to take action on this immediately given that the price isn’t crazy

Nico:

- Heard from someone at makerdao that one of their initial gov voting systems wasn’t effective because there were too many proposals in the absence of a cost

Gavin:

- Should think about way we can reduce friction and encourage proposal creations

Nico:

- Can encourage champions to create a gitcoin grant for implementing proposals

### TODOs

- Complete LIP-25 and LIP-36 implementations
- Talk about next for steps for moving these LIPs into last call
