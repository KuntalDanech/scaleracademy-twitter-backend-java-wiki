# Contributing to Twitter Backend

We love your input! We want to make contributing to this project as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features
- Becoming a maintainer


## Steps to contribute

* Comment on the issue you want to work on. Make sure it's not assigned to someone else.

### Making a Pull Request

> - Make sure you have been assigned the issue to which you are making a PR.
> - If you make PR before being assigned, It will be labelled [`invalid`](https://github.com/scaleracademy/twitter-backend-java/pulls?q=is%3Aopen+is%3Apr+label%3Ainvalid) and closed without merging.

* Fork the repo and clone it on your machine.
    ```bash
    git clone https://github.com/<your-github-id>/twitter-backend.git
    cd twitter-backend
    ```
* Add an upstream link to the main branch in your cloned repo
    ```bash
    git remote add upstream https://github.com/scaleracademy/twitter-backend.git
    ```
* Keep your cloned repo up to date by pulling from upstream (this will also avoid any merge conflicts while committing new changes)
    ```bash
    git pull upstream master
    ```
* Create your feature branch
    ```bash
    git checkout -b <feature-name>
    ```
* Commit all the changes
    ```bash
    git commit -am "Meaningful commit message"
    ```
* Push the changes for review
    ```bash
    git push origin <branch-name>
    ```
* Create a Pull Request from our repo on GitHub.

## Setting up the Development Environment using [Eclipse (Java EE)](https://www.eclipse.org/downloads/packages/release/2020-09/r/eclipse-ide-enterprise-java-developers) or [STS](https://spring.io/tools)

> - You can always use your favourite IDE like [IntelliJ IDEA](https://www.jetbrains.com/idea/) or [VS Code](https://code.visualstudio.com/)
> - Please check that the [JAVA_HOME](https://docs.oracle.com/cd/E19182-01/821-0917/inst_jdk_javahome_t/index.html) environment variable is set up using [JDK 11](https://adoptopenjdk.net/) to ensure optimal results.
- Import the project into your Workspace as an **Existing Maven Project.**
- Go to the file called [application-dev.properties](https://github.com/scaleracademy/twitter-backend/blob/master/src/main/resources/application-dev.properties) under [`src/main/resources`](https://github.com/scaleracademy/twitter-backend/blob/master/src/main/resources)
- Here you will find four environment variables namely
    - **`MYSQL_DB_HOST`** and **`MYSQL_DB_PORT`** at [Line 37](https://github.com/scaleracademy/twitter-backend/blob/fb2f7c56184ef4e56e599602905708e933bd30a1/src/main/resources/application-dev.properties#L37)
    - **`MYSQL_DB_UNAME`** and **`MYSQL_DB_PASSWD`** at [Line 40](https://github.com/scaleracademy/twitter-backend/blob/fb2f7c56184ef4e56e599602905708e933bd30a1/src/main/resources/application-dev.properties#L40) and [41](https://github.com/scaleracademy/twitter-backend/blob/fb2f7c56184ef4e56e599602905708e933bd30a1/src/main/resources/application-dev.properties#L41) respectively.
    - You can either set these environment variables under your Maven Build and SpringBoot run OR
    - You can also **remove** these and enter the following in place of the environment variables
        - `MYSQL_DB_HOST` will be your MySQL or MariaDB **host**. Like `localhost` or `127.0.0.1` or `0.0.0.0`
        - `MYSQL_DB_PORT` will be the **port** at which your database server resides. Like `3306`
        - `MYSQL_DB_UNAME` will be the **username** for your database. Like `root`
        - `MYSQL_DB_PASSWD` will be the **password** for accessing the database. Like `root123`
	- For exceptional cases If MySQL or MariaDB has a lower version then for MySQL we can set `mysql-connector-java` artifactId version as required and we can set JDBC driver (e.g `spring.datasource.driver-class-name`) as required in `application.properties`.
- After this right-click on the project and select Run As **Maven Build**
- Under **goals** write **`clean verify`** and Run the Build. _This produces an executable JAR under the `target` folder_
- After a Successful Build. Run the application by Right-Clicking on the project and clicking on Run as *Spring Boot App*
- You can access the application under **port 8080**
- If you want to change the port on which the application is running. Please make the changes in [application-dev.properties](https://github.com/scaleracademy/twitter-backend/blob/master/src/main/resources/application-dev.properties) at Line [73](https://github.com/scaleracademy/twitter-backend-java/blob/c4f41995e75b1a0f9d3ab1b2d0c41eb313c1b3b6/src/main/resources/application-dev.properties#L73) and uncomment the line and enter your desired port.
- If you are still facing any difficulties Please raise an [Issue](https://github.com/scaleracademy/twitter-backend-java/issues/new/choose) or reach out to [me](https://subho.xyz/site/en/contact.html).
- If you feel the documentation needs an update. Please send a Pull Request to update the same.


### Additional Notes

* Code should be properly commented to ensure its readability.
* If you've added code that should be tested, add tests with JUnit.
* Make sure your code is properly formatted.
* Issue that pull request!
* Your code should pass the automated CI pipeline Tests before making it into the codebase.
* Use Maven Wrapper for Java Code code `mvnw clean verify` for Windows and `./mvnw clean verify` for UNIX-based systems.

## Issue suggestions/Bug reporting

When you are creating an issue, make sure it's not already present. Furthermore, provide a proper description of the changes. If you are suggesting any code improvements, provide details about the improvements.

**Great Issue suggestions** tend to have:

- A quick summary of the changes.
- In case of any bug provide steps to reproduce
  - Be specific!
  - Give a sample code if you can.
  - What you expected would happen
  - What actually happens
  - Notes (possibly including why you think this might be happening, or stuff you tried that didn't work)


## License

By contributing, you agree that your contributions will be licensed under its  [AGPL-3.0 License](https://github.com/scaleracademy/twitter-backend/blob/master/LICENSE).