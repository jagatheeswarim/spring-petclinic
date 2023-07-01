pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=PetClinic \\
  -Dsonar.projectName=\'PetClinic\' \\
  -Dsonar.host.url=http://13.235.55.229:9000 \\
  -Dsonar.token=sqp_02e77a661033af78ef51b19a7efc792d20d54bdb'''
      }
    }

  }
}