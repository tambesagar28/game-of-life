node{
	stage('git')
	{
		// git clone
		git 'https://github.com/tambesagar28/game-of-life.git'
	}
	stage('build the code')
	{
		// Buliding the code using sh
		mvn 'package'
	}
}