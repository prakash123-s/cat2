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
        sh 'mvn -f cat/pom.xml install -DskipTests'
      }
    }
    stage("Test"){
      steps{
        sh 'mvn -f cat/pom.xml test'
      }
    }
   
    stage("Deploy"){
      steps{
        sh 'cp "/var/lib/jenkins/workspace/cat/cat/target/cat.war" "/opt/apache-tomcat-9.0.89/webapps" '
      }
    }

    
  }
}
