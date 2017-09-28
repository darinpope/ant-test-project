node('docker') {
    docker.image('darinpope/ant:latest').inside {
        checkout scm
        sh '''
            export ANT_OPTS="-Xmx1024m -XX:MaxPermSize=512m"
            java -version
            ant -version
            mvn -version
            wget http://archive.apache.org/dist/ant/binaries/apache-ant-1.9.2-bin.tar.gz
            ant -Dsrc=src -Dbuild=build -Ddist=dist -DbuildDir=${WORKSPACE} clean dist
        '''
    }
}
