node{
	stage('Build')
	{
		docker.image('python:2-alpine')
		steps
		{
			echo "Im working HERE"
			checkout([$class: 'GitSCM', \
				branches: [[name: '*/jenkinsBranch']], \
				doGenerateSubmoduleConfigurations: false, \
				extensions: [], \
				submoduleCfg: [], \
				userRemoteConfigs: \
				[[credentialsId: 'github', \
				url: 'https://github.com/nathanPCD/creating-a-pipeline-in-blue-ocean/']]])
		

				sh 'python -m py_compile sources/add2vals.py sources/calc.py' 

				echo "done!!"
		}
	}
}