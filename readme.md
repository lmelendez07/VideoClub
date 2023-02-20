# Video Club

This is a software project for a video club that allows customers to rent and return videos, manage their accounts, and browse the available video catalog.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Before you can run the tests, you'll need to have the following software installed on your machine:
-   Node.js
-   PostgreSQL

You'll also need to have the video club software installed and running. Follow the instructions in the README.md file to install and start the software.

### Installing

To install the video club software, follow these steps:
1.  Clone the repository to your local machine.
2.  Install the necessary dependencies by running `npm install`.
3.  Set up the database by running the SQL scripts located in the `db` folder.
4.  Update the configuration file (`config.js`) with your database credentials.
5.  Start the server by running `npm start`.

## Running the tests

To run the tests, follow these steps:

1.  Open a terminal or command prompt and navigate to the project root directory.
2.  Run the following command to install the testing dependencies:

```css
npm install --dev
```

3. Create a test database by running the following commands in the `psql` command-line tool:
```bash
CREATE DATABASE video_club_test;
\c video_club_test
\i db/schema.sql
```

4.  Update the test configuration file (`config-test.js`) with your test database credentials. Open the file in a text editor and replace the placeholders with your database information.
```yaml
const config = {
  database: {
    host: 'localhost',
    port: 5432,
    user: 'your-username',
    password: 'your-password',
    database: 'video_club_test'
  }
};
```

5. Run the tests by running the following command:
```bash
npm test
```

6.  The test results will be displayed in the console. If all tests pass, you should see a message indicating that all tests have passed. If any tests fail, you'll see an error message that indicates which test(s) failed and why.

## Deployment
### Prerequisites.
Before you can deploy the video club software, you'll need to have the following:
-   A production server with Node.js and PostgreSQL installed.
-   A domain name or IP address pointing to the server.
-   A secure shell (SSH) client installed on your local machine.

### Deployment Steps.
1. Connect to the production server using SSH. You can use the following command to connect:
```java
ssh username@server-ip-address
```
Replace `username` with your username on the server and `server-ip-address` with the IP address of the server.

2.  Create a new directory to store the video club software:
```bash
mkdir video-club
```

3. Copy the project files to the new directory using the `scp` command. In your local machine terminal, navigate to the root directory of the project and run the following command:
```typescript
scp -r . username@server-ip-address:/path/to/video-club
```
Replace `username` with your username on the server, `server-ip-address` with the IP address of the server, and `/path/to/video-club` with the path to the `video-club` directory on the server that you created in step 2.

4. Connect to the server via SSH and navigate to the `video-club` directory:
```bash
cd /path/to/video-club
```

5. Install the project dependencies:
```css
npm install --production
```

6. Create a production database by running the following commands in the `psql` command-line tool:
```bash
CREATE DATABASE video_club_production;
\c video_club_production
\i db/schema.sql
```

7. Update the production configuration file (`config-production.js`) with your production database credentials. Open the file in a text editor and replace the placeholders with your database information.
```yaml
const config = {
  database: {
    host: 'localhost',
    port: 5432,
    user: 'your-username',
    password: 'your-password',
    database: 'video_club_production'
  }
};
```

8. Start the production server:
```sql
npm start
```

9. Visit the domain name or IP address of the server in a web browser to ensure that the software is running.

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

If you'd like to contribute to the video club software project, please follow these steps:
1.  Fork the repository and create a new branch for your feature or bug fix.
2.  Make your changes and write tests to ensure they work correctly.
3.  Push your changes to your fork and submit a pull request to the main repository.
4.  Wait for a code review and address any feedback before your changes are merged.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Luis Melendez** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* This proyect was made for the git subject on the programming class.