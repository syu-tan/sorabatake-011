# sorabatake-011

## Examples

## Foundation Crop
![img](img/earth_class_predict.png)
## Cloud Prediction
![img](src/output/008/band_8.png)
![img](src/output/008/predict_aruw_nir.png)

## Dataset
- [SEN12MS-CR DATASET](https://patricktum.github.io/cloud_removal/sen12mscr/)
    ```shell
    wget "ftp://m1639953:m1639953@dataserv.ub.tum.de/s1_africa.tar.gz"

    # or
    rsync -chavzP --stats rsync://m1554803@dataserv.ub.tum.de/m1554803/ .
    ```
- [SEN12MS-CR-TS DATASET](https://patricktum.github.io/cloud_removal/sen12mscrts/)
    ```shell
    wget "ftp://m1554803:m1554803@dataserv.ub.tum.de/ROIs1158_spring_s1.tar.gz"

    # or
    rsync -chavzP --stats rsync://m1639953@dataserv.ub.tum.de/m1639953/ . 
    rsync -chavzP --stats rsync://m1659251@dataserv.ub.tum.de/m1659251/ .
    ```

- Cloud Dataset
    kaggle user 
    ```shell
    # Download
    kaggle datasets download -d hmendonca/cloud-cover-detection
    # Unzip
    unzip cloud-cover-detection.zip
    ```

    Link: https://www.kaggle.com/datasets/hmendonca/cloud-cover-detection


## Environment
### Need
- Dcoker
- Docker Compose
- Nvidia Driver
- Nvidia Docker 

### Procedure
```shell
docker compose -f compose_foundation.yml up -d
docker compose -f compose_cloud.yml up -d
```