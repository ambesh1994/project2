pipeline {
agent{ label 'worker1'}
stages
{
    stage ("build") {
    steps {
    sh '''
    docker build -t httpd -f httpd.dockerfile .
    '''
    }
    }
    stage ("run") {
    steps {
    sh '''
    docker run -d -p 12345:80 --name httpd httpd
    '''
    }
    }
}
}
