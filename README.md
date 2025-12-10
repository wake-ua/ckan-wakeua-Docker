# *TDATA/ckan-DEPLOY*

> Deploy TDATA with docker on production

---

## Objectives

- Develop a distribution for TDATA CKAN portal

---

## Funding Information

This research project is supported by:

**Funding organization/institution:**  Conselleria de Educación, Universidades y Empleo de la Generalitat Valenciana
**Program or grant:** Subvenciones a grupos de investigación consolidados
**Project code/reference:** CIAICO/2022/019
**Duration:** [01/01/2023 – 31/12/2025]  

---

## Technology
- Python
- Docker
- CKAN
---

## Installation and Usage

### Install 
- Docker: https://docs.docker.com/get-docker/

### Configure
Inside *prod* folder we can configure environment variables and other services options.

### Run
Download and build the corresponding images
```
git clone https://github.com/docpad/dockerfile.git

cd prod

docker-compose up -d
```

### Create user
Create an user to start uploading data.
```docker exec -it ckan /usr/local/bin/ckan -c /etc/ckan/production.ini sysadmin add newuser```
Log in the web and generate an 
### Services

| Service    | Port | Description                                                   |
|------------|------|---------------------------------------------------------------|
| CKAN       | 5000 | CKAN with standard extensions                                 |
| solr       |      | A pre-built SolR image set up for CKAN.                       |
| postgres   |      | CKAN’s database, later also running CKAN’s datastore database |
| redis      |      | A pre-built Redis image                                       |
| datapusher | 8800 | A pre-built CKAN Datapusher image                             |


---

## Authors / Contributors
- Alberto Berenguer Pastor – [@aberenguerpas](https://github.com/aberenguerpas)  

---

## License

This project is distributed under the [MIT License](LICENSE)


---

## 💬 Contact

For questions, collaborations, or further information:

📧 [wake@dlsi.ua.es](mailto:wake@dlsi.ua.es)  
🌐 [Wake Research group](https://wake.dlsi.ua.es/)
