# Compound-V2-subgraph

### Concept

1. Subquery = the graph on polkadot
2. Acala has a subgraph on Subquery for us to grab the on-chain activities.
3. The subgraph here is forked from theGraph's official compound subgraph.
4. To make this subgraph to work for pike, we have to host a graph node ourselves, and deploy the subgraph to our hosted graph node

### Acala's technical support

Please contact Syed@Acala

### Future Recommendation

When starting this repo I followed Acala's EVM+ docs, https://evmdocs.acala.network/tutorials/subgraph, and tried to get the compound subgraph running.
Later I found out that, in order to get the subgraph running, We will need to deploy our own graph node, which is cumbersome.
I suggest in the future, instead of hosting our graph node and index the evm event logs through acala's EVM rpc, we can rewrite compound's subgraph on subquery, utilizing it's substract EVM support. See https://university.subquery.network/build/substrate-evm.html

### unfinished task

Pike's contracts has been deployed to mandala Pub Dev network, I tried starting a local graph node and deploy the subgraph to local to index mandala Pub Dev network, but it does not work.

Please contact Syed for help.

### start local graph-node

```
# follow https://evmdocs.acala.network/network/network-setup/local-development-network
# make sure the following is up:
# 1. local mandala node
# 2. eth-rpc-adapter
# 3. local acala's subquery node
# check with Syed@Acala if anything is not working
docker compose up
```

### create and deploy subgraph

```
# add back comptroller address to subgraph.yaml line 12
yarn
yarn create-local
yarn deploy-local
```
