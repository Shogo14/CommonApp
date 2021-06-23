## イメージビルド
```bash
docker build -t front/latest .
```

```bash
docker run -it -p 3000:3000 -v $PWD:/front front/latest
```