node('docker') {
    docker.image('darinpope/ant:latest').inside {
        checkout scm
        sh '''
            java -version
            ant -version
            mvn -version
            ant -Dsrc=src -Dbuild=build -Ddist=dist clean
        '''
    }
}
