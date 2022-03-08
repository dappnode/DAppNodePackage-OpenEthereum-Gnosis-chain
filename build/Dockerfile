ARG UPSTREAM_VERSION

FROM openethereum/openethereum:${UPSTREAM_VERSION}
USER root
RUN ln -s /home/openethereum/openethereum /usr/local/bin/openethereum
USER openethereum

ENTRYPOINT [ "sh", "-c", "exec openethereum --chain xdai --jsonrpc-port 8545 --jsonrpc-interface all --jsonrpc-apis web3,eth,net,parity --jsonrpc-hosts all --jsonrpc-cors all --ws-interface all --ws-port 8546 --ws-apis=web3,eth,net,parity,pubsub --ws-origins=all --ws-hosts=all --ws-max-connections=10 --max-peers=100 --metrics --metrics-interface all ${EXTRA_OPTS}"]
