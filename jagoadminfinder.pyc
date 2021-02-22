import requests
from termcolor import colored
from colorama import Fore
import colorama
from tqdm import tqdm
import argparse
import threading
import time
import datetime

colorama.init()

def logo():
    print(Fore.RED+"""
     _       _           _       _____ _           _           
    / \   __| |_ __ ___ (_)_ __ |  ___(_)_ __   __| | ___ _ __ 
   / _ \ / _` | '_ ` _ \| | '_ \| |_  | | '_ \ / _` |/ _ \ '__|
  / ___ \ (_| | | | | | | | | | |  _| | | | | | (_| |  __/ |   
 /_/   \_\__,_|_| |_| |_|_|_| |_|_|   |_|_| |_|\__,_|\___|_|   
                                                               

By Xnuvers007

command = jagoadminfinder.py -t <Site> using http://
""")    
wordlist = open("list.txt","r")
def findPanel(url):
    for words in wordlist:
        words = words.strip()
        req = requests.get(url+"/"+words)
        if req.status_code == 200:
            print(req.url)
parser = argparse.ArgumentParser("""
python3 AdminFinder -t [url]
ex:python3 AdminFinder -t http://google.com
""")
parser.add_argument("-t","--t")
args = parser.parse_args()
url = args.t
if url !=None:
    for _ in tqdm(range(100),
                  desc="Loading...",
                  ascii=False, ncols=75):
        time.sleep(0.3) #loading...
    for i in range(50):
        t = threading.Thread(target=findPanel,args=(url,))
        t.start()
else:
    logo()


logo()
