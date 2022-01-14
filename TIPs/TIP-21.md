

| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| TIP-21 | TWAP Price Feeds deployment | Draft | padzank (@padzank) | Deploy Optimism Uniswap V3 TWAP function in the PriceFeed.sol contract and enable market creation around the price feeds of Uniswap V3 pools on Optimism | https://discord.gg/rPpPcMXSeU | 2022-02-14

## Simple Summary

This TIP proposes to deploy Optimism Uniswap V3 TWAP function in the PriceFeed.sol contract and enable market creation around the price feeds of Uniswap V3 pools on Optimism

## Abstract

Thales has, so far, supported Chainlinks tamper-proof Data Feeds as exclusive on-chain feeds for resolving Thales markets. To add some more versatility to the Thales marketplace and expand it's reach, this TIP proposes to integrate Optimism Uniswap V3 TWAP oracle into Thales and allow for creation of markets around any asset that has a pool on Uniswap V3 on Optimism.

## Motivation

The security and decentralization that Chainlink Data Feeds offer are detrimental to the success of Thales that provides it's users an on-chain, permissionless, and non-custodial way to participate in the price and variable movements of various supported assets. While constantly communicating with Chainlink labs and frequently integrating novel Data Feeds from them that are viable for market creation, Thales is always looking to in parallel to expand it's capabilities and offer it's users novel markets.  
As Uniswap V3 TWAP oracle offers on-chain data feeds around price of pooled assets, it is a perfect fit for Thales to allow creation of exotic and volatile markets not yet offered by Chainlink on Optimism. Before deploying this type of market, however, there needs to be a thorough research of the amount of liquidity for a certain pool aimed to be deployed and risk assesment of the manipulation probability. If the research shows that the certain TWAP feed has low risk of showing nonfactual result and that is not economically feasible to manipulate the said price feed for the goal of also manipulation Thales market resolution (assets pool liquidity is greater than a certain threshold and has low chance of being reduced while Thales market is in trading phase), the said market can be deployed on the Thales marketplace.  
This novel type of Data Feeds can also provide a powerful marketing tool when doing initiatives together with other protocols/projects that have assets pooled in Uniswap V3 protocol on Optimism.

## Specification

 - This TIP entails Thales ProtocolDAO to modify the [PriceFeed.sol](https://github.com/thales-markets/contracts/blob/main/contracts/PriceFeed/PriceFeed.sol) contract so it additionally integrates Uniswap V3 TWAP oracle on Optimism for market creation.

 - This integration would allow the PriceFeed.sol contract to take in any Uniswap V3 pool address and output the Time-weighted Averaged Price from that specific pool in time interval chosen by the ProtocolDAO after researching the said pool and deriving the most optimal value.


## Rationale

n/a

## Test Cases

n/a

## Implementation

n/a

## Copyright

Copyright and related rights waived via CC0.