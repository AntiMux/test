properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: '',
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
    }
}
