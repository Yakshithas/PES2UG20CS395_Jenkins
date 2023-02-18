pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ pes2ug20cs395_5b.cpp -o pes2ug20cs395_5b'
                echo 'build stage successful'
                build job: 'PES2UG20CS395-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './pes2ug20cs395_5b'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'pipeline failed'
        }
    }
}
