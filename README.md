
#User needs to run the following commands in python once the program is done running:
#for uploads run this:

import requests

files = {'file': ('parking_violations_short.csv', open('parking_violations_short.csv', 'rb'), 'text/csv', {'Expires': '0'})}

r = requests.post('http://127.0.0.1:9000', files=files)

r.text    #for test of what was uploaded

#for downloads tun this:

import requests

r = requests.get('http://127.0.0.1:9000/correlations')

r.text
