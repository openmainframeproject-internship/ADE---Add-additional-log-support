## Installing ADE

To install the Anomaly Detection Engine for Linux logs (ADE) requires the following steps

    Create a Linux system with the software defined in System Requirements .
    Create the ADE executable described in Creating an executable using maven
    Configure the ADE executable so it works in your environment described in Customizing ADE for your environment
    Validate that the ADE executable works in your environment

## System Requirements

ADE requires that the following software has been installed on the Linux system were your are building and validating the ADE executable

    Linux:
        Red Hat Enterprise Linux, SUSE, or Ubuntu

    JDBC compliant SQL database :
        JDBC compliant database such as Derby
        use the network server version of the database
        current delivery has been tested with Derby
            Apache Derby download
            Apache Derby quick start
            Apache Derby installation
            Apache Derby network server
        current delivery has been tested with MariaDB 10.1.12
            MariaDB Enterprise
            MariaDB Download

        Java developer kit:
            JDK 1.7 or higher

        Apache Maven software management tool:
            Apache Maven download
            Apache Maven installation instructions

ADE requires that the following software has been installed on the Linux system were your are using the ADE executable

    Linux:
        Red Hat Enterprise Linux, SUSE, or Ubuntu

    JDBC compliant SQL database :
        JDBC compliant database such as Derby
        use the network server version of the database
        current delivery has been tested with Derby
            Apache Derby download
            Apache Derby quick start
            Apache Derby installation
            Apache Derby network server
        current delivery has been tested with MariaDB 10.1.12
            MariaDB Enterprise
            MariaDB Download
## Creating an executable using maven

    To create the executable maven must be installed. ADE uses maven to download all of the open source packages which ADE requires. List of Open Source Packages used by ADE

    Download the current master branch from GitHub. ADE on GitHub

    Run the following maven command from the ADE root directory build created when you downloaded ADE from GitHub.

        mvn clean package

        The maven command requires access to the internet.
        The build process will print a lot of output to the screen but if it completes successfully there will be a BUILD SUCCESS message.
        The packaged build output will be a .tgz file in the /ADE-assembly/target directory that contains everything needed to run ADE.

        Copy ADE-assembly/target/ADE-assembly–bin.tgz to a linux directory and expand using tar -zxvf.

## Customizing ADE for your environment

    Examine the default configuration for ADE provide provided in conf/setup.props and make the appropriate changes to the default configuration in order for ADE to run in your environment.

    The setup.props file is a properties file that contains a number of properties used by ADE during runtime. For more details see Configuration - setup.props

    By default setup.props comes populated with values for connecting to a Derby database named db1.

    # Database properties 
    ade.databaseUrl=jdbc:derby://localhost:1527/databases/db1
    ade.databaseDriver=org.apache.derby.jdbc.ClientDriver
    ade.databaseUser=dbuser
    ade.databasePassword=passw0rd

    If you use a different database you must update appropriately. If you are working on a shared system it may be useful to change the database name to something unique to you so you can work your own database.

    Customize bin/env.sh

    Update DB_CLIENT_PATH variable point to the path to the appropriate JDBC client jar.
    Configure output options

    The default configuration provided by ADE includes the xslt files in the output to support displaying the xml using a web browser. If the output of ADE does not need to be viewed using a web browser, then including the xslt files can be turned off by changing the value of the property key createXSLDirectory to false in the flowlayout.xml.

    The commands needed to invoke ADE functions can be found in ./bin .

## Validate executable

    To validate that ADE is working in your environment you can take advantage of the scripts and baseline provided. The analysis_comp_test.sh script in .bin/test will invoke ADE commands to validate that the executable is generating the expected results.
        The test script creates a test database
        It primes the database with baseline logs
        It creates a model using the baseline logs loaded into the database
        It analyzes additional base line logs and creates the xml files
        It compares the resulting xml files to the expected xml files downloaded from GitHub 
    analysis_comp_test.sh uses a DERBY database created especially for this test.

        analysis_comp_test.sh

