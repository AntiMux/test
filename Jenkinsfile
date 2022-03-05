properties([
        parameters([
                string(
                        name: 'tag',
                        defaultValue: '',
                        description: 'Tag to run'
                )
        ])
])

def devops_branch = params.devops_branch

pipeline {

    agent any
    stages {
        stage("build") {
            steps {
                echo '${tag}'
            }
        }
    }
}
