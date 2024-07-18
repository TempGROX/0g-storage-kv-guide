<div align=center>
  <img src="https://github.com/TempGROX/TempGROX/blob/main/src/photos/rounded-in-photoretrica.png" width="150">
  <h1>0g-storage-kv-guide</h1>
  <br>
</div>

# Hardware Requirement

|KEY|VALUE|
|:--|:----|
|RAM|16 GB|
|CPU|4 cores|
|Disk|500 GB|
|Bandwidth|500 MBps|

# Install

## Clone the source code
```bash
git clone -b v1.1.0-testnet https://github.com/0glabs/0g-storage-kv.git
```

## Build the source code

```bash
cd 0g-storage-kv
git submodule update --init

# Build in release mode
cargo build --release
```

## Config
Make the following settings in the file `config.toml`:

```toml
# rpc endpoint
rpc_listen_address
# ips of storage service, separated by ","
zgs_node_urls = "http://ip1:port1,http://ip2:port2,..."

# layer one blockchain rpc endpoint
blockchain_rpc_endpoint

# flow contract address
log_contract_address

# block number to start the sync, better to align with the config in storage service
log_sync_start_block_number

# storage nodes to download data from, separated by ","
# the provided nodes should cover full data in the storage network
zgs_node_urls
```

## Run
```bash
cd run

# consider using tmux in order to run in background
../target/release/zgs_kv --config config.toml
```

# The end!
If you liked this guide, please go to all my social networks)

<br>
<div id="badges" align="center">
  <a href="https://discord.com/users/961408999411048461">
    <img src="https://img.shields.io/badge/Discord-blue?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="https://medium.com/@James_Brandon">
    <img src="https://img.shields.io/badge/Medium-black?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="https://keybase.io/jamesbrandon">
    <img src="https://img.shields.io/badge/Keybase-orange?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
  <a href="https://x.com/JBTGrox">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
  <a href="https://linktr.ee/JBrandon_?utm_source=linktree_admin_share">
    <img src="https://img.shields.io/badge/Linktree-green?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
</div>
