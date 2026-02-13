JAR=btreelib.jar

# Path to your project folder
ASSIGN=/root/Documents/main/btree_project_spring_26-2

# Correct LIBPATH to point to the correct location
LIBPATH = $(ASSIGN)/lib/$(JAR)

# The CLASSPATH should include both the JAR file and the src directory
CLASSPATH = $(LIBPATH):$(ASSIGN)/src

# Java compile and run commands with classpath set
JAVAC = javac -classpath $(CLASSPATH)
JAVA  = java -classpath $(CLASSPATH)

# Target to compile the test files (BTTest.java, TestDriver.java, etc.)
tests: $(ASSIGN)/src/tests/BTTest.java $(ASSIGN)/src/tests/TestDriver.java
	$(JAVAC) $(ASSIGN)/src/tests/*.java

# Target to run the tests using the BTTest class
bttest: tests
	$(JAVA) tests.BTTest   # Runs the tests using the BTTest class

# Clean up the compiled class files in the tests directory
clean:
	rm -f $(ASSIGN)/src/tests/*.class *~ \#* core
