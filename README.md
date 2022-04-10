# Docker Uygulaması


## Imageyi lokalde çalıştırma
+ proje dosyasını [indiriyoruz](https://github.com/Rabiaakbulut/docker-uygulama)

+ indirdiğimiz dosyada terminali çalıştırıyoruz (dockerfile'nin olduğu dizin)

+ container imageyi build edelim
```
docker build -t rabia_docker .
```

+ imageyi run ederek containerı çalıştıralım
makinemizin 3001 portundan containerın 3000 portuna bağlanalım
```
docker run -dp 3001:3000 rabia_docker
```

+ tarayıcıda http://localhost:3001/ adresine gidelim

![lokalhost resmi](/lokalhost.png)
***

## Imageyi Docker Hub'a Yükleme

+ projeyi Docker Hub'a yüklemek için repository(rabia_docker) oluşturalım

+ Docker Hub'a giriş yapalım
```
docker login -u rabiaakbulut
```

+ docker tag ile imaja yeni isim verelim
```
docker tag rabia_docker rabiaakbulut/rabia_docker
```

+ imageyi Docker Hub'a push edelim
```
docker push rabiaakbulut/rabia_docker
```
