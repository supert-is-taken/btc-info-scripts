Example usage and output
========================

Adding the switch '-w' will provide an html table to stdout instead.
Adding the switch '-r' will omit the formatting header.
You will need to add all the scripts to your path. In particular, all the commands need to have in their path the file script_functions.

### connected peers

    $ watch -n 120 peerinfo

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

### example: gauge support for bigger blocks

    $ recentblocks -n100 | grep '0x3\|8MB\|BIP' | nl

     1	402092  0kb    3     25           0.00000000  0x00000004  23:01:12  2016-03-10  BW fisher jinxin 8MB 
     2	402089  469kb  1035  25.25634121  0.00024767  0x00000004  22:54:01  2016-03-10  BW fisher jinxin 8MB 
     3	402088  760kb  1585  25.36129505  0.00022795  0x00000004  22:45:49  2016-03-10  BW fisher jinxin 8MB 
     4	402087  666kb  1406  25.28892542  0.00020549  0x00000004  22:34:06  2016-03-10  BW fisher jinxin 8MB 
     5	402086  647kb  990   25.2494546   0.00025197  0x00000004  22:22:16  2016-03-10  BitFury BIP100 
     6	402084  917kb  1809  25.3931681   0.00021734  0x00000004  22:03:52  2016-03-10  BitFury BIP100 
     7	402080  755kb  647   25.13813717  0.00021350  0x00000004  21:29:12  2016-03-10  BitFury BIP100 
     8	402058  973kb  760   25.18560129  0.00024421  0x00000004  18:10:56  2016-03-10  BW fisher jinxin 8MB 
     9	402052  912kb  1821  25.45101831  0.00024768  0x30000000  17:34:42  2016-03-10  KnCMiner 
    10	402050  974kb  2684  25.87142579  0.00032467  0x00000004  17:23:33  2016-03-10  BitFury BIP100 
    11	402048  974kb  668   25.13128263  0.00019653  0x00000004  16:28:28  2016-03-10  BitFury BIP100 
    12	402046  213kb  531   25.10301688  0.00019401  0x00000004  16:13:03  2016-03-10  BW fisher jinxin 8MB 
    13	402041  871kb  1191  25.24507342  0.00020577  0x00000004  15:44:24  2016-03-10  BW fisher jinxin 8MB 
    14	402040  974kb  2748  25.56512728  0.00020565  0x30000000  15:40:10  2016-03-10  slush 
    15	402039  974kb  787   25.14990979  0.00019048  0x00000004  15:21:23  2016-03-10  BitFury BIP100 
    16	402037  974kb  2209  25.50945801  0.00023063  0x00000004  15:09:52  2016-03-10  BitFury BIP100 
    17	402035  974kb  2879  25.57063911  0.00019821  0x00000004  14:47:35  2016-03-10  BitFury BIP100 
    18	402033  974kb  2808  25.69458953  0.00024736  0x00000004  14:19:12  2016-03-10  BW fisher jinxin 8MB 
    19	402030  974kb  2063  25.35922513  0.00017413  0x00000004  13:28:51  2016-03-10  BitFury BIP100 
    20	402024  974kb  1554  25.32312218  0.00020793  0x00000004  12:08:38  2016-03-10  BitFury BIP100 
    21	402019  974kb  1232  25.2988586   0.00024258  0x00000004  11:41:02  2016-03-10  BitFury BIP100 
    22	402016  974kb  1919  25.38563263  0.00020095  0x00000004  11:18:20  2016-03-10  BW fisher jinxin 8MB 
    23	402009  405kb  776   25.15654205  0.00020173  0x00000004  10:31:11  2016-03-10  BitFury BIP100 
    24	402001  974kb  2786  25.6316401   0.00022672  0x00000004  09:35:36  2016-03-10  BW fisher jinxin 8MB 
    25	402000  610kb  1196  25.24906519  0.00020825  0x00000004  09:08:01  2016-03-10  BitFury BIP100 
    26	401998  624kb  1096  25.21599857  0.00019708  0x00000004  08:51:07  2016-03-10  BW fisher jinxin 8MB 


## dependencies

Requires (debian packages) jq, geoip-bin and also bitcoin-cli with a running bitcoind.

