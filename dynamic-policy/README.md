# Decentralized Insurance Smart Contract

## About
A robust and feature-rich smart contract implementation for decentralized insurance on the Stacks blockchain using Clarity. This contract enables automated insurance policy management, risk assessment, claims processing, and staking mechanisms.

## Features
### Core Functionality
- Multi-tier insurance policies
- Dynamic premium calculation
- Automated claims processing
- Risk assessment system
- Staking mechanism with rewards
- Comprehensive policy management
- Evidence-based claims verification

### Advanced Features
- Risk-based pricing
- Cooldown periods for claims
- Stake-weighted risk calculations
- Tier-based coverage multipliers
- Dynamic premium adjustments
- Reward distribution system

## Architecture

### Data Storage
1. **Policy Management**
   - Policy details stored in `insurance-policies` map
   - Tier information in `policy-tiers` map
   - Risk profiles in `risk-profiles` map

2. **Claims Processing**
   - Claims data stored in `insurance-claims` map
   - Evidence hashing for verification
   - Verdict and payout tracking

3. **Staking System**
   - Staker information in `staker-info` map
   - Reward calculations and distribution
   - Lock periods and cooldowns

### Core Variables
```clarity
reserve-pool: Total insurance reserve
stake-pool: Total staked amount
protocol-owner: Contract administrator
base-premium: Minimum premium amount
claim-ceiling: Maximum claim amount
```

## Contract Components

### 1. Policy Management
- Policy creation and modification
- Premium calculation based on risk
- Coverage limits and restrictions
- Policy expiration handling

### 2. Claims Processing
- Claim submission with evidence
- Automated validation
- Verdict assignment
- Payout processing

### 3. Risk Assessment
- Dynamic risk scoring
- Claim history evaluation
- Stake-weighted calculations
- Duration multipliers

### 4. Staking Mechanism
- Token staking
- Reward distribution
- Lock periods
- Minimum stake requirements

## Policy Tiers

### Basic Tier
- Standard coverage
- No premium discount
- Minimum stake requirement: 1M uSTX

### Premium Tier
- 2x coverage multiplier
- 10% premium discount
- Minimum stake requirement: 2M uSTX

### Elite Tier
- 3x coverage multiplier
- 20% premium discount
- Minimum stake requirement: 3M uSTX

## Risk Assessment

### Factors Considered
1. Base risk score
2. Claim history
3. Stake weight
4. Policy duration

## Setup and Deployment

### Prerequisites
- Stacks blockchain environment
- Clarity CLI tools
- STX tokens for deployment

### Deployment Steps
1. Initialize contract
2. Set up policy tiers
3. Configure base parameters
4. Verify deployment

## Security Considerations

### Access Control
- Protocol owner permissions
- Claim assessor validation
- Stake verification

### Risk Mitigation
- Cooldown periods
- Maximum coverage limits
- Minimum stake requirements
- Evidence verification

### Error Handling
- Comprehensive error codes
- Transaction validation
- Parameter checking

## Error Codes
```clarity
ERR-UNAUTHORIZED (u1): Unauthorized access attempt
ERR-NO-POLICY-EXISTS (u2): Policy not found
ERR-FUNDS-INSUFFICIENT (u3): Insufficient funds
ERR-INVALID-PARAMETERS (u4): Invalid input parameters
ERR-POLICY-TERMINATED (u5): Policy has expired
ERR-DUPLICATE-CLAIM (u6): Claim already exists
ERR-INVALID-CLAIM-DATA (u7): Invalid claim data
ERR-STAKE-TOO-LOW (u8): Insufficient stake amount
ERR-COOLDOWN-ACTIVE (u9): Cooldown period active
ERR-RISK-SCORE-HIGH (u10): Risk score too high
```