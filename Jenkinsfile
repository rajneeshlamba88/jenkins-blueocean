pipeline {
  agent any
  stages {
    stage('Widget') {
      parallel {
        stage('Widget') {
          steps {
            sh 'echo "Deploy Widget"'
          }
        }

        stage('sub-job') {
          steps {
            sh 'echo "this is sub"'
          }
        }

      }
    }

    stage('Widget Deploy') {
      steps {
        sh 'echo "this is for widget"'
      }
    }

  }
}