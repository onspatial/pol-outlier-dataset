
# Step 1 (Run the simulation):

1. Fork the repository to your github ( there is a button in github to fork)
2. Clone the repository to your local machine and go to the `pol` directory. For me it was: `git clone git@github.com:haenter/pol.git` then `cd pol`

- - **NOTE:** the path to the `pol` folder should not contain `space` or maybe other special characters. (I got Exception that file does not exist on a Linux Machine)

3. Install maven local dependencies as indicated in `pom.xml` file

   - `mvn install:install-file -Dfile=src/main/resources/libs/jts-1.13.1.jar -DgroupId=com.vividsolutions -DartifactId=jts -Dversion=1.13.1 -Dpackaging=jar`

   - `mvn install:install-file -Dfile=src/main/resources/libs/geomason-1.5.2.jar -DgroupId=sim.util.geo -DartifactId=geomason -Dversion=1.5.2 -Dpackaging=jar`

   - `mvn install:install-file -Dfile=src/main/resources/libs/mason-19.jar -DgroupId=sim -DartifactId=mason -Dversion=19 -Dpackaging=jar`

   - `mvn install:install-file -Dfile=src/main/resources/libs/mason-tools-1.0.jar -DgroupId=at.granul -DartifactId=mason-tools -Dversion=1.0 -Dpackaging=jar`

4. Build the project using maven: `mvn clean install`
5. From github: `There are two ways to run a simulation: (1) GUI and (2) headless. For the GUI version, run the main method in src/main/java/edu/gmu/mason/vanilla/WorldModelUI.java. For the headless version, invoke the main method in src/main/java/edu/gmu/mason/vanilla/WorldModel.java with appropriate arguments. `
6. I use bash file to run the project loacated in examples e.g. `run.sh`
7. YOU HAVE DONE THE FIRST STEP! You should see the simulations in progress with the default configurations.

# Step 2 (Data Preparation)

I have used `scripts/data_wrangling/*` to create datasets.
