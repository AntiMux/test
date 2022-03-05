properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: 'tags/test5',
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
                        url: "https://github.com/AntiMux/test.git",
                        branch: "tags/${myTag}"
                )
            }
        }
        stage("print directory"){
            steps {
                sh 'ls .'
                sh 'git tag --points-at HEAD'
            }
        }
    }
}
