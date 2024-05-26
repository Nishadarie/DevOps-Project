pipeline {
  agent any
  environment {
    REPO_URL = 'https://github.com/your-repo.git'
  }
  stages {
    stage('Clone Repository') {
      steps {
        git url: "${REPO_URL}", branch: 'main'
      }
    }
    stage('Build Docker Images') {
      steps {
        script {
          docker.build('3d10180ad580b301df2ed6bc128aede0dd4088e9728a1db19ff15c6ccb548f04')
        }
      }
    }
    stage('Deploy Containers') {
      steps {
        script {
          docker.image('3d10180ad580b301df2ed6bc128aede0dd4088e9728a1db19ff15c6ccb548f04').run()
        }
      }
    }
  }
}
