pipeline {
  agent {
    docker {
      image 'registry.cn-hangzhou.aliyuncs.com/newbe36524/aspnet:5.0-buster-slim'
      args '-p 5000:80'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'dotnet restore'
      }
    }

  }
}