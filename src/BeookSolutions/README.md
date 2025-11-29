# BeookSolutions CLI

This repository is a **mirror** of the `src/BeookSolutions` folder from the monorepo:

https://github.com/marekvonrogall/tools/tree/main/src/BeookSolutions

It exists to let users clone and use this project easily without downloading the entire monorepo.

---

## Installation

```bash
git clone https://github.com/marekvonrogall/beooksolutions-cli.git
cd beooksolutions-cli
docker build -t beooksolutions-cli .
docker run -it -p 5000:5000 beooksolutions-cli
```

## Usage

### API Endpoints

#### 1. Ping

Check if the service is running:

- Request

`GET http://localhost:5000/Solution/ping`

- Response

`200 OK`

Body:
`"works! (Beook Solutions)"`

#### 2. Enable

Enable solutions in the uploaded SQLite database file.

- Request
  
`POST http://localhost:5000/Solution/enable`

Form data:
`file` - the SQLite database file to modify (multipart/form-data)

- Response

Returns the modified SQLite file as a downloadable binary.

#### 3. Disable

Disable solutions in the uploaded SQLite database file.

- Request
  
`POST http://localhost:5000/Solution/disable`

Form data:
`file` - the SQLite database file to modify (multipart/form-data)

- Response

Returns the modified SQLite file as a downloadable binary.
