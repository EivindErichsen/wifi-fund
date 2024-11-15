Successful connection to wifi
wifi connect -s “datarespons” -p “***” -k 1

warning and errors while connected:
[00:00:44.505,706] <err> net_pkt: Data buffer (1499) allocation failed.
[00:00:44.505,706] <wrn> net_conn: pkt cloning failed, pkt 0x2002f650 dropped

Devzone suggested fix - [increase CONFIG_SYSTEM_WORKQUEUE_STACK_SIZE](https://devzone.nordicsemi.com/f/nordic-q-a/97812/net_pkt-data-buffer-42-allocation-failed)

CONFIG_NET_PKT_RX_COUNT=32
CONFIG_NET_PKT_TX_COUNT=48
CONFIG_NET_BUF_RX_COUNT=32
CONFIG_NET_BUF_TX_COUNT=96
CONFIG_HEAP_MEM_POOL_SIZE=90000
CONFIG_NET_BUF_DATA_SIZE=256
CONFIG_NET_MGMT_EVENT_STACK_SIZE=2048
CONFIG_SYSTEM_WORKQUEUE_STACK_SIZE=4096

