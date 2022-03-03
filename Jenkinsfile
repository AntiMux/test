
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

pipeline {

    agent any
    stages {
        stage("build") {
            steps {
                sh 'echo ${devops_branch}'
            }
        }
    }
}
