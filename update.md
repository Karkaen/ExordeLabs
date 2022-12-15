#### 1)   komutunu girin 

```
cd ExordeModuleCL
```

#### 2)  komutunu girin

```
nano localConfig.json 
```

#### 3)  yön tuşlarını kullanarak lastUpdate kısmına gidip 1.3.5 olarak değiştirin

#### 4)  Ctrl+X basın sonra Y basın sonra Enter basın

#### 5)  komutunu girin

```
docker build -t exorde-cli .
```

#### 6)  Aşağıdaki komutta ETHEREUMADRESİNİZ kısmını kendi adresiniz ile değiştirererek komutu girin 

```
docker run \
-d \
--restart unless-stopped \
--pull always \
--name exorde-cli \
exordelabs/exorde-cli \
-m ETHEREUMADRESİNİZ \
-l 2
```

~~Conflict Hatası Alanlar ~~

```
docker stop exorde-cli 
```

ve 

```
docker rm exorde-cli 
```

komutlarını girdikten sonra tekrardan dan devam etsin

#### 8)  komutunu girin

```
screen -r exorde
```

#### 9) komutunu girin

```
docker ps
```

#### 10)  Logları görmek için
```
docker logs --follow öğrendiğimizid
```
