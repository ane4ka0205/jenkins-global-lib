@Library('CommonLib@master') _
def job = new com.lib.helloworld()

def json = new com.lib.jsonviewer()

node {

  stage('poll the data') {
    git credentialsId: 'git_account', url: 'https://github.com/ane4ka0205/jenkins-library-test.git'
  }

  stage('hello world') {
    job.hello()
  }

  stage('check the result') {
    json.showUserInfo("${workspace}/data.json")
  }


}
