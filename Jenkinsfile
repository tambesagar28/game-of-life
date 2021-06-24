pipeline{
    agent any
    parameters{
        string(name:'PERSON', defaultValue:'Mr.Jenkins', description:'Hello Motherfucker')
        choice(name:'Branch',choices:['Master','Sprint-1','Sprint-3'], description:'Select the branch name')
    }
    stages{
        stage('git-1'){
            steps{
                git 'https://github.com/tambesagar28/game-of-life.git'
                echo "Hello${params.PERSON}"
                echo "Select ${params.Barnch}"
            }
           
        }
        stage('Build-1'){
            steps{
                sh 'mvn package'
            }
        }
        stage('artifact'){
            steps{
                archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
            }
        }
    }
}