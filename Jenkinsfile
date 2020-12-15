pipeline {
  agent {
    docker {
      image 'registry.cn-hangzhou.aliyuncs.com/newbe36524/sdk:5.0'
      args '-p 5000:80'
    }

  }
  stages {
    stage('Restore') {
      steps {
        sh 'dotnet restore'
      }
    }

    stage('Run') {
      steps {
        sh 'dotnet run --project BlazorApp1'
      }
    }

  }
}