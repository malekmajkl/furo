## local Devel

### build furo locally

```sh
git clone {github_furo_repository}
cd ../furo
docker run -it -d --name node -v "$(pwd)"/furo:/furo node:10
docker exec -it node npm install
docker exec -it node npx gulp build
python3 -m build
```

### install build furo package

```sh
pip3 install dist/furo-{version}-py3-none-any.whl
```
