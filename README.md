All in AMD crypto module based on [cryptojs](https://github.com/gwjjeff/cryptojs).

    crypto = require( 'crypto' )
    key = '12345678'
    us = 'Hello World'
    mode = new crypto.mode.ECB crypto.pad.pkcs7
    ub = crypto.charenc.UTF8.stringToBytes us
    eb = crypto.DES.encrypt ub, key, {asBytes: true, mode: mode}
    ehs= crypto.util.bytesToHex eb
    eb2= crypto.util.hexToBytes ehs
    ub2= crypto.DES.decrypt eb2, key, {asBytes: true, mode: mode}
    us2= crypto.charenc.UTF8.bytesToString ub2
    # should be same as the var 'us'
    console .log us2
