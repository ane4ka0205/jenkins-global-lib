@Library('CommonLib@master') _

node {https://github.com/ane4ka0205/jenkins-global-lib.git

  stage('poll the data') {
    git credentialsId: 'git_account', url: 'https://github.com/ane4ka0205/jenkins-library.git'
  }

  stage('hello world') {
    job.hello()
  }

  stage('check the result') {
    json.showUserInfo("${workspace}/data.json")
  }


}
