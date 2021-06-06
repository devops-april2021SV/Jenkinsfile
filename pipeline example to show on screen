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
    }
    post{
        success{
            echo 'The job ran successfully'
        }
    }
}
