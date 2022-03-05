properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: '',
                        description: 'Tag to run'
                )
        ])
])

def tag = params.tag

pipeline {

    agent any
    stages {
        stage("build") {
            steps {
                echo "${tag}"
            }
        }
    }
}
