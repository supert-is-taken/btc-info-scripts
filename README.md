Example usage and output
========================

Adding the switch '-w' will provide an html table to stdout instead.

### connected peers

    $ watch -n 10 peerinfo

    #    client                ver       startingheight  synced_blocks   location          address
    -    ------                ---       --------        --------------  -------------     -------
    1    Satoshi               0.9.99    -1              -1              Germany           xxxxxx
    2    Satoshi               0.9.99    -1              -1              Germany           xxxxxx
    3    bitcoinj              0.12.2    -1              401677          Germany           xxxxxx
    4    BitcoinUnlimited      0.        402052          401677          United States     xxxxxx
    5    Satoshi               0.11.2    -1              400824          United States     xxxxxx
    6    BitcoinUnlimited      0.        402052          401677          United States     xxxxxx
    7    BitcoinUnlimited      0.        402052          401677          Germany           xxxxxx
    [....]

    local block count:  400531
    tx in mempool:  486  Mb


### recent blocks

    $ watch -n 120 recentblocks -n 5

    height  size   #_tx  coinbase     fees/tx     version    time      date        coinbase_str
    ------  ----   ----  --------     -------     -------    ----      ----        ------------
    402052  912kb  1821  25.45101831  0.00024768  x30000000  17:34:42  2016-03-10  KnCMiner 
    402051  974kb  2955  25.41630761  0.00014088  x00000004  17:25:20  2016-03-10
    402050  974kb  2684  25.87142579  0.00032467  x00000004  17:23:33  2016-03-10  BitFury BIP100 
    402049  226kb  481   25.08214367  0.00017078  x00000004  16:30:53  2016-03-10  AntPool 
    402048  974kb  668   25.13128263  0.00019653  x00000004  16:28:28  2016-03-10  BitFury BIP100 

    tx in mempool:  486  Mb

### fees

    $ watch -n 120 feestate

    1 BTC = 418.13 USD
    Fees in mempool: 1.1451 BTC, 478.80 USD
    Relay fee: 0.00002000 BTC, 0.008 USD
    Average fees in last block: 0.00024768 BTC,  0.104 USD
    estimated fee for inclusion in...
        1 blocks: -1 BTC, -418.13 USD
        2 blocks: 0.00047544 BTC, 0.20 USD
        3 blocks: 0.00038877 BTC, 0.16 USD
        4 blocks: 0.00029707 BTC, 0.12 USD
        5 blocks: 0.00029707 BTC, 0.12 USD
        6 blocks: 0.00029707 BTC, 0.12 USD
        7 blocks: 0.00024333 BTC, 0.10 USD
        8 blocks: 0.00024333 BTC, 0.10 USD
    tx in mempool:  6794 , usage: 112  Mb, size: 51  Mb


## dependencies

Requires (debian packages) jq, geoip-bin and also bitcoin-cli with a running bitcoind.

