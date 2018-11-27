pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        mail(subject: 'Jenkins Test Email', body: 'Hello World, my what a windy day you have today.', from: 'nathan@pc-doctor.com', to: 'nathan@pc-doctor.com', charset: 'UTF-8')
      }
    }
  }
}