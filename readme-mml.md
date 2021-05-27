## local Devel

### install dependencies

```sh
git clone {github_furo_repository}
cd ../furo
docker run -it -d --name node -v "$(pwd)"/furo:/furo node:10
docker exec -it node npm install
```

### build furo theme package

```sh
docker exec -it node npx gulp build
python3 -m build
```

### install furo package

```sh
pip3 install dist/furo-{version}-py3-none-any.whl
```
