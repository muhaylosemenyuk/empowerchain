## empowerd tx gov submit-legacy-proposal

Submit a legacy proposal along with an initial deposit

### Synopsis

Submit a legacy proposal along with an initial deposit.
Proposal title, description, type and deposit can be given directly or through a proposal JSON file.

Example:
```bash
$ empowerd tx gov submit-legacy-proposal --proposal="path/to/proposal.json" --from mykey
```

Where proposal.json contains:

{
  "title": "Test Proposal",
  "description": "My awesome proposal",
  "type": "Text",
  "deposit": "10test"
}

Which is equivalent to:

$ empowerd tx gov submit-legacy-proposal --title="Test Proposal" --description="My awesome proposal" --type="Text" --deposit="10test" --from mykey

```
empowerd tx gov submit-legacy-proposal [flags]
```

### Options

```
  -a, --account-number uint      The account number of the signing account (offline mode only)
      --aux                      Generate aux signer data instead of sending a tx
  -b, --broadcast-mode string    Transaction broadcasting mode (sync|async) (default "sync")
      --chain-id string          The network chain ID
      --deposit string           The proposal deposit
      --description string       The proposal description
      --dry-run                  ignore the --gas flag and perform a simulation of a transaction, but don't broadcast it (when enabled, the local Keybase is not accessible)
      --fee-granter string       Fee granter grants fees for the transaction
      --fee-payer string         Fee payer pays fees for the transaction instead of deducting from the signer
      --fees string              Fees to pay along with transaction; eg: 10uatom
      --from string              Name or address of private key with which to sign
      --gas string               gas limit to set per-transaction; set to "auto" to calculate sufficient gas automatically. Note: "auto" option doesn't always report accurate results. Set a valid coin value to adjust the result. Can be used instead of "fees". (default 200000)
      --gas-adjustment float     adjustment factor to be multiplied against the estimate returned by the tx simulation; if the gas limit is set manually this flag is ignored  (default 1)
      --gas-prices string        Gas prices in decimal format to determine the transaction fee (e.g. 0.1uatom)
      --generate-only            Build an unsigned transaction and write it to STDOUT (when enabled, the local Keybase only accessed when providing a key name)
  -h, --help                     help for submit-legacy-proposal
      --keyring-backend string   Select keyring's backend (os|file|kwallet|pass|test|memory) (default "os")
      --keyring-dir string       The client Keyring directory; if omitted, the default 'home' directory will be used
      --ledger                   Use a connected Ledger device
      --node string              \<host\>:\<port\> to tendermint rpc interface for this chain (default "tcp://localhost:26657")
      --note string              Note to add a description to the transaction (previously --memo)
      --offline                  Offline mode (does not allow any online functionality)
  -o, --output string            Output format (text|json) (default "json")
      --proposal string          Proposal file path (if this path is given, other proposal flags are ignored)
  -s, --sequence uint            The sequence number of the signing account (offline mode only)
      --sign-mode string         Choose sign mode (direct|amino-json|direct-aux), this is an advanced feature
      --timeout-height uint      Set a block timeout height to prevent the tx from being committed past a certain height
      --tip string               Tip is the amount that is going to be transferred to the fee payer on the target chain. This flag is only valid when used with --aux, and is ignored if the target chain didn't enable the TipDecorator
      --title string             The proposal title
      --type string              The proposal Type
  -y, --yes                      Skip tx broadcasting prompt confirmation
```

### SEE ALSO

* [empowerd tx gov](empowerd_tx_gov.md)	 - Governance transactions subcommands
* [empowerd tx gov submit-legacy-proposal cancel-software-upgrade](empowerd_tx_gov_submit-legacy-proposal_cancel-software-upgrade.md)	 - Cancel the current software upgrade proposal
* [empowerd tx gov submit-legacy-proposal ibc-upgrade](empowerd_tx_gov_submit-legacy-proposal_ibc-upgrade.md)	 - Submit an IBC upgrade proposal
* [empowerd tx gov submit-legacy-proposal param-change](empowerd_tx_gov_submit-legacy-proposal_param-change.md)	 - Submit a parameter change proposal
* [empowerd tx gov submit-legacy-proposal software-upgrade](empowerd_tx_gov_submit-legacy-proposal_software-upgrade.md)	 - Submit a software upgrade proposal
* [empowerd tx gov submit-legacy-proposal update-client](empowerd_tx_gov_submit-legacy-proposal_update-client.md)	 - Submit an update IBC client proposal
