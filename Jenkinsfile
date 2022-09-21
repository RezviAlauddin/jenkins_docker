pipeline {
  agent { label "linux" }
  stages {
    stage("build") {
      steps {
        sh """
        docker login --username rezvialauddin --password-stdin docker@mlops#rezvi#mlops@ 
        """
        sh """
          docker build -t hello_there .
        """
      }
    }
    stage("run") {
      steps {
        sh """
          docker run --rm hello_there
        """
      }
    }
  }
}