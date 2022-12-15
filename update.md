1)  

> `cd ExordeModuleCLI`

 komutunu girin 

2)  

> `nano localConfig.json`

 komutunu girin

3)  yön tuşlarını kullanarak lastUpdate kısmına gidip 1.3.5 olarak değiştirin

4)  Ctrl+X basın sonra Y basın sonra Enter basın

5)  

> `docker build -t exorde-cli .`

 komutunu girin
 
6)  Aşağıdaki komutta ETHEREUMADRESİNİZ kısmını kendi adresiniz ile değiştirererek komutu girin 

7-a)  

    > docker run \
    > -d \
    > --restart unless-stopped \
    > --pull always \
    > --name exorde-cli \ exordelabs/exorde-cli \
    > -m ETHEREUMADRESİNİZ \
    > -l 2


7-b)Conflict hatası alanlar 

> `docker stop exorde-cli`

 ve 

> `docker rm exorde-cli`

 komutlarını girdikten sonra tekrardan 7-a) dan devam etsin

8)  

> `screen -r exorde`

 komutunu girin

9) 

> `docker ps`

 komutunu girin

10)  öğrendiğiniz container id’yi aşağıdaki komutta yerine yazıp komutu girin

11)  

> `docker logs --follow öğrendiğimizid`
