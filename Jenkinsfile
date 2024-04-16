pipeline {
  agent any
  tools{
    maven 'Maven 3.6.3'
  }
  stages{
      stage("build"){
          steps{
              echo 'step 1: compiling the code......'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'step 2: running unit test......'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'step 3: generating artifacts-packages......'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
