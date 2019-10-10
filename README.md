# About Wappster

Wappster is a [Docker](https://www.docker.com/)-based tool to easily deploy and manage [self-hosted wapps](https://github.com/MichaelSchmidle/wapps) (short for “web apps”). It’s based on open source software like [Portainer](https://www.portainer.io/) and [Traefik](https://traefik.io/).

# Why Self-host?

There are two reasons for self-hosting:

* Cost: Paying substantially more for consuming the software as a service than self-hosting it.
* Privacy: Not entrusting the provider with sensible data.

# Requirements

Wappster requires [Docker](https://www.docker.com/) 17.06.0+ and [Docker Compose](https://docs.docker.com/compose/) 1.14.0+.

# First Usage

To run wappster, go through the following four simple steps.

## Step 1: Docker Network

Create the required Docker network ``wapps`` that all wapps will connect to when deployed, i.e.:

```
sudo docker network create wapps
```

## Step 2: Download

Download or clone this repository, i.e.:

```
git clone https://github.com/MichaelSchmidle/wappster
```

## Step 3: Pre-configuration

Copy the file ``default.env`` of the repository that you just downloaded/cloned to ``.env``. Then open the copied file in a text editor and define the required environment variables, i.e.:

```
cd wapps
cp default.env .env
nano .env
```

Further explanation of each environment variable can be found inside the copied ``.env`` file itself.

## Step 4: Launch

Finally, after saving the ``.env`` file, spin up your instance of wappster with ``docker-compose``, i.e.:

```
sudo docker-compose up -d
```
