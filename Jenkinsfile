pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('two') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('three') {
      steps {
        echo 'this is the package job'
        sh 'run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}