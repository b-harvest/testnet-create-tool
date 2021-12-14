# IBC testnet-create-tool
Once you've completed all of the steps below, run Hermes.

Hermes must be run with config.toml.
```shell
hermes -c hermes-config/config.toml start
```

## OS Preferences

It should be configured as below.

If you want to easily configure the os configuration, run the script as shown below.

* go 16.3
* jq
* make
* rust(cargo,rustup)

```shell
chmod +x os_env.sh
./os_env.sh
```

## Chains Preferences

The chain is designated as 10 and automatically sets Genesis files and config files when you run the script below.
Each chain uses the latest ibc-only software in Git Repo.
Also, the Hermes relayer is installed automatically.
(Takes some time 5m?)

Hermes
- v0.9.0

Chain list
- gaiad v6.0.0
- terrad v0.5.12
- bandd v2.3.2
- iris v1.2.1
- osmod v4.2.0
- regen v2.1.0
- akash v0.14.1
- sentinel v0.8.3 
- crypto.com chain-main_3.3.3_Linux_x86_64.tar.gz
- persistenceone v0.1.3

```shell
chmod +x local_env.sh
./local_env.sh
```

## IBC Preferences

All 10 chains have 45 mesh ibc connections in both directions with hermes 45 accounts.

If you run the script below, the IBC will automatically connect.
(Takes some time 5m?)

```shell
chmod +x create_channel.sh
./create_channel.sh
```

## Easy chain reset

```shell
chmod +x chain_reset.sh
./chain_reset.sh
```