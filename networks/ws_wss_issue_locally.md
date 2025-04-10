## SSL issue locally during WS/WSS connection via Postman

I had a difficulty during first testing via Postman: on staging I got success code, but locally it wound work whatsoever. Locally I had error `Error: write EPROTO 55061481703872:error:100000f7:SSL routines:OPENSSL_internal:WRONG_VERSION_NUMBER:../../../../src/third_party/boringssl/src/ssl/tls_record.cc:231:
`

it turns out, when you're normally using `wss://`, locally it has to be `ws://` because you don't have SSL certificates locally
