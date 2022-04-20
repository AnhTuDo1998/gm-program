# Overview
Codes from the Solana bootcamp hosted by Chainlink

# How to run

## Compile
To compile the solana program:
```
cargo build-bpf --manifest-path=./Cargo.toml --bpf-out-dir=dist/program
```

## Select & Run test cluster
You will need to install the Solana CLI first before selecting the test cluster (either local or remote devnet)
```
sh -c "$(curl -sSfL https://release.solana.com/stable/install)
```

Test your installation:
```
solana --version
```

### Local cluster
Select local cluster for testing and deploy.
```
solana config set --url localhost
```

Create a new keypair/wallet for interacting on our local validator node:
```
solana-keygen new
```

Start local validator
```
solana-test-validator
```

### Test Devnet
Change the endpoint of your CLI to the devnet and also asking for some funds
```
solana config set --url https://api.devnet.solana.com
solana airdrop 2 
```

## Deploy program
To deploy your smart-contract/program (replace with path to compiled library as needed):
```
solana program deploy dist/program/gm_program.so
```

# Bootcamps docs
For more information on the bootcamp: 
- [setup guide](https://docs.google.com/document/d/e/2PACX-1vTf4o3Va9TrwsFpYDnTLB8LpIwK1MUh0WIBtajio-Jk78aWlIKF-87BfFdRG2HcfExIq3WIFut_IwdA/pub?_hsmi=2&_hsenc=p2ANqtz-8PahmymbTCyCxBlhjA4S8Sev1tfmKz6UGUOCWhuFz8egxRAvCZxQ-WM1DIdajYi5BN95NRCYT0zyk5WVl67OwYHDq4CbYWdsb7aAy6UgficX4PcZE)
- [day 1 excercises](https://docs.google.com/document/d/e/2PACX-1vSOgwdz9-vpBDwh3Epr3fdjzGyMWB1GHNT4H7YysNRyBFRJ0_qpcafgGcZUgNJLoyTH9IBVBaaInHsc/pub)
- [day 2 excercises](https://docs.google.com/document/d/e/2PACX-1vTm2gQPzKGtoZtTeXJGw6ux69gKDrAtiC8qD6GqWTQwfLaokAv9nnTgnGaniHOOLTZoKosRy0FgvGVy/pub)
