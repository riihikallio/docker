# Web-palvelin harjoitusta 1.15 varten

Tämä perustuu nginx-kuvaan ja yhteen staattiseen sivuun.

## Asennus

```bash
docker build -t devops riihikallio/devops
```

## Käyttö

```bash
docker run -p 80:80 devops
```
Jos portti 80 on isäntäkoneella jo käytössä niin ensimmäisen '80' tilalle voi vaihtaa jonkin vapaan portin.

## Lisenssi
[MIT](https://choosealicense.com/licenses/mit/)