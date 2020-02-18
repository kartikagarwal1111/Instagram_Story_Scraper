# Instagram_Story_Scraper
Scrapes the seen list of story we post on insta and stores it in database.
Instagram doesnot provide seen list of users 24 hours after one posts a story.
Using this script,we can store the seen list of each story in a database.

Format of storage-------

For each follower who sees the story ,1 is marked in the column of the story and 0 instead.
After posting next story,the story id changes and a new column is added to the database.

Use-------

To detect inactive accounts by using sql queries over the table after storing data for ample amount of time and finding the users with least number of views.Multiple users can use this to find inactive users in their mutuaal connections(if in case some has muted the story of one user)

Requirements--------

python3

ChromeDriver----

ChromeDriver 79.0.3945.79

location--->   /home/[userr]/Documents/chromedriver

google-chrome should have the following location----

/home/[username]/.config/google-chrome

Packages to be present ----->

import os,time, getpass

from selenium import webdriver

from selenium.webdriver.common.by import By

from selenium.webdriver.common.keys import Keys

from signal import signal, SIGINT

import requests

import json

import sqlite3