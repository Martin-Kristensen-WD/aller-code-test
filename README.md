# Code test - Aller Media 

## Setup

Installer dependencies:

```bash
# npm
npm install
```

## Start JSON server 
Jeg har simuleret at artiklerne kommer fra et endpoint, som det ville gøre i virkeligheden. Dertil bruger jeg JSON server til at lave et localhost endpoint. 

Kør dette script inden npm run dev 
```
json-server --watch data/db.json
```
Det laver dette endpoint: http://localhost:3000/posts 

## Development Server

Start dev server på http://localhost:5678/

```bash
npm run dev
```

