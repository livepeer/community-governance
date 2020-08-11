# LIP Meeting 5

**Meeting Date/Time**: Thursday August 6th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/7

**Recording**: https://youtu.be/OP6fIN1rFek

**Notes**: Adam Soffer

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [LIP-35: inflationChange Calculation and Parameter Update](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-35.md)
        - [Technical update discussion](https://github.com/livepeer/LIPs/issues/34)
        - [Parameter update discussion](https://github.com/livepeer/LIPs/issues/40)
        - Champion: @viktorbunin
    - [LIP-25: Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/25)
        - Champion: @kyriediculous 
    - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/35)
        - Champion: @yondonfu 
- Security audits for LIP-35, LIP-25 and LIP-36
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-35: Inflation Change proposal

Yondon
- Ready to create a poll for LIP 35

Viktor
- Will create the poll later today. Just waiting for team to send over the token to cover creation cost

Doug
- Going to share updates in our discord channels. 
- Will send out a tweet about it
- Might start a forum AMA thread in case people have questions
- There’s a community call next week. Will be a good last chance for community to ask some questions

Viktor
- Bison Trails will tweet it out

Doug
- If the poll passes, would we be in position to execute within hours, days, weeks? What’s the estimated timeline?

Yondon
- The estimated timeline will be days. After the poll is complete, if it is accepted we should be equipped to execute.

### LIP-25: Extensible Governance Contract

Nico
- Implementation wise it’s close. One discussion point that remains is whether we should keep the nonce. Not needed but it’s a potential way to ensure proper ordering of events in case multiple events are in the same block
- We can move to last call now or resolve the discussion point for and then move to laast call

Yondon
- Don’t see a benefit in the contract nonce. We can discuss in the PR review. 


### LIP-36: Cumulative Earnings Claiming

Yondon
- We have a WIP implementation that needs review

Nico
- The spec hasn’t been updated. Will update by tomorrow

Doug
- The cost to claim earnings is very high due to high gas prices. Particular for users who have a low value staked for a long time. There’s likely hundreds of users in this scenario
- There is an opportunity to use a snapshot based approach that would allow them to submit one transaction that moves their LPT rewards from the minter to their account.
- Beginning of an idea, not a completed thought yet but thought it would be good to have a discussion on it and see if it’s viable

Nico
- This snapshot mechanism doesn’t need to be tightly coupled to LIP-36. It could be a separate LIP

Yondon
- Like the points made around reviewing the snapshot in the period before or during the poll because the community can come to consensus


### Security audits for LIP-35, LIP-25 and LIP-36
Yondon:
- Given that the scope of LIP-35 is small it’s appropriate to proceed with internal security review with members of the Livepeer core team
- For LIP-25, and LIP-36, it feels more appropriate to take additional steps. Have been in communication with a few external firms to understand availability in the new month sa well as cost. The goal of this engagement would be to have an extra set of eyes and checks for correctness.
- Have spoken with Trail of Bits but is not a available. Waiting to hear back about from Consensys Diligence and Zeppelin. 
- Might be worth exploring some security tools internally


### Open Discussion

Nico
- Would be nice if an orchestrator could specify recipient address for winning tickets

Yondon
- There’s nothing preventing orchestrator to be a smart contract 
