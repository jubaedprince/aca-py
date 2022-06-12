<!-- Command to provision aca-py -->

aca-py provision \
--wallet-type indy \
--endpoint http://18.219.146.82 \
--seed 100F40010300000c00000000010001A0 \
--wallet-name WalletTest6 \
--wallet-key MASTER_KEY_SECRET \
--genesis-url https://indy-test.bosch-digital.de/genesis \

<!-- Command to provision to run aca-py -->

aca-py start \
--inbound-transport http 0.0.0.0 8000 \
--endpoint http://18.219.146.82 \
--outbound-transport http \
--admin 0.0.0.0 8080 \
--genesis-url https://indy-test.bosch-digital.de/genesis \
--wallet-type indy \
--wallet-name WalletTest6 \
--wallet-key MASTER_KEY_SECRET \
--seed 100F40010300000c00000000010001A0 \
--admin-insecure-mode \
--label MY_SSI_AGENT \
--log-level debug \
--storage-type indy \
--auto-ping-connection \
--webhook-url http://18.219.146.82:3000
--max-message-size 10485760
