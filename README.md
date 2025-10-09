# Blockchain Developer Bootcamp - DApp University Token

A comprehensive full-stack blockchain project featuring an ERC-20 token implementation with React frontend, built for educational purposes as part of a blockchain developer bootcamp curriculum.

## 🚀 Project Overview

This project demonstrates the complete development lifecycle of a decentralized application (DApp), including:

- **Smart Contract Development**: Custom ERC-20 token implementation in Solidity
- **Testing Framework**: Comprehensive test suite using Hardhat and Chai
- **Frontend Integration**: React-based web application with blockchain interaction capabilities
- **Deployment Pipeline**: Hardhat deployment scripts for multiple networks
- **Contract Verification**: Etherscan integration for contract verification

## 🏗️ Architecture

### Smart Contract Layer
- **Token.sol**: Complete ERC-20 token implementation with standard functionalities
- **Network Support**: Configured for localhost development and Sepolia testnet
- **Security Features**: Input validation, overflow protection, and proper event emission

### Frontend Layer
- **React Application**: Modern React 18 with hooks and functional components
- **State Management**: Redux integration with middleware support
- **UI Components**: ApexCharts for data visualization, Blockies for address visualization
- **Web3 Integration**: Ready for MetaMask and other wallet connections

### Development Infrastructure
- **Hardhat Framework**: Complete development environment with testing and deployment
- **Testing Suite**: Comprehensive unit tests covering all contract functionalities
- **Environment Management**: Secure environment variable handling with dotenv

## 📁 Project Structure

```
blockchain-developer-bootcamp/
├── contracts/              # Smart contracts
│   └── Token.sol          # ERC-20 token implementation
├── scripts/               # Deployment scripts
│   └── 1_deploy.js       # Token deployment script
├── test/                  # Test files
│   └── Token.js          # Comprehensive token tests
├── src/                   # React frontend source
│   ├── App.js            # Main application component
│   ├── index.js          # React DOM entry point
│   └── ...               # Additional React components
├── public/                # Static assets
├── artifacts/             # Compiled contracts
├── cache/                 # Hardhat cache
├── hardhat.config.js     # Hardhat configuration
└── package.json          # Project dependencies
```

## 🛠️ Technologies Used

### Blockchain & Smart Contracts
- **Solidity ^0.8.0**: Smart contract programming language
- **Hardhat 2.9.1**: Ethereum development environment
- **Ethers.js 5.5.4**: Ethereum library for blockchain interaction
- **Waffle**: Smart contract testing framework
- **Chai**: Assertion library for testing

### Frontend Development
- **React 18.0.0**: Modern JavaScript library for user interfaces
- **Redux 4.1.2**: Predictable state container
- **React-ApexCharts**: Interactive data visualization
- **React-Blockies**: Ethereum address visualization
- **Moment.js**: Date and time manipulation

### Development Tools
- **dotenv**: Environment variable management
- **Lodash**: JavaScript utility library
- **Reselect**: Redux selector optimization

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MetaMask browser extension (for frontend interaction)
- Git

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/juanjoseexpositogonzalez/blockchain-developer-bootcamp.git
   cd blockchain-developer-bootcamp
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   PRIVATE_KEYS=your_private_key_here
   ALCHEMY_API_KEY=your_alchemy_api_key
   ETHERSCAN_API_KEY=your_etherscan_api_key
   ```

4. **Compile Smart Contracts**
   ```bash
   npx hardhat compile
   ```

5. **Run Tests**
   ```bash
   npx hardhat test
   ```

## 🚦 Usage Guide

### Smart Contract Operations

#### Local Development
1. **Start local blockchain**
   ```bash
   npx hardhat node
   ```

2. **Deploy to local network**
   ```bash
   npx hardhat run scripts/1_deploy.js --network localhost
   ```

#### Testnet Deployment (Sepolia)
```bash
npx hardhat run scripts/1_deploy.js --network sepolia
```

#### Contract Verification
```bash
npx hardhat verify --network sepolia CONTRACT_ADDRESS "Dapp University" "DAPPU" "1000000"
```

#### Available Networks
```bash
npx hardhat verify --list-networks
```

### Frontend Development

#### Development Mode
```bash
npm start
```
Opens the application at [http://localhost:3000](http://localhost:3000)

#### Production Build
```bash
npm run build
```
Creates an optimized production build in the `build` folder

#### Run Frontend Tests
```bash
npm test
```

## 🧪 Testing

The project includes comprehensive test coverage for the smart contract:

### Test Categories
- **Deployment Tests**: Verify correct contract initialization
- **Transfer Tests**: Test token transfer functionality
- **Approval Tests**: Test allowance mechanisms
- **Delegated Transfer Tests**: Test transferFrom functionality
- **Failure Cases**: Comprehensive error handling validation

### Running Specific Tests
```bash
# Run all tests
npx hardhat test

# Run with gas reporting
REPORT_GAS=true npx hardhat test

# Run specific test file
npx hardhat test test/Token.js
```

### Test Coverage
- ✅ Contract deployment and initialization
- ✅ Token transfers (success and failure scenarios)
- ✅ Approval mechanisms and allowances
- ✅ Delegated transfers via transferFrom
- ✅ Event emission verification
- ✅ Edge cases and error conditions

## 🎯 Smart Contract Features

### ERC-20 Standard Implementation
- **Name**: Dapp University
- **Symbol**: DAPPU
- **Decimals**: 18
- **Total Supply**: 1,000,000 tokens
- **Initial Distribution**: All tokens allocated to deployer

### Core Functions
- `transfer(address to, uint256 amount)`: Transfer tokens between addresses
- `approve(address spender, uint256 amount)`: Approve spending allowance
- `transferFrom(address from, address to, uint256 amount)`: Execute delegated transfers
- `balanceOf(address account)`: Check token balance
- `allowance(address owner, address spender)`: Check spending allowance

### Security Features
- Input validation for all functions
- Protection against zero address transfers
- Proper overflow/underflow protection
- Comprehensive event emission
- Reentrancy protection

## 🌐 Network Configuration

### Supported Networks
- **Localhost**: Local Hardhat network for development
- **Sepolia**: Ethereum testnet for testing and demonstration

### Network Details
```javascript
// Localhost
- Network: localhost
- Chain ID: 31337 (Hardhat default)

// Sepolia Testnet
- Network: sepolia  
- Chain ID: 11155111
- RPC: Alchemy provider
- Explorer: https://sepolia.etherscan.io/
```

## 📊 Contract Analytics

### Gas Optimization
The contract is optimized for gas efficiency:
- Efficient storage patterns
- Optimized function implementations
- Minimal external calls
- Proper data type usage

### Token Economics
- **Total Supply**: Fixed at 1,000,000 tokens
- **Distribution**: Centralized initial distribution
- **Transferability**: Full ERC-20 compatibility
- **Decimals**: Standard 18 decimal places

## 🔧 Development Workflow

### Recommended Development Process
1. **Smart Contract Development**
   - Write/modify Solidity contracts
   - Compile with `npx hardhat compile`
   - Run tests with `npx hardhat test`

2. **Frontend Development**
   - Develop React components
   - Test with `npm test`
   - Run development server with `npm start`

3. **Integration Testing**
   - Deploy contracts to local network
   - Test frontend integration
   - Verify end-to-end functionality

4. **Deployment**
   - Deploy to testnet
   - Verify contracts on Etherscan
   - Deploy frontend to hosting platform

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Standards
- Follow Solidity style guidelines
- Write comprehensive tests for new features
- Update documentation for API changes
- Ensure all tests pass before submitting

## 📝 License

This project is licensed under the UNLICENSED license - see the contract headers for details.

## 🎓 Educational Purpose

This project serves as a comprehensive learning resource for:
- Blockchain development fundamentals
- Smart contract programming in Solidity
- DApp frontend development with React
- Testing methodologies for blockchain applications
- Deployment and verification processes
- Web3 integration patterns

## 🔗 Useful Links

- [Hardhat Documentation](https://hardhat.org/docs)
- [Ethers.js Documentation](https://docs.ethers.io/)
- [OpenZeppelin Contracts](https://docs.openzeppelin.com/contracts/)
- [React Documentation](https://reactjs.org/docs)
- [Ethereum Development Documentation](https://ethereum.org/developers/)

## 📧 Support

For questions, issues, or contributions, please:
- Open an issue on GitHub
- Check existing documentation
- Review test cases for usage examples

---

**Built with ❤️ for the blockchain developer community**

*This project demonstrates real-world blockchain development practices and serves as a foundation for building more complex decentralized applications.*
