# Sui-Devnet-Guncelleme

Sunucumuza bağlanıyoruz ve sırasıyla şu komutları giriyoruz;

```
cd sui && rm -rf genesis.blob
```

```
wget -qO genesis.blob https://github.com/MystenLabs/sui-genesis/raw/main/devnet/genesis.blob
```

```
sed -i 's/stable/main/' docker-compose.yaml
```

```
sed -i 's/127.0.0.1/0.0.0.0/' fullnode-template.yaml
```

```
docker-compose down --volumes
```

```
docker-compose up -d
```
Son olarak Log kontrol ediyoruz;
```
docker logs -f sui-fullnode-1 --tail 50
```

Ve işlemler bu kadar arkadaşlar..

Hepinize kolay gelsin.
