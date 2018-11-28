node{

	
		
	stage('Build')
	{
			docker.image('python:2-alpine').inside{
				// def customimage = docker.build("my-image:{$env.BUILD_ID}") 
				//customimage.push(), .inside{  } // save the image or run steps inside of it
				//def dockerfile = 'Dockerfile.test'
		        //def customImage = docker.build("my-image:${env.BUILD_ID}", "-f ${dockerfile} ./dockerfiles")
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