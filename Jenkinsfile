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

        stage('jobs') {
          steps {
            sh 'echo "uter"'
          }
        }

        stage('git-checkout') {
          steps {
            ws(dir: '/tmp/temp') {
              git(url: 'https://github.com/rajneeshlamba88/jenkins-blueocean.git', branch: 'main', changelog: true, poll: true)
            }

            sh 'echo "${WORKSPACE}"'
          }
        }

      }
    }

    stage('Widget Deploy') {
      parallel {
        stage('Widget Deploy') {
          steps {
            sh 'echo "this is for widget"'
          }
        }

        stage('sub-job-sub') {
          steps {
            sh 'echo "test"'
          }
        }

      }
    }

  }
}