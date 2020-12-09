# [ROADMAP](https://github.com/dOrgTech/OpenRaise/blob/master/docs/Roadmap.md)

> A Toolkit for accountable on-chain fundraising, and being developed through a collaboration by [dOrg](https://dorg.tech/#/) and [Level K](https://www.levelk.io/). [DXdao](https://dxdao.daostack.io/) commissioned them to develop its fundraiser dapp using [@FairmintCO](https://twitter.com/FairmintCO) smart contracts. DXdao recently ratified the configuration parameters, including pre-mint, curve slope, dividend split, and kickstarter threshold.

# OpenRaise

> "Accountable fundraising for the next generation of decentralized organizations"

⚠️ These contracts are in beta and have not been audited, do not use these contracts in production.

Blockchain, and Ethereum in particular, promises to reshape capital formation. However, the ICO craze of 2017 demonstrated the need for accountability, giving rise to new models for fundraising such as Continuous Organizations and DAICOs. Open Raise is a modular library of smart contracts and UI components that bring these ideas to life and make it easy for organizations to run accountable fundraising campaigns. The first release will support curve bonded token sales with self-enforcing dividend claims. The roadmap (see below) consists of adding DAICO support and modularizing the code before integrating with popular DAO frameworks and supporting additional functionality.

## Fundraising Mechanisms

- [Bonding Curves](./docs/BondingCurve.md)
- [DAICO](./docs/DAICO.md)

## Token Features

- [Dividend Claims](./docs/DividendToken.md)

## Example

**DAO Reserve (amount and vesting period)**

100,000 DXD Tokens will be issued to the dxDAO in a pre-mint, vested monthly over 3 years (i.e. 1/36th = ~2775 DXD will be vested each month for 3 years)

**Curve slope / issuance**

The curve slope is linear, as per the cOrg model.

Will be calculated such that 300,000 USD (in ETH, at current market price) would be raised in exchange for 12,000 DXD, or about 11% of the total supply.

**Kickstarter goal**

This is a minimum threshold for the fundraise, until which point investors can withdraw the entirety of their investment.

Will be set to an amount equivalent to 50,000 USD denominated in ETH using current market price at deployment.

**Reserve percentage**

A portion of the collateral invested in the curve is held in reserve to facilitate sell orders (providing a liquidity guarantee).

Will be set at 10% as per cOrg model recommendations. Investors want their money to be used to grow the dxDAO, not sit in reserve.

**Dividend percentage**

A portion of revenue is allocated to the reserve, increasing the value of all outstanding bonding curve tokens.

Will be set to 10% of the revenue, for a minimum of 5 years. The duration of revenue allocation here can be increased at a later date, but never decreased.
