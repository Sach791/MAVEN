pipeline{
  agent any
  tools{
    maven 'Maven'
    jdk 'JDK'
  }

  stages{
    stage('checkout'){
      steps{
        git branch:'master',https://github.com/Sach791/MAVEN.git
          }
    }

    stage('build'){
      steps{
        sh 'mvn clean package'
      }
    }
      stage('test'){
        steps{
          sh 'mvn test'
        }
      }
      stage('Run Application'){
        steps{
          sh 'java -jar target/MAVEN-1.0-SNAPSHOT.jar'
        }
      }

      post{
        success{
          echo'build and deployment successful'
        }
      failure{
        echo'Build failed'
      }
      }
    }
      
      
