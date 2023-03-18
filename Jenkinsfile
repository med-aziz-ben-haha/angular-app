pipeline{
    agent any


	stages {


 stage('Getting project from Git') {
            steps{
      			checkout([$class: 'GitSCM', branches: [[name: '*/master']],
			extensions: [],
			userRemoteConfigs: [[url: 'https://github.com/med-aziz-ben-haha/test_app_angular.git']]])
            }
        }


        stage('Cleaning the project') {
            steps{
                sh "npm install"
            }
        }





        stage('Artifact Construction') {
            steps{
                sh "ng build  "
            }
        }

}


}
