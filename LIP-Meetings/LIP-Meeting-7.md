# LIP Meeting 7

**Meeting Date/Time**: Thursday September 3rd 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/10

**Recording**: https://youtu.be/q6I2DkY8yMU 

**Notes**: Yondon

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [LIP-25: Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/25)
        - Champion: @kyriediculous 
    - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/35)
        - Champion: @yondonfu 
    - [Earnings Snapshot Proposal](https://github.com/livepeer/LIPs/issues/52)
        - Champion: @dob 
        - Relationship with LIP-36 and whether the two LIPs need to be voted on/deployed around the same time
        - MVP requirements for client implementations to support snapshot proof generation
    - [LIP-56: Reward Period](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-56.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/56)
        - Champion: @yondonfu 
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-25

This LIP is pretty much ready for a vote - just needs final review for post-security review changes (no major findings - just a few notes for consideration that were incorporated into the implementation). But, we noted that the changes in this LIP are not changes that the community urgently cares about/needs right now. Combine that with the fact that voting is expensive right (even though the vote txs cost very little gas, with 500 gwei gas prices they'll still cost a couple of dollars) now due to high gas prices it might not be pragmatic to try to ask the community to pay attention to a vote for this LIP. Since we have the gas optimization LIPs in the pipeline it could make sense to focus on making those the next focal point for the community in a vote. Then, once some value is delivered with those LIPs we can revisit voting on this LIP. The main tradeoff with this decision is that we'll have to continue to manually go through multi-step upgrades for those gas optimization LIPs. 

Next steps
- Final review for the post-security review changes
- On hold until gas opimtization LIPs are voted on

### LIP-36

Kicking off a security review next week. Working on getting to a code/spec freeze before then.

Next steps
- Get into Last Call
- Security review next week

### LIP-52

Doug was wondering what would be faster/more practical given current resources: updating the explorer to support the earnings proof submission or creating a standalone tool that has a rougher UI/UX? Adam thinks that updating the explorer shouldn't take too long - that will be the plan.

This LIP requires LIP-36 (so that as soon as you claim from the snapshot you can use the more efficient claiming algo going forward without having to deal with iterative per round claiming) so it will need to be deployed after LIP-36. There is a question of whether we should bundle the two together. Arguments on both sides - bundling makes voting easier, but keeping separate allows voters to consider the LIPs separately. Defaulting to voting on them separately for now, but can adjust if needed later.

The soonest we could deploy LIP-36 + LIP-52 is by the week of September 21st.

Next steps:
- Get into Last Call
- Complete contract and proof generation implementation 

### LIP-56

Draft LIP created and draft implementation created. Still open to feedback - have received some initial feedback from Doug, but open to additional feedback especially from orchestrators since this LIP affects them the most. Want to move quickly though since reward calls have been really expensive with 500 gwei gas prices recently.

Next steps:
- Iterate on draft LIP & implementation
- Get into Last Call

### Open Discussion

Doug: Just putting this thought out there, but is there a way to speed up the process for getting all the gas cost optimization LIPs deployed? Maybe create a LIP with updates to the governance process?

Yondon: Yeah the only way to speed up the process while adhering to the current governance process is to create a LIP to reduce the Last Call and/or the poll period.

Acknowledged that it would take at least 20 days to pass a LIP that changes the Last Call and/or the poll period. This might not substantially speed up the process for the gas optimization LIPs. Might be more worthwhile to just focus on getting the gas optimization LIPs through the process ASAP instead of spending many mental cycles on an additional LIP for updating the governance process. That being said also acknowledged that it would be useful to consider changes to the governance process to accomodate for situations such as this one where there may not be a critical bug that needs to be fixed, but there is a sense of urgency for deploying certain features due to other factors (such as high gas prices).