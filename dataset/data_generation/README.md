# Table of Contents

- [General info](#general-info)
- [Contents of the Data Generation](#contents-of-the-data-generation)
- [Requirements](#requirements)

# General Info

This is the source code used by feTruth for data generation, including move method refactoring mining, method invocation retrieval, training data generation, and testing data generation.

# Before use

1. Setup a MySQL 8 database, and run scripts in `resources/sql scripts/` to create tables.
2. Clone your target projects to the `repos/` directory.
3. Modify the `resources/config.properties`, connect your MySQL and set the `rootPath` to the 
**absolute path** of `data_generation/` directory like `/home/feTruth/dataset/data_generation/`. Please ensure the path ends with a `/`.
4. List your target projects in `projects.txt`, each project name should be on a new line. The project name should matchc the directory name in `repos/`.
5. Modify the `resources/log4j.properties` to change the log level if you want.

# Contents of the Data Generation

/src/main/java:

- /refactoringminer: The source code for move method refactoring mining.

- /methodinvocation: The source code for method invocation retrieval.

- /datageneration: The source code for training and testing data generation.

/src/main/resources:

- /sql scripts: The scripts for database table creation.
- config.properties: The file for configuring the MySQL database and the project's root path.
- testingApps.txt: Testing projects.

# Requirements

- Java 11.0.17 or newer
- Apache Maven 3.8.1 or newer
