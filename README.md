# MERN 2.0 and CLOUD9
Starter boilerplate for MERN 2.0 combine with Cloud 9

## Steps to delploy in **ubuntu**

1. Prepare MERN with CLOUD9
```bash
mkdir [app_name]
cd [app_name]
clone https://github.com/Hashnote/mern-starter.git .
docker run -d -v $([app_name]):/workspace -p port_for_ide:8181 -p port_for_app:#### sapk/cloud9 --auth user:password
```

2. Setup requirement for MERN app
After running the above apps, browsering to ubuntu machine which the port_for_ide to login Cloud9 ide
At cloud9 ide termincal run the following command:

```bash
#install mongodb
apt-get update && apt-get install -y mongodb

#install heroku
#install nodejs modules
npm install
```

3. Modify server/config.js to make sure the app listing port is the same with the open port in docker (step 1)

4. Running mongodb database

```bash
mkdir data
mongod --dbpath data --nojournal

```

5. Runing service

```bash
npm start
#Check other options inside package.json file
```
