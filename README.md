<p align="center">
  <img src="https://github.com/iotexproject/ioTube/blob/master/ioTube.png" width="480px">
</p>

&nbsp;

# ioTube
A decentralized bridge between Ethereum and IoTeX for exchanging native coins and ERC20/XRC20 tokens

## Deploy on IoTeX
* Deploy a MinterPool `mp`
* Deploy a TokenList `tl`
* Deploy a VoterList `vl`
* Deploy a BurnableTokenCashier with `tl`
* Deploy a TransferValidatorWithMinterPool with `mp`, `tl`, `vl`
* Transfer ownership of `mp` to the TransferValidatorWithMinterPool
* Add voters to `vl`

## Deploy on Ethereum
* Deploy a TokenSafe `ts`
* Deploy a TokenList `tl`
* Deploy a VoterList `vl`
* Deploy a TokenCashierWithSafe with `tl` and `ts`
* Deploy a TransferValidatorWithTokenSafe with `ts`, `tl`, and `vl`
* Transfer ownership of `ts` to the TransferValidatorWithTokenSafe
* Add voters to `vl`

## Build a tube for an ERC20 token
* Add this token to `tl` on Ethereum
* Deploy a ShadowToken and add it to `tl` on IoTeX
