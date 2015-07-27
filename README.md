
#USER NEEDS TO RUN THE FOLLOWING COMMANDS IN PYTHON ONCE THIS PROGRAM IS DONE RUNNING:
#FOR UPLOADS RUN THIS:

import requests

files = {'file': ('parking_violations_short.csv', open('parking_violations_short.csv', 'rb'), 'text/csv', {'Expires': '0'})}

r = requests.post('http://127.0.0.1:9000', files=files)

r.text    #for test of what was uploaded

#FOR DOWNLOADS RUN THIS:

import requests

r = requests.get('http://127.0.0.1:9000/correlations')

r.text
