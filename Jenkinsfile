pipeline {
    agent any
    parameters{
        choice(name:'VERSION', choices:['1','2','3'], description:'Version to run')
    }

    stages {
        stage('Build') {
                when{
                        expression {params.VERSION == '1'}
                    }
                steps {
                        input('Do you want to proceed?')
                        echo 'This is the Build Step'
                    }
            }
        stage('Test') { 
                        when{
                                expression {params.VERSION == '2'}
                            }
               steps {
                        echo 'This is the TEST Step'
                    }
            }
        stage('Deploy') { 
                        when{
                                expression {params.VERSION == '3'}
                            }
                steps {
                         echo 'This is the DEPLOY Step'
                    }
            }
    }
    post{
        success{
            echo 'The job ran successfully'
        }
    }
}


