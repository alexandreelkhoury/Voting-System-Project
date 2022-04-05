# Alyra Test Voting

## Unit tests
27 tests valides

Toutes les fonctions du contrat sont testées

1 file: Voting.js

### 1) ---Registering Voters---

- should make sure status is at registering voters
- should add a voter and emit event
- shouldn't add a voter if the voter is already registered
- shouldn't add a voter if it is not the owner
- shouldn't add a voter if the workflow status is not set at RegisteringVoters


### 2) ---Proposals Registration Started---

- should start proposal registration
- shouldn't start the proposals registering if it is not the owner
- shouldn't start the proposals registering if the workflow status is not set at RegisteringVoters
- should add a proposal and emit event
- shouldn't add a proposal if it is not a voter
- shouldn't add a proposal if the workflow status is not set to RegisteringVoters


### 3) ---Ending Proposal Registration---

- shouldn't end the proposals registering if it is not the owner
- shouldn't end the proposals registering if the workflow status is not set at ProposalsRegistrationStarted
-should end proposal registration

### 4) ---Voting Session Started---

- should start voting session
- should set a vote and emit event
- shouldn't set a vote if it is not a voter
- shouldn't set a vote if the voter has already voted
- shouldn't set a vote if the workflow status is not set at VotingSessionStarted
- shouldn't start the voting session if it is not the owner
- shouldn't start the voting session if the workflow status is not set at ProposalsRegistrationEnded

### 5) ---Ending Voting Session---

- should end voting voting session
- shouldn't end the voting session if it is not the owner
- shouldn't end the voting session if the workflow status is not set at VotingSessionStarted

### 6) ---Votes Tallied---

- shouldn't tally votes if the workflow status is not set at VotingSessionEnded
- should tally votes and get the winning proposal ID
- shouldn't tally votes if it's note the owner calling the function

