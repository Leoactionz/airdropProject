### Steps — to create SPL token project on CLI

```jsx
// create token
solana-keygen new

// check pubkey
solana-keygen pubkey

// check balance
solana balance --url devnet

// Drop some solana
solana airdrop 2 H8VpR9mqSnPaR9T2DCHhPbHaP4zj9z6SK2BznHyeHSN2 --url devnet

// check balance
solana balance --url devnet

// create account
spl-token create-account 9Ndpeimbh5SAgRKbXogiGe3jXP14Zm1Exh8DhVU4uZTL --url devnet

// check account balance of new account BpR...
spl-token balance --address BpRXuMxTPit5vQvCUEViU54hb54Dn9CpUm4TfakNhvMd --url devnet

// mint token for 9Nd...
spl-token mint 9Ndpeimbh5SAgRKbXogiGe3jXP14Zm1Exh8DhVU4uZTL 1000 --url devnet

// check account balance of new account BpR...
spl-token balance --address BpRXuMxTPit5vQvCUEViU54hb54Dn9CpUm4TfakNhvMd --url devnet

// Total number of new token(9Nd...) -- Circulating number of tokens used by Solana users
spl-token supply 9Ndpeimbh5SAgRKbXogiGe3jXP14Zm1Exh8DhVU4uZTL -u devnet

// Announce minting authority -- to avoid mint unlimited tokens
spl-token authorize 9Ndpeimbh5SAgRKbXogiGe3jXP14Zm1Exh8DhVU4uZTL mint --disable -u devnet

// Burn some tokens within account only
spl-token burn BpRXuMxTPit5vQvCUEViU54hb54Dn9CpUm4TfakNhvMd 100 -u devnet
Burn 100 tokens

// Transfer some tokens to a friend(new wallet address on devnet, you can use phantom) 
spl-token transfer 9Ndpeimbh5SAgRKbXogiGe3jXP14Zm1Exh8DhVU4uZTL 150 BZqeW1vPCPht7ecsMrWXtm3qWYSP7YfUbCPMzyt6mty4 -u devnet --allow-unfunded-recipient --fund-recipient

```
