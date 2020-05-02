node{
  stage('git checkout'){
  git 'https://github.com/rksingh29/my-app'
  }
  stage('compile-package'){
    def mvnhome = tool name: 'maven3', type: 'maven'
    sh "${mvnhome}/bin/mvn package"
  }
  stage('Copy to other Server'){
    sshagent(['ssh-ec2']) {
      sh 'scp -o StrictHostKeyChecking=no target/*.jar ec2-user@172.31.44.173:/home/ec2-user/builds'
    }
  }
}
