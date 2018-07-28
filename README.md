## 啟動
> `geth --datadir data --networkid 123456 --rpc --rpccorsdomain "*" --nodiscover --rpcapi="db,eth,net,web3,personal" console`

## 查詢帳號
> eth.accounts[0]
"0x066f8944dba86f30e2dc3546d31133fb2a709f4a"
> 123456

> eth.accounts[1]
"0xe5412d5747076c00cf5322429d23c183e601a1d9"
> 456789

## 查詢餘額
> web3.fromWei(eth.getBalance(eth.accounts[0], "ether"))
"0"
> web3.fromWei(eth.getBalance(eth.accounts[1], "ether"))
"0"

## 匯款
> eth.sendTransaction({from:eth.accounts[0], to:eth.accounts[1],value:web3.toWei(3,"ether")})

```
INFO [07-28|15:31:56.820] Submitted transaction                    fullhash=0x0bbc249fe43bb0c29abb0e8c505ed44479eb0e49d50d64b890a7b0b7e2af5938 recipient=0xe5412d5747076C00Cf5322429D23C183e601a1d9
"0x0bbc249fe43bb0c29abb0e8c505ed44479eb0e49d50d64b890a7b0b7e2af5938"
```