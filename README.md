# Apache Spark Setup Guide for Windows


## Prerequisites

Pls ensure you've these ready on your system before going further...
- Java Development Kit (JDK) installed (Java 8 or later)
- Scala installed (optional, for Scala programming)
- Python installed (optional, for PySpark)

## Steps

### 1: Download Apache Spark

1. Go to the [Apache Spark downloads page](https://spark.apache.org/downloads.html).
2. Select the latest Spark release(select 3.3.3 if available).
3. Choose a package type (preferably "Pre-built for Apache Hadoop")(select .Pre-built for Apache Hadoop2.7 if available)
4. Download the package in ZIP(tgz) format

### 2: Extract Spark

1. Extract the downloaded ZIP file to a directory of your choice[try to keep it in the root directory] (e.g., `C:\spark`).
2. Set up environment variables:
    - Right-click on "This PC" or "My Computer" and select "Properties."
    - Click on "Advanced system settings."
    - Click on "Environment Variables..."
    - Under "System variables," click "New" and add:
        - Variable name: `SPARK_HOME`
        - Variable value: `C:\spark`
    - Find the "Path" variable in the list, click "Edit," and add `%SPARK_HOME%\bin` to the list of paths.
     Set `JAVA_HOME`:
    - Add a line: `set JAVA_HOME=<path_to_java>` (e.g., `set JAVA_HOME=C:\Program Files\Java\jdk-15`)

### 3: Verify Installation

1. Open Command Prompt.
2. Run the Spark shell to verify the installation:
    - For Scala: `spark-shell`
    - For PySpark: `pyspark`
    => Spark context will be created for both cases, You can check the spark UI by clicking [here](localhost:4040)

If everything is set up correctly, the Spark shell should start without errors.


Happy Sparking!
