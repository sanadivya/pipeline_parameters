pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script {
                    properties ([
                        parameters ([
                            choice(
                                choices: ["ONE", "TWO"],
                                name: 'PARAMETER_01'
                            ),
                            booleanParam(
                                defaultValue: 'true',
                                description: 'Run this job',
                                name: 'BOOLEAN'
                            ),
                            text(
                                defaultValue: '''
                                This is multi-line
                                string parameter example
                                ''',
                                name: 'MULTI_LINE_STRING'
                            ),
                            string(
                                defaultValue: 'scriptcrunch',
                                name: 'STRING_PARAMETER',
                                trim: true
                            )
                        ])
                    ])
                }
            }
        }
    }
}