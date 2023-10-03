# Ensure the following are installed:

Java JDK = java -version

sudo apt install openjdk-11-jdk

Maven = maven --version

sudo apt install maven

# To build your java application to a .jar file use:
mvn clean package -DskipTests=true
# NOTE target directory will be created after build. To view the .jar file check teh path Java-SHOPPING CART-App/target

# Write the Dockerfile

# Build the docker image using:
docker build -t shopping -f docker/Dockerfile .

# Run the container using:
docker run --rm -i -p 8070:8070 --name shopping-cart shopping

# Visit http://localhost:8070/ to view the web app.
