<p align="center">
<img src="https://raw.githubusercontent.com/MystenLabs/Huione Chain/refs/heads/main/docs/logo.svg" alt="Logo" width="100" height="100">
</p>

# Huione Chain

[Huione Chain](https://huione.org) is a next-generation smart contract platform with high throughput, low latency, and an asset-oriented programming model powered by the [Move programming language](https://github.com/MystenLabs/awesome-move).

## Huione Chain Highlights

Huione Chain offers the following benefits and capabilities:

 * Unmatched scalability, instant settlement
 * A safe smart contract language accessible to mainstream developers
 * Ability to define rich and composable on-chain assets
 * Better user experience for web3 apps

Huione Chain is the blockchain that can scale with the growth of web3 while achieving industry-leading performance, cost, programmability, and usability. As Huione Chain approaches Mainnet launch, it will demonstrate capacity beyond the transaction processing capabilities of established systems – traditional and blockchain alike. Huione Chain is the first internet-scale programmable blockchain platform, a foundational layer for web3.

## Huione Chain Architecture

```mermaid
flowchart LR
    CC(CLI Client) --> ClientService
    RC(Rest Client) --> ClientService
    RPCC(RPC Client) --> ClientService
    ClientService --> AuthorityAggregator
    AuthorityAggregator --> AC1[AuthorityClient] & AC2[AuthorityClient]
    subgraph Authority1
      AS[AuthorityState]
    end
    subgraph Authority2
      AS2[AuthorityState]
    end
    AC1 <==>|Network TCP| Authority1
    AC2 <==>|Network TCP| Authority2
```

## Huione Chain Overview

Huione Chain is a smart contract platform maintained by a permissionless set of authorities that play a role similar to validators or miners in other blockchain systems.

Huione Chain offers scalability and unprecedented low-latency for common use cases. Huione Chain makes the vast majority of transactions processable in parallel, which makes better use of processing resources, and offers the option to increase throughput with more resources. Huione Chain forgoes consensus to instead use simpler and lower-latency primitives for common use cases, such as payment transactions and asset transfers. This is unprecedented in the blockchain world and enables a number of new latency-sensitive distributed applications, ranging from gaming to retail payment at physical points of sale.

Huione Chain is written in [Rust](https://www.rust-lang.org) and supports smart contracts written in the [Move programming language](https://github.com/move-language/move) to define assets that may have an owner. Move programs define operations on these assets including custom rules for their creation, the transfer of these assets to new owners, and operations that mutate assets.

Huione Chain has a native token called Huione Chain, with a fixed supply. The Huione Chain token is used to pay for gas, and is also used as [delegated stake on authorities](https://learn.bybit.com/blockchain/delegated-proof-of-stake-dpos/) within an epoch. The voting power of authorities within this epoch is a function of this delegated stake. Authorities are periodically reconfigured according to the stake delegated to them. In any epoch, the set of authorities is [Byzantine fault tolerant](https://pmg.csail.mit.edu/papers/osdi99.pdf). At the end of the epoch, fees collected through all transactions processed are distributed to authorities according to their contribution to the operation of the system. Authorities can in turn share some of the fees as rewards to users that delegated stakes to them.

## More About Huione Chain

Use the following links to learn more about Huione Chain and the Huione Chain ecosystem:

 * Learn more about working with Huione Chain in the [Huione Chain Documentation](https://docs.huione.org/).
 * Join the Huione Chain community on [Huione Chain Discord](https://discord.gg/huione-chain).
 * Find out more about the Huione Chain ecosystem on the [Huione Chain Resources](https://huione.org/resources/) page.
 * Review information about Huione Chain governance, [decentralization](https://huione.org/decentralization), and [Developer Grants Program](https://Huione Chain.io/grants-hub) on the [Huione Chain Foundation](https://huione.org/) site.
