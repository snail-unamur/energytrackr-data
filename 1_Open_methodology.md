# Research methodology

## How the data was collected and analysed

A small set of relevant repositories were chosen from the JavaAwesome repository including specific criteria.

Those criteria include :

- Repository must be _OpenSource_
- The project must be at least partly coded in Java and tested in Java
- The project must be a _Maven project_ and must include a _pom.xml file_
- The line coverage of the project must be greater or equal to 60%
- The amount of lines of java code must be greater or equal to 20000
- Repository must _be maintained up_ to the date of the data collection
- Number of commits must be greater or equal to 500
- Tests duration must not exceed 40 seconds to avoid running for too long

## Steps

### About the project analyse

To find relevant repositories developed in Java, we select projects from AwesomeJava : https://github.com/akullpp/awesome-java

We first check whether (at least) a pom file exists at the root of the repo.
Then we execute the command `mvn clean test` or `mvn clean verify`. For some repositories, running the tests and assessing the coverage requires to modify the pom to execute it. Finally we just check if the amount of lines of java code is greater or equal to 20000.

### On energyTracker

Getting used to the tool requires some adaptation depending on the environment.

Once it is done, we write config files for each selected repository (see README.md file in energytrackr repo root for format).

We use the energytrackr statistic tool to assess energy consumption of selected repositories using this config. We get energy_measurements files identified by the date of execution. We then sort the resulting file using provided command lines by energytrackr and we plot it.
