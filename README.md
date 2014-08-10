<h1>Docker-Flask</h1>
Docker-Flask is a Docker setup for a very simple Flask application. It runs on Python 3.x via Nginx and UWSGI. To build this Docker file and get going follow the installation instructions below -- *installation instructions are written for Mac OS X users*

<h2>Step 1: Install Docker</h2>
Download Docker's [boot2docker](https://github.com/boot2docker/osx-installer/releases) to get started.

<h2>Step 2: Start boot2docker</h2>
Start *boot2docker* with the following command in your terminal:

```bash
$  boot2docker up
```
The command will return something that looks like the following statement. Copy and paste what *boot2docker* returned and execute it in your terminal:

```bash
$  export DOCKER_HOST=tcp://192.168.59.103:2375
```

<h2>Step 3: Download docker-flask</h2>
```bash
$  git clone https://github.com/ryanmcdermott/docker-flask.git
$  cd docker-flask
```

<h2>Step 4: Build docker-flask</h2>
```bash
$  docker build --rm --tag=flask .
```

<h2>Step 5: Run docker-flask</h2>
```bash
$  docker run -it -p 80:80 flask
```

You should see Docker running a supervisord session with Nginx and UWSGI. Now all that's left to do is open up your browser and type the IP address that boot2docker returned. In this example it was 192.168.59.103.

You should see the text *Flask is running!* in your browser. That's all there is to it!
