pipeline {
    agent { label "node1"}
    stages {
        stage ('git pull') {
            steps {
                git branch: 'master', url: 'https://github.com/Sharmila-qt1/StudentCoursesRestAPI.git'

            }

        }
        stage ('docker image build') {
            steps {
                sh """docker image build -t students:1.0 .
                docker image tag students:1.0 sharmila1274/students:1.0
                docker image push sharmila1274/students:1.0"""
            }
        }
    }
}