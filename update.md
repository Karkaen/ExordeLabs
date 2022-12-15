1)   komutunu girin 

`cd ExordeModuleCLI`

2)  komutunu girin

`nano localConfig.json `

3)  yön tuşlarını kullanarak lastUpdate kısmına gidip 1.3.5 olarak değiştirin

4)  Ctrl+X basın sonra Y basın sonra Enter basın

5)  komutunu girin

`docker build -t exorde-cli . `

6)  Aşağıdaki komutta ETHEREUMADRESİNİZ kısmını kendi adresiniz ile değiştirererek komutu girin 

`docker run \
-d \
--restart unless-stopped \
--pull always \
--name exorde-cli \
exordelabs/exorde-cli \
-m ETHEREUMADRESİNİZ \
-l 2`

Conflict hatası alanlar 

`docker stop exorde-cli `

ve 

`docker rm exorde-cli `

komutlarını girdikten sonra tekrardan dan devam etsin

8)  `screen -r exorde` komutunu girin

9) `docker ps` komutunu girin

10)  öğrendiğiniz container id’yi aşağıdaki komutta yerine yazıp komutu girin

11)  `docker logs --follow öğrendiğimizid`
