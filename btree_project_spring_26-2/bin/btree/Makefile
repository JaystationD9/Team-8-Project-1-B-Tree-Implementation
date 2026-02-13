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

PROGS = together tests

# Default target to compile the program and tests
all: $(PROGS)

# Target to compile all Java files in the btree directory
together: $(ASSIGN)/src/btree/BTreeFile.java
	$(JAVAC) $(ASSIGN)/src/btree/BTreeFile.java

# Target to compile all Java files in the tests directory
tests: $(ASSIGN)/src/tests/BTTest.java $(ASSIGN)/src/tests/TestDriver.java
	$(JAVAC) $(ASSIGN)/src/tests/*.java

# Clean up the compiled class files in the btree and tests directories
clean:
	rm -f $(ASSIGN)/src/btree/*.class $(ASSIGN)/src/tests/*.class *~ \#* core

# Add a run target to execute the tests after compilation
run_tests: tests
	$(JAVA) tests.BTTest   # Runs the tests using the BTTest class
