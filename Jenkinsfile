node{
  stage('git checkout'){
  git 'https://github.com/rksingh29/my-app'
  }
  stage('compile-package'){
    def mvnhome = tool name: 'maven3', type: 'maven'
    sh "${mvnhome}/bin/mvn package"
  }
}
