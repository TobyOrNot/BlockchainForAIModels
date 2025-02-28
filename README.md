
Blockchain for the Management and Distribution of Machine Learning Models
📌 Project Overview
This project explores the integration of blockchain technology to decentralize the management and distribution of machine learning models, ensuring transparency, security, and accessibility. By leveraging Ethereum smart contracts, the platform enables users to interact with AI models while maintaining the integrity of model versions and ensuring fair access.

🚀 Key Features
✔ Decentralized AI Access – Users can retrieve and utilize a machine learning model via a blockchain-based infrastructure.
✔ Immutable Model Versioning – Ensures the integrity of AI models using smart contracts.
✔ Transparent and Secure Transactions – Leverages blockchain to record all interactions with the model.
✔ Ethereum Smart Contracts – Manages access, transactions, and updates of machine learning models.
✔ Efficient Model Execution – Implements an AI model (a sparse perceptron) for sentiment analysis of movie reviews.

🛠 Tech Stack
🔹 Blockchain: Ethereum, Solidity, Smart Contracts
🔹 Machine Learning: Python, NumPy, Scikit-learn (for perceptron model)
🔹 Backend: Node.js, Web3.js
🔹 Frontend: React, Next.js
🔹 Smart Contract Deployment: Hardhat

📖 How It Works
Model Deployment: The trained ML model is stored off-chain, with metadata and hash stored on Ethereum.
Smart Contracts: Contracts handle model access, updates, and verification.
User Interaction: Users submit data through a decentralized app (DApp) and receive predictions.
Blockchain Logging: Every interaction is securely logged for transparency.
🔧 Setup & Installation
1. Clone the Repository
sh
Copia
Modifica
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
2. Install Dependencies
sh
Copia
Modifica
npm install  # For the DApp
pip install -r requirements.txt  # For the ML model
3. Deploy Smart Contracts
sh
Copia
Modifica
npx hardhat compile
npx hardhat run scripts/deploy.js --network localhost
4. Run the Application
sh
Copia
Modifica
npm start
📜 Smart Contract Example (Solidity)
solidity
Copia
Modifica
pragma solidity ^0.8.0;

contract ModelRegistry {
    mapping(uint256 => string) public modelVersions;

    function addModelVersion(uint256 version, string memory modelHash) public {
        modelVersions[version] = modelHash;
    }

    function getModelVersion(uint256 version) public view returns (string memory) {
        return modelVersions[version];
    }
}
🌎 Documentation
📄 Full Thesis (Italian): [Link to PDF]

🏆 Authors
Tobias Paparelli - Blockchain & Machine Learning Integration
[Your Contact Info or LinkedIn]
🛡 License
📜 MIT License – Feel free to use, modify, and distribute with attribution.
