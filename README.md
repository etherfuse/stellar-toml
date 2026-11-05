# stellar-toml (deprecated)

This repo is no longer used. Don't add files here.

Our `stellar.toml`, `stellar-testnet.toml` and `walletconnect.txt` now live in the
terraform repo, in
[`cloudflare/workers/stellar-toml/`](https://github.com/etherfuse/terraform/tree/master/cloudflare/workers/stellar-toml)
(ENG-2016). The `stellar-toml-proxy` Worker serves them on every `*etherfuse.com` host:
`/.well-known/stellar.toml` (hosts containing `sand` or `devnet` get
`stellar-testnet.toml`) and `/.well-known/walletconnect.txt`.

To change them, edit the file there and open a terraform PR. Merging deploys it.

This repo used to build the `stellar-toml` Cloudflare Pages project, which the Worker
read from. That project is no longer used, and the repo will be archived.
