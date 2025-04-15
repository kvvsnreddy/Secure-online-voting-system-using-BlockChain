🗳️ Aqua: A Blockchain-Based Multi-Winner E-Voting System
License

GitHub Stars

Issues

🌟 About Aqua
Aqua is a decentralized, secure, and transparent e-voting system built on the Ethereum blockchain. It leverages blockchain technology to ensure fairness, immutability, and trust in the voting process. Designed for multi-winner elections , Aqua supports committee sizes up to 3 members and implements the Approval Voting (AV) rule to compute results.

Whether you're running a small community election or a large-scale decision-making process, Aqua provides a user-friendly, cost-effective, and accessible solution that can be used from any device with an internet connection.

🔧 Key Features
Decentralized & Immutable : Powered by blockchain, Aqua ensures votes are tamper-proof and verifiable.
Multi-Winner Elections : Supports committee elections with up to 3 members using Approval Voting.
User-Friendly Interface : Simple and intuitive front-end for voters and administrators.
Secure & Transparent : Utilizes smart contracts to automate and secure the voting process.
Cross-Platform Accessibility : Accessible from any device with an internet connection.
Cost-Effective : Minimal gas fees for deploying and interacting with the smart contract.
Multi-Language Support : Available in both English and Greek.
🚀 Getting Started
Prerequisites
Node.js : Download Node.js
Metamask Wallet : Install the MetaMask browser extension .
Ethereum Testnet (Goerli) : Use the Goerli testnet for testing purposes. Get free test ETH from a faucet like Goerli Faucet .
Installation
Clone the Repository :
bash

git clone https://github.com/NikStef/AquaBlockchainVoting-english-version.git
cd AquaBlockchainVoting-english-version
Install Dependencies :
bash

npm install
Set Up Environment Variables :
Create a .env file in the root directory and add your Ethereum private key and network details:

env

PRIVATE_KEY=your_private_key_here
INFURA_API_KEY=your_infura_api_key_here
Deploy the Smart Contract :
Use Hardhat to deploy the Aqua.sol smart contract:
bash

npx hardhat run scripts/deploy.js --network goerli
Run the Front-End :
Start the development server:
bash

npm start
Connect MetaMask :
Open your browser, connect your MetaMask wallet, and navigate to http://localhost:3000.
📜 How It Works
1. Initialization
The VotingInitiator deploys the smart contract and sets up the election parameters (e.g., committee size, candidates).
2. Registration
Voters and candidates are registered during this phase. Only registered voters can participate.
3. Voting
Eligible voters cast their approval votes via the Aqua interface. Votes are recorded on the blockchain.
4. End Phase
The VotingInitiator ends the election, computes the results, and announces the winning committee.
📊 Example Election
Candidates :
Parisis Nikolaos
Gialamas Aggelos
Rapti Ioanna
Danika Maria
Georgiou Alexhs
Voter Preferences :
Voter 1: {Parisis Nikolaos, Rapti Ioanna, Georgiou Alexhs}
Voter 2: {Gialamas Aggelos, Danika Maria}
Voter 3: {Rapti Ioanna, Danika Maria, Georgiou Alexhs}
Winning Committee :
{Georgiou Alexhs, Danika Maria, Rapti Ioanna}
🛠️ Smart Contract Functions
VotingInitiator Functions
setCandidate(string name): Add a candidate during the "Registration" phase.
setVoter(address voterAddress): Register a voter during the "Registration" phase.
changePeriod(string newPeriod): Transition between phases (e.g., "Register" → "Voting").
getResults(): Compute and display the winning committee during the "End" phase.
Voter Functions
castVote(uint[] approvedCandidates): Cast approval votes during the "Voting" phase.
Public View Functions
getState(): Check the current voting period.
getCandidateLength(): Get the total number of candidates.
getVoterLength(): Get the total number of registered voters.
getCandidateName(uint id): Retrieve the name of a candidate by ID.
📂 Project Structure

AquaBlockchainVoting/
├── contracts/               # Smart contract files (Aqua.sol)
├── scripts/                 # Deployment scripts
├── public/                  # Static assets (HTML, CSS, images)
├── src/                     # Front-end source code
│   ├── components/          # React components
│   ├── pages/               # Application pages
│   └── App.js               # Main application file
├── .env                     # Environment variables
├── package.json             # Dependencies and scripts
└── README.md                # This file!
🤝 Contributing
We welcome contributions! Whether you're fixing bugs, adding features, or improving documentation, your help is appreciated. Follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/YourFeatureName).
Commit your changes (git commit -m "Add feature XYZ").
Push to the branch (git push origin feature/YourFeatureName).
Open a pull request.
