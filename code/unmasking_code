import os
import re
import random
import fileinput
import sys
os.chdir('/opt/elk/logs/vp')
states = ['AL','AK','AZ','AR','CA','CO','CT','DE','FL','GA','HI','ID','IL','IN','IA','KS','KY','LA','ME','MD','MA','MI','MN','MS','MO','MT','NE','NV','NH','NJ','NM','NY','NC','ND','OH','OK','OR','PA','RI','SC','SD','TN','TX','UT','VT','VA','WA','WV','WI','WY','on:','AS','DC','FM','GU','MH','MP','PW','PR','VI']
alpha = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','X','Y','Z'] 
numbers = ['0','1','2','3','4','5','6','7','8','9']
def replaceAll(file):
    for line in fileinput.input(file, inplace=1):
        if '<tid>MASKED</tid>' in line:
            line = re.sub(r'<tid>MASKED</tid>','<tid>'+random.choice(alpha)+random.choice(alpha)+random.choice(alpha)+random.choice(alpha)+random.choice(states)+random.choice(alpha)+random.choice(alpha)+random.choice(alpha)+random.choice(alpha)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(numbers)+random.choice(alpha)+'</tid>',line)
        sys.stdout.write(line)
	
replaceAll('act_server-DL-unmasked1.log')