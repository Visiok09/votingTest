This smart contract that implements a voting system. Here's a description of its key components and functionalities:

Contract Variables:

owner: Stores the address of the contract owner.
counter: Keeps track of the number of voting instances created.
maxCandidatesNum: Defines the maximum number of candidates allowed in a voting instance.
Comission: Represents the commission percentage for the contract owner.
Structs:

Candidate: Represents a candidate in the voting, storing their balance and existence status.
Voting: Represents a voting instance, storing information such as whether it has started, the winner, start date, winner's balance, bank balance, period, and a mapping of candidates.
Mapping:

Votings: Maps voting IDs to their respective voting instances.
Constructor:

Initializes the contract owner and sets the maximum number of candidates and commission percentage.
Public Functions:

takePartInVoting: Allows participants to deposit funds and vote for a candidate in an active voting instance.
WithdrowMyPrize: Allows the winner to withdraw their prize after the voting period is over.
getVotingInfo: Retrieves the information of a specific voting instance.
checkCandidate: Checks if a candidate exists in a specific voting instance.
Owner-Only Functions:

addVoting: Allows the contract owner to create a new voting instance with a specified period and candidate addresses.
startVoting: Starts a specific voting instance.
editVotingPeriod: Allows the contract owner to edit the period of a specific voting instance.
addCandidate: Allows the contract owner to add a candidate to a specific voting instance.
deleteCandidate: Allows the contract owner to remove a candidate from a specific voting instance.
setMaxCandidatesNum: Allows the contract owner to set the maximum number of candidates.
Modifiers:

onlyOwner: Restricts access to functions only to the contract owner.
```shell
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat run scripts/deploy.js
```
