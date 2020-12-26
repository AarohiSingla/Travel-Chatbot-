# Travel-Chatbot-

1- train nlu by running       

python nlu_training.py

2- train core by 

python -m rasa_core.train -d domain.yml -s data/stories.md -o models/dialogue -c policy.yml


3- Run Bot server by ( 1st cmd)
python -m rasa_core.run --enable_api -d models/dialogue -u models/nlu/default/current --cors "*" -o out.log --endpoints endpoints.yml --port 5500 --credentials credentials.yml


4- Run web app by  (2nd cmd)
python web_app.py

5-Run below command on( 3rd cmd)
python -m rasa_core_sdk.endpoint --actions action
