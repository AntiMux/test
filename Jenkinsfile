properties([
        parameters([
                string(
                        name: 'devops_branch',
                        defaultValue: 'master',
                        description: 'Devops branch.'
                ),
                string(
                        name: 'infra_branch',
                        defaultValue: 'master',
                        description: 'Infra branch.'
                )
        ]),
])

def devops_branch = params.devops_branch

pipeline {

    agent any
    stages {
        stage("build") {
            steps {
                echo '${devops_branch}'
            }
        }
    }
}
