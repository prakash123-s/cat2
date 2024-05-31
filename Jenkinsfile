pipeline{
  agent any
  tools{
    maven 'maven'
  }
  stages{
    stage("Git Checkout"){
      steps{
        git branch: 'main', url: 'https://github.com/prakash123-s/cat2'
      }
    }
    stage("Build"){
      steps{
        sh 'mvn -f cat/pom.xml -DskipTests'
      }
    }
    stage("Test"){
      steps{
        sh 'mvn -f cat/pom.xml test'
      }
    }

    
  }
}
