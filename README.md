Example usage and output
========================

    $ peerinfo

    #    client            ver                       location             startingheight  synced_blocks
    -    ------            ---                       --------             --------------  -------------
    1    Satoshi           0.11.2                    United States        398962          -1
    2    Satoshi           0.9.99                    Germany              -1              -1
    3    Satoshi           0.11.0                    United States        375495          -1
    4    Satoshi           0.11.2                    Germany              365235          -1
    5    BitcoinUnlimited  0.12.0(EB16; AD4)         Sweden               400362          400526
    6    BitcoinUnlimited  0.12.0(EB16; AD4)         Germany              400396          400531
    7    Classic           0.11.2                    China                400396          -1
    8    BitcoinUnlimited  0.11.2                    Germany              400398          400531
    9    Satoshi           0.11.0                    United States        400398          400531
    10   Satoshi           0.9.99                    Germany              -1              -1
    11   Satoshi           0.11.1                    United States        400406          400531
    12   Satoshi           0.11.2                    France               400408          400531
    13   BitcoinUnlimited  0.11.2                    Norway               400422          400531
    14   BitcoinUnlimited  0.11.2                    Romania              400422          400531
    15   BitcoinUnlimited  0.11.2                    Sweden               400426          400531
    16   bitcoinj          0.12.2                    Germany              400429          -1
    17   Satoshi           0.11.2                    United States        400445          400531
    18   bitcoinj          0.13.3/MultiBitHD:0.2.0   Taiwan               400452          -1
    19   Satoshi           0.12.0                    Singapore            400453          400531
    20   Satoshi           0.12.0                    Germany              400502          400531
    21   Satoshi           0.11.1                    Russian Federation   400454          400519
    22   Satoshi           0.12.0                    Venezuela            183278          -1

    local block count:  400531
    tx in mempool:  486  Mb


    $ recentblocks 10

    height  size   # tx  time      date
    ------  ----   ----  ----      ----
    400531  0kb    1     09:13:59  2016-02-29
    400530  912kb  2107  09:12:04  2016-02-29
    400529  0kb    2     09:06:52  2016-02-29
    400528  976kb  2473  09:05:44  2016-02-29
    400527  956kb  2173  08:48:07  2016-02-29
    400526  976kb  2005  08:41:05  2016-02-29
    400525  976kb  2224  08:34:08  2016-02-29
    400524  956kb  3329  08:29:57  2016-02-29
    400523  976kb  2160  08:27:53  2016-02-29
    400522  958kb  1322  07:47:22  2016-02-29

    tx in mempool:  486  Mb
