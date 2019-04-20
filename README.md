# HTCondor Tarea 

## Autores:
    - Juan Felipe Orozco Escobar
    - Diana Marcela Garcia Correa

## Asignatura:
    - Plataformas Computacionales a Gran Escala
    - Universidad del Valle 2018B

## Información:
En este repositorio se expone la implementación de la tarea del ejemplo planteado en la diapositiva 41 de la siguiente presentación:

    https://docs.google.com/presentation/d/1_D_Q6aC9fJk1QEOeaOfEPR51IPQw-fd1VEmcZyL0mnE/edit#slide=id.p4
    
## Ejecución:
Ejecutar las siguientes líneas de código para hacer el levantamiento del container con HTCondor y acceder al bash del mismo:

    docker run -d --rm --mount type=bind,source=/ruta/descarga/archivos/HTCondorTarea,target=/home/submitter -w /home/submitter -h htcondor --name htcondor andypohl/htcondor
    docker exec -it -u 1000:1000 htcondor bash

Una vez dentro del container ejecutar:
    
    condor_submit testR.condor

Nota. recordar cambiar a ruta de descarga de los archivos del repositorio en el argumento source='...'
