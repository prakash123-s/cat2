pipeline{
  agents any
  tools{
    maven 'maven'
  }
  stages{
    stage("Git Checkout"){
      steps{
        git branch: 'main', url: 'https://github.com/prakash123-s/cat2'
      }
    }
  }
}
