**Student's Name:** Ayush Shridhar

**Mentor:** James Caffrey

**Project:** ADE- Add additional log support

**Project Description:** ADE supports only linux syslogs at the moment, the aim of this project is
to extend support to more complicated logs such as nginx/spark.

**Problem Definition:** ADE has pretty limited applicability at the moment. There are a lot of other applications
where ADE can be used, such as web servers and high performace computing. The aim of this project will enhance ADE to
support these applications, by handling additional logs (apart from just Linux syslogs).

**Deliverables** The final goal is to showcase the ability of ADE to work on much complicated logs structures.

**Additional Information** Since this project is based on the existing ADE project, the work will be done in a new branch
in the main [openmainframeproject/ade](https://github.com/openmainframeproject/ade) repository. 

**Coding Plan**

| Week | Tasks | Goals |
|------|-------|-------|
| _Week 1_ | Study ADE internals | Realize the best way to introduce Spark logs in the project |
| _Week 2_ | Understand ADE working, go through documentation | Get a high-level understanding of the structure of the project |
| _Week 3_ | Setup and install ADE locally | Get ADE running locally and play around with it |
| _Week 4_ | Create schema for handling spark logs | Develop and test database schema |
| _Week 5_ | Look at integrating this new schema into existing ADE (via cli/config file)| Set up new parameters/arguments to handle new logs|
| _Week 6_ | Generate the corresponding database | Get database ready to be used in later stages |
| _Week 7_ | Study the internal class struture | Get an idea of what needs to be added |
| _Week 8_ | Implement required classes and methods | Start working towards core implementation |
| _Week 9_ | Continue with the implementation | Finalize the classes and functions|
| _Week 10_ | Add tests for the above | Ensure everything is in place for the next part |
| _Week 11_ | Buffer week | Work towards resolving all bugs/issue that might have come up in earlier weeks |
| _Week 12_ | Look at training the ML model | Setup required parameters/arguments to setup the ML model|
| _Week 13_ | Work towards training the model on this new database | Get the machine learning model working |
| _Week 14_ | Analyse/verify the results | Ensure eveything is working as it is supposed to |
| _Week 15_ | Work on extensive tests and documentation | Document the new additions in the project |
| _Week 16_ | Buffer week | Work towards resolving all bugs/issue that might have come up in earlier weeks |

The aforementioned project plan gives a rough idea of what needs to be done from a high level design and implementation point of view. It is subject to changes as and when necessary.