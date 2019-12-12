pipeline {
  agent any
  stages {
    stage('package') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('deploy') {
      steps {
        sh 'cp /root/.jenkins/workspace/SistemaPromo_master/target/SistPromo.war /opt/wildfly/standalone/deployments'
      }
    }

  }
}