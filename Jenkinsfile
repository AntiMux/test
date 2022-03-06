properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: 'test10',
                        description: 'Tag to run'
                )
        ])
])

def myTag = params.tag

pipeline {

    agent any
    stages {
        stage("build") {
            steps {
                echo "${myTag}"
            }
        }
        stage("Checkout"){
            steps {
                cleanWs()
                git(
                    branch: 'master'
                )
                sh "git checkout tags/${myTag}"
        }
        stage("print directory"){
            steps {
                sh 'ls .'
                sh 'git tag --points-at HEAD'
            }
        }
    }
}
