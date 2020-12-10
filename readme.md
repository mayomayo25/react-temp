# install
```
docker-compose build
docker-compose run --rm react sh -c "npm install -g create-react-app && create-react-app app"
docker-compose run
```

# Tips
## hot reload
If the project runs inside a virtual machine such as (a Vagrant provisioned) VirtualBox, create an .env file in your project directory if it doesn’t exist, and add CHOKIDAR_USEPOLLING=true to it. This ensures that the next time you run npm start, the watcher uses the polling mode, as necessary inside a VM.
```
cd app
touch .env

CHOKIDAR_USEPOLLING=true
```