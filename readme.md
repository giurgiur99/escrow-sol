# Solana Escrow Program

A secure token swap implementation on Solana blockchain that enables trustless exchanges between two parties (Alice and Bob). The program demonstrates atomic swaps of SPL tokens using an escrow mechanism.

## Features

- Atomic token swaps between two parties
- Support for SPL Token and Token-2022 programs
- Secure vault system for holding tokens during the exchange
- Complete test suite demonstrating the escrow workflow

## How it Works

1. **Initialization**: Creates test accounts for Alice and Bob, along with two different token mints (Token A and Token B)

2. **Make Offer**:

   - Alice creates an escrow offer by specifying:
     - Amount of Token A to offer
     - Amount of Token B wanted in return
   - Tokens are securely locked in a program-controlled vault

3. **Take Offer**:
   - Bob can accept the offer by providing the requested Token B amount
   - The program atomically swaps:
     - Token A from vault to Bob
     - Token B from Bob to Alice

## Technical Stack

- Solana Web3.js
- Anchor Framework
- SPL Token Program
- TypeScript
- Mocha Test Framework

## Prerequisites

- Node.js
- Solana Tool Suite
- Anchor Framework

## Security

This implementation includes:

- Program-derived addresses (PDAs) for secure token storage
- Proper account validation
- Atomic transaction execution
