<center><img src="https://raw.githubusercontent.com/colav/colav.github.io/master/img/Logo.png"/></center>

# KayPacha
SQL data extraction for Scienti and Colav parners  Oracle databases

# Description
Package extract the data from SQL databases from Oracle Databases from Scienti or Colav parners
Models are defined here, filters etc..

# Installation

## Package
`pip install kaypacha`


# Usage
Oracle DB Colav docker database for scienti have to be already loaded, [take a look here](https://github.com/colav/oracle-docker)

Remember you only can use max 2 threads due a Oracle XE version limitation [more information here](https://docs.oracle.com/en/database/oracle/oracle-database/18/xeinl/licensing-restrictions.html)

Saving the model product for scienti on MongoDB (default users are UDEA_CV,UDEA_GR,UDEA_IN)

`
kaypacha_scienti --model_year 2022 --model product  --max_threads 2 --checkpoint
`

Saving all models for scienti on MongoDB

`
kaypacha_scienti --model_year 2022 --max_threads 2 --checkpoint
`

Getting a JSon file sample for the model product for scienti (**WARNING**: getting the full DB in a file require a huge amount of RAM, use it with careful.)
`
kaypacha_scienti --model_year 2022 --model product --json prod.json --max_threads 2 --sample
`

### Example university of externado

`
kaypacha_scienti --model_year 2022 --model product --max_threads 2 --cvlac_user UEXT_CV --gruplac_user UEXT_GR --institulac_user UEXT_IN --checkpoint
`

## Entities models supported fo Scienti
* product (EN_PRODCUTO)
* netowrk (EN_RED)
* project (EN_PROYECTO)
* event (EN_EVENTO)

# TODO
* implement all the main tables for Scienti.
  * event "EN_EVENT"
  * resgiter "EN_REGISTRO"
  * industrial_secret "EN_SECRETO_INDUSTRIAL"
  * recognition "EN_RECONOCIMIENTO"
  * event "EN_EVENTO"
  * patent "EN_PATENTE"
  * art_product "EN_PROD_ARTISTICA_DETALLE"

# License
BSD-3-Clause License 

# Links
http://colav.udea.edu.co/



