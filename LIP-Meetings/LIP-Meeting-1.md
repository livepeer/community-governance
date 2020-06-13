# LIP Meeting 0

**Meeting Date/Time**: Thursday June 11th 2020, 17:00 UTC

**Meeting Duration**: 1 hour

**GH Agenda**: https://github.com/livepeer/community-governance/issues/2

**Recording**: https://www.youtube.com/watch?v=dbI1d6BA2K8

**Notes**: Yondon Fu

## Agenda
<!-- Meeting agenda -->

- LIP candidates
  - [Extensible Governance Contract](https://github.com/livepeer/LIPs/blob/master/LIPs/LIP-25.md)
    - [Design discussion](https://github.com/livepeer/LIPs/issues/25)
    - [Parameter discussion](https://github.com/livepeer/LIPs/issues/30)
- Open discussion period (5-10 minutes)

## Notes

Note: While the writing below attributes ideas to certain people, it was a best attempt at capturing the dialogue during the meeting and is not necessarily a word for word representation for what was said during the meeting.

### Extensible Governance Contract

What are the major open discussion points?
- RBAC vs. address based control
- Modular delay vs. global delay
- Initial parameters in the system

Seems like we have rough consensus that RBAC would be a good idea, but we're wary about the benefit vs. engineering cost tradeoff. We may be able to use open source libraries here. Something to consider there is whether the libraries have been vetted or now. Two paths: If the library is already audited great. If not, we can consider the library code in scope for the security review that we would do (audit and/or bug bounty) for this sytem

Unbonding period could change
Right now it is a week, but there were thoughts around extending it to multiple months
If it was couple months it would not be reasonable for the delay to be based off of it

For any contentious topic, you need to stay bonded until the very end of the poll.
Let's base delay decision with assumption that voters are bonded until the end of the poll to account for that
i.e. We should not make assumptions about it being ok for the delay to be shorter just because we think voters could unbond before the end of a poll - we usually cannot considert he decision of a poll final until it ends especially if it is contentious.

Would be interested in keeping people bonded after for longer if they vote Yes, but not sure how feasible it is right now. We can consider this separately.

Delay also gives clear transparency for when upgrade will happen so people can prepare

How do you upgrade this governance contract?
You can transfer ownership of Controller to a new contract

Should we formalize the notion of a security commiteee if we're using a RBAC?
Community opt-in for the status quo
Let's add this to the agenda for next time

### Open Discussion

Did anyone think more about sentiment polls from last time?
Doug: Let's start lighterweight and engage with forum, discussion posts first

Gavin: Numbered option in a poll? i.e. Ranked choice list
Could definitely be useful for gauging sentiment
Harder to use this for determining if a proposal is executed or not
Yondon: I think MakerDAO uses a continuous voting system that allows proposals to be continuously submitted and the one with the most support is used

### TODOs

- Research RBAC implementations - can we use an open source implementation? How generic is it?
- Based on RBAC research, decide how to implement modular delay i.e. per role or per action per role?
- Consider formalizing notion of security committee next time
