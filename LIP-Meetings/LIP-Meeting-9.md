# LIP Meeting 9

**Meeting Date/Time**: Thursday October 8th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/12

**Recording**: https://youtu.be/Cn8JlkBT8Sc

**Notes**: Adam Soffer

## Agenda

<!-- Meeting agenda -->

- LIP candidates
  - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
    - [Discussion](https://github.com/livepeer/LIPs/issues/35)
    - Champion: @yondonfu
    - Poll recap
  - [LIP-52: Earnings Snapshot Proposal](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-52.md)
    - [Discussion](https://github.com/livepeer/LIPs/issues/52)
    - Champion: @dob
    - Poll recap
  - [LIP-56: Reward Period](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-56.md)
    - [Discussion](https://github.com/livepeer/LIPs/issues/56)
    - Champion: @yondonfu
    - Technical responsibility update
  - [LIP-25: Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
    - Champion: @kyriediculous
    - Timeline for creating a poll
-
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-36: Cumulative Earnings Claiming

Yondon

- Official status of this proposal is final. It was accepted in a poll and deployed to mainnet.

Gavin

- Seems like a low orchestrator turnout.

Yondon

- Are there any other projects that do something that help increase voting engagement?

Gavin

- Something as simple as an opt-in mail list can increase the level of engagement.

Nico

- It would be beneficial to provide a more general non-technical summary of what an LIP does so that it’s more easily digestible. Would also be nice to provide more transparency around who created a poll. Perhaps using 3box. Depending on who creates a poll could create more confidence in voters.
- Can document this as a GitHub issue for the poll application

Gavin

- Would you be up for documenting this as a GitHub issue for the poll application?

Nico

- Do we think gas prices affect poll participation

### LIP-52: Earnings Snapshot Proposal

Nico

- A snapshot was taken. A new contract was deployed that stores the merkleroot of this snapshot. This is entirely queryable on chain.
- We also released a CLI tool that allows users to verify and claim their earnings.
- Planning on deploying LIP-52 on Monday.
- We’re also updating the explorer that removes the need to manually claim earnings. The explorer will automatically claim past earnings without requiring any further action when staking.

Yondon

- Should we create a blog post that udates delegators on the changes in the explorer?

Adam

- We can introduce a dismissible alert banner at the top of the explorer explaining the change

### LIP-56: Reward Period

Yondon

- Looking into splitting up the minter contract for greater flexibility.
- Hasn’t been much progress here. Moving forward, Nico will give updates on this specific proposal

### LIP-25: Extensible Governance Contract

Nico

- We've had the security review done
- We've addressed the recomendation in the security review
- One last follow up review, after which we can set this LIP to a proposed status
- Aiming for a deployment date at the end of October

Yondon

- One of the reasons this LIP was shelved was because there was a greater sense of urgency to

Eric

- I think there's a way to package this story in a way that's easier for tokenholders to understand

Yondon

- Perhaps having a separate poll description that's less technical would be a helpful tool highlighting why this LIP is important

Gavin

- Someone non-technical should be able to read 2 or 3 sentances and know whether they want to vote

Yondon

- This should be a prerequesite for this poll
