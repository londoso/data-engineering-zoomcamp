# Install terraform

```shell
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common unzip

wget https://releases.hashicorp.com/terraform/1.3.7/terraform_1.3.7_linux_amd64.zip

unzip terraform_1.3.7_linux_amd64.zip -d ~/bin/
```

# Autenticación

```shell
export GOOGLE_APPLICATION_CREDENTIALS="/home/anderson/google-sa.json"

gcloud auth activate-service-account --key-file $GOOGLE_APPLICATION_CREDENTIALS
```