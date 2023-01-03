Airflow :


##  Orchestrer et  automatiser notre Data Pipeline.

Pour orchestrer et automatiser notre data pipeline, nous avons utilisés le DAGs (code_automation_airflow.py) :
- avant d'executer notre code , il faut lancer notre airflow webserver a l'aide dela commande : airflow webserver -p 8080 :
![Run Airflow Webserver](https://github.com/anasdaghai98/airflow/blob/main/airflow%20webserver.JPG)
---------image run airflow web server------------
apres que on a executé notre code et acceder a notre UI airflow , il nous a afficher un probleme de scheduler not run : 
![Alt Text](url)
------------scheduler not run----------------
pour regler ce probleme on a executer la commande airflow scheduler dans notre terminal : 
![Alt Text](url)
-------------commande scheduler run-----------------------------
![Alt Text](url)
--------------after run scheduler-------------------------------
tout est bien maintenent , on peut executer notre dag sans probleme !
comme vous voyer ci dessous : Airflow UI , notre dag qui s'appelle anas est en mode on :
![Alt Text](url)
-------image dags on-----
en cliquent sur notre dag >> graph >> vous voyer ici notre tasks : 
![Alt Text](url)
-------tasks proccess------------
et pour voir si notre code s'execute chaque 5 second , on cliquent sur schedule en haut de la page , il nous affiche cette liste d'execution , 
comme vous voyer ci dessous dans la date d'execution , chaque 5 sec il execute notre code :
![Alt Text](url)
--------scheduler execute task successfuly---------
et pour si notre code est executer et que il y'a pas d'erreur , on vas verifier notre fichier log , 
comme vous voyer dans le fichier log , le code est executer par succes  et  effectue les traitements nécessaires
![Alt Text](url)
---------log image-----------------


