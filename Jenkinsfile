pipeline {
  agent {
    label 'master' 
  }

  stages {
    // stage('Semgrep') {
    //   steps {
    //     sh '''echo \'Running semgrep...\'
    //     /usr/local/bin/docker run --rm -v "${PWD}:/src" returntocorp/semgrep --config=https://semgrep.dev/p/r2c-CI'''
    //   }
    // }

    stage('Docker node test') {
      agent {
        docker {
          label 'master'
          image 'node:7-alpine'
          args '--name docker-node'
        }
      }
      steps {
        sh 'node --version'
      }
    }

  }
}