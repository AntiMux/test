properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: 'test5',
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
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: 'refs/tags/${myTag}']],
                    extensions: [[$class: 'CloneOption', shallow: false, depth: 0, reference: '']],
                  ])
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
