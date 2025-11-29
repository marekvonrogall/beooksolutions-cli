# BeookSolutions API

A simplified, dockerized version of [Beook Solutions](https://github.com/marekvonrogall/BeookSolutions).
## Installation

```bash
git clone https://github.com/marekvonrogall/beooksolutions-api.git
cd beooksolutions-api
docker build -t beooksolutions-api .
docker run -it -p 5000:5000 beooksolutions-api
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
