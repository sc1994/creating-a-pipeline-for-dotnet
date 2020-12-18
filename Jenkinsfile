pipeline {
  agent {
    docker {
      image 'registry.cn-hangzhou.aliyuncs.com/newbe36524/sdk:5.0'
      args '-p 5656:80'
    }

  }
  stages {
    stage('Restore') {
      steps {
        sh 'dotnet restore'
      }
    }

    stage('Publish') {
      steps {
        sh 'dotnet publish -c Release -o publish'
        sh 'ls'
      }
    }
    
    stage('Deliver') {
      steps {
        sh '''cd publish
ls        
dotnet BlazorApp1.dll &'''
        input '点击确认按钮继续'
      }
    }
  }
}
