Airflow :


##  Orchestrer et  automatiser notre Data Pipeline.

Pour orchestrer et automatiser notre data pipeline, nous avons utilisés le DAGs (code_automation_airflow.py) :
- avant d'executer notre code , il faut lancer notre airflow webserver a l'aide dela commande : airflow webserver -p 8080 :
![Run Airflow Webserver](https://github.com/anasdaghai98/airflow/blob/main/airflow%20webserver.JPG)

apres que on a executé notre code et acceder a notre UI airflow , il nous a afficher un probleme de scheduler not run : 
![Error Scheduler](https://github.com/anasdaghai98/airflow/blob/main/before%20run%20scheduler.JPG)

pour regler ce probleme on a executer la commande airflow scheduler dans notre terminal : 
![Probleme resolu](https://github.com/anasdaghai98/airflow/blob/main/after%20run%20scheduler.JPG)

tout est bien maintenent , on peut executer notre dag sans probleme !
comme vous voyer ci dessous : Airflow UI , notre dag qui s'appelle anas est en mode on :

![Dags nommé (anas) is on ](https://github.com/anasdaghai98/airflow/blob/main/dags%20on.JPG)

en cliquent sur notre dag >> graph >> vous voyer ici notre tasks : 
![Process tasks ](https://github.com/anasdaghai98/airflow/blob/main/4tasks.JPG)

comme vous voyer dans l'image notre process commence par start puis il execute notre premier script , apres il execute notre deuxieme script, 
et a la fin le processus end qui indique que c'est le dernier process qui sera executer dans notre dag
et pour voir si notre code s'execute chaque 5 second , on cliquent sur schedule en haut de la page , il nous affiche cette liste d'execution , 
comme vous voyer ci dessous dans la date d'execution , chaque 5 sec il execute notre code :

![Scheduler executed succesfully](https://github.com/anasdaghai98/airflow/blob/main/each%205%20sec%20succesfully.JPG)

et si notre code est executer et que il y'a pas d'erreur , on vas verifier notre fichier log , 
comme vous voyer dans le fichier log , le code est executer par succes  et  effectue les traitements nécessaires !
![Notre fichier Log ](https://github.com/anasdaghai98/airflow/blob/main/log%20file.JPG)



