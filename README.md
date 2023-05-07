
## Building Docker Image

Must set target platform if building from Apple Silicon version of Docker.

```sh
docker image build -t streamlit_test_amd64 --platform linux/amd64 .   
```

## Push to Azure

Assume already created a [Azure Container Registry][]

#### One Time Docker Login

```sh
docker login intbasiscontainers.azurecr.io
```

Paste username and password from Credentials page in Azure Portal

#### Push

```sh
docker tag streamlit_test_amd64 intbasiscontainers.azurecr.io/streamlit_test_amd64
docker push intbasiscontainers.azurecr.io/streamlit_test_amd64
```


  [Azure Container Registry]: https://azure.microsoft.com/en-us/products/container-registry
