
## Setup
`docker-compose up -d localstack` command against the `docker-compose.yml` 

Create a `.env` file at the root of the project and add in your own values for these enviornment variables.

  - `AWS_ENDPOINT='http://localhost:8000/'`
  - `AWS_REGION='localhost'`
  - `AWS_ACCESS_KEY_ID='fake-access-key'`
  - `AWS_SECRET_ACCESS_KEY='fake-secret-key'`


## Running
DynamoDB Local
  - Open a terminal at the the folder where you extracted the jar file
    - Run: `java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb`default port: `8000`.
    - Open a browser at: `http://localhost:8000/shell`

LocalStack Docker container
  - Run `docker-compose up -d localstack`
  - `docker-compose start`.

Lambda Functions

  - Run `npm run seed` to seed some test data.
  - Run `npm start` to start the functions locally.

Eendpoint.

  - `curl -i localhost:3000/contacts`
