# LIP Meeting 6

**Meeting Date/Time**: Thursday August 20th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/9

**Recording**: https://youtu.be/Ierxk7FH_mE 

**Notes**: Yondon

## Agenda
<!-- Meeting agenda -->

- LIP candidates
    - [LIP-35: inflationChange Calculation and Parameter Update](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-35.md)
        - Post-poll check-in (there may or may not be anything that needs to be discussed there)
        - Champion: @viktorbunin
    - [LIP-25: Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/25)
        - Champion: @kyriediculous 
    - [LIP-36: Cumulative Earnings Claiming](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-36.md)
        - [Discussion](https://github.com/livepeer/LIPs/issues/35)
        - Champion: @yondonfu 
    - [Earnings Snapshot Proposal](https://github.com/livepeer/LIPs/issues/52)
        - Champion: @dob 
- Security audits for LIP-25 and LIP-36
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### LIP-35

Poll complete. LIP-34, LIP-35 and LIP-40 were assigned Final status after LIP-40 was deployed earlier this week. No further updates needed for this LIP.

### LIP-25

Currently in last call. Implementation just needs a final internal review. In conversation with an independent contractor to help with external security review. Should be able to kick off next week. Security review for LIP-25 is decoupled from that of LIP-36.

Next steps:
- External security review

### LIP-36

Implementation not as far along as LIP-25. Working on addressing a few remaining edge cases and updating the spec.

In conversation with a few external security review options.

Worth noting that:
- 100 round claim limit will be removed
- Right now gas cost of claiming increases linearly with # of rounds. After this LIP, gas cost of claiming will be constant regardless of the # of rounds
- Do not expect this to be contentious given that it represents tremendous cost savings for all tokenholders especially given the high gas prices on Ethereum right now

Next steps:
- Complete implentation
- Complete internal review
- Schedule external security review

### Earnings Snapshot Proposal

Nico is the technical co-champion of this LIP and has been working on a technical spec.

LIP-36 reduces cost going forwards, but this LIP would reduce costs for claiming for past rounds.

While this introduces externally injected state that is computed off-chain, the thought is that it can be acceptable because the state is approved via the governance process. All voters can check if the state is valid off-chain themselves when they decide whether to vote to approve or reject this LIP during a poll.

The technical changes in the contracts are relatively small. But, there will be some work to do off-chain so users can prove their stake/fees in the snapshot. Might be able to leverage existing tooling such as the subgraph for this.

An easy way to generate the proof can be hosted. The ways to generate the required data + proof will also be documented so that anyone can 1) verify the state themselves when voting in the poll 2) generate their own proofs if needed.

Next steps:
- Create formal LIP that includes the technical spec
- Start implementation
- Evaluate need for security review once the technical spec is fleshed out

### Security audits for LIP-25 and LIP-36

One for LIP-25 is close to being finalized.

One for LIP-36 is also in last conversations, but might not be able to start until September.

### Open Discussion

Doug: We should try to move quickly on LIPs that could help with the high gas prices issue on Ethereum
