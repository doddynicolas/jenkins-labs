node{
  stage ('git'){
    url:' https:doddynicolas/jenkins-labs
  }
  stage ('build jenkins image'){
    sh " docker build -t doddy-devops/jenkins:1.0 ."
  }
  stage ('push the jenkins image'){
    withCredentials([string (credentialsId:'jenkins-pwd', variable: 'dockerHubPwd')]){
      sh "docker login -u doddy-devops -p ${dockerHubPwd}
    }
    sh "docker push doddy-devops:1.0
}
