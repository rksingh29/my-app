node{
  stage('git checkout'){
  git 'https://github.com/rksingh29/my-app'
  }
  stage('compile-package'){
  mvn 'clean package'
  }
}
