@Library('CommonLib@master') _
def job = new com.myscript()

def json = new com.myscript()

node {

  stage('poll the data') {
    git credentialsId: 'git_account', url: 'https://github.com/fsadykov/jenkins-library-test.git'
  }

  stage('hello world') {
    job.hello()
  }

  stage('check the result') {
    json.showUserInfo("${workspace}/data.json")
  }


}
