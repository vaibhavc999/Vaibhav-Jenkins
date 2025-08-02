// Jenkinsfile Groovy
pipeline {
  agent any
   tools {
        maven 'Maven' 
    }
  stages {
    stage('Test') {
      steps {
        sh "mvn test"
        echo 'Test'
      }
    }

    stage('Build') {
      steps {
        sh "mvn package"
        echo 'Buid'
      }
    }

    stage('Deploy Test') {
      steps {
        //deploy adapters: [tomcat10(url: "http://172.28.175.144:9090//", credentialsId: "tomcat")],
        //                   war: '**/*.war', contextPath: '/app' 
        echo 'Deploy Test'
      }
    }

    stage('Deploy Prod') {
      steps {
        echo 'Deploy Prod'
      }
    }

  }
  post{
    always {
        echo "here only"
    }
    success{
        echo "yess"
    }
    failure{
        echo "no"
    }
  }
}
