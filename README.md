# District Proposals
The district0x Network Token allows holders to signal for new districts to be built by the district0x Team. Prior to the launch of Aragon Core on the MainNet, signaling will be conducted via a custom CarbonVote implementation. The CarbonVote implementation is hosted at https://vote.district0x.io/ and is automatically populated with proposals that have been deemed as 'qualifying'.

## Qualifying Proposals
To be deemed as a 'qualifying proposal' the following conditions must be met:
* The proposal was submitted as an issue in the [district0x/district-proposals](https://github.com/district0x/district-proposals) repository
* The proposed district adheres to the [District Proposal Standard template](#district-proposal-standard)
* The proposed district is not unethical, as defined by the [district0x Network Code of Ethics](#district0x-network-code-of-ethics)

## District Proposal Standard
The District Proposal Standard is a template for proposals designed to ensure that submissions have been well thought through and contain a sufficient amount of supporting details for the community to make an informed decision in regards to its potential utility afforded. All proposals should be structured as follows:

**Name**: Provide a name of the proposed district. Ideally this would also be listed in the issue title/description.

**Purpose**: Define a purpose of the proposed district. Try to include a one liner with an additional paragraph if needed.

**Description**: Describe how the district should operate in detail. Include relationships between the district and users, tokenholders, and any other parts of the district0x network.

## district0x Network Code of Ethics
See [DGP 1](https://github.com/district0x/governance/issues/1) in 'issues' in the [district0x/governance](https://github.com/district0x/governance/) repository

## Proposal Incentives
To incentivize the submission of thoughtful district proposals, the following rewards will be issued:
* 250   DNT = Proposal submitted as issue, adheres to District Proposal Standard, and is ethical
* 500000 DNT = Proposal is launched as a new district on the district0x Network

If you would like your proposal to be considered for a reward, please be sure to include an ETH address in your proposal or in the comments. Alternatively, after completing the proposal, you may reach out to a district0x team member with this information on Slack.

Note: Proposal incentive reward amounts are subject to change in the event of abuse of the system

## How to vote from MyEtherWallet
1. Go to https://www.myetherwallet.com/#contracts
2. In the `Contract Address` field insert the contract address displayed on the voting interface
3. In the ABI / JSON Interface enter the following:
```
[{"constant":false,"inputs":[{"name":"candidate","type":"uint256"}],"name":"vote","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"offset","type":"uint256"},{"name":"limit","type":"uint256"}],"name":"getVoters","outputs":[{"name":"_voters","type":"address[]"},{"name":"_candidates","type":"uint256[]"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"votersCount","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"votes","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"voters","outputs":[{"name":"","type":"address"}],"payable":false,"type":"function"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"candidate","type":"uint256"}],"name":"onVote","type":"event"}]
```
4. Press `Access`
5. Select function -> `vote`
6. In the `Candidate` field put the number of your selection, which is shown as the `ID:` on the voting interface
7. Send the transaction. **No DNT is required to send**, but please ensure you have a very small amount of ETH (<0.001) to cover for the gas fee. The recommended gas limit is 100000.
