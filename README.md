# Sui-Devnet-Guncelleme

Sunucumuza bağlanıyoruz ve sırasıyla şu komutları giriyoruz;
1
```
cd sui && rm -rf genesis.blob
```
2
```
wget -qO genesis.blob https://github.com/MystenLabs/sui-genesis/raw/main/devnet/genesis.blob
```
3
```
sed -i 's/stable/main/' docker-compose.yaml
```
4
```
sed -i 's/127.0.0.1/0.0.0.0/' fullnode-template.yaml
```
5
```
docker-compose down --volumes
```
6
```
docker-compose up -d
```
Son olarak Log kontrol ediyoruz;
```
docker logs -f sui-fullnode-1 --tail 50
```

Ve işlemler bu kadar arkadaşlar..

Hepinize kolay gelsin.
