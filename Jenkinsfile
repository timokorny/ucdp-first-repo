node {
	stage 'checkout'
   checkout([$class: 'GitSCM', 
			branches: [[name: '*/master']], 
			doGenerateSubmoduleConfigurations: false, 
			extensions: [], 
			submoduleCfg: [], 
			userRemoteConfigs: [[credentialsId: 'myCredentials', url: 'https://github.com/timokorny/ucdp-first-repo.git']]])
   echo 'checked out'
   
   stage 'Build'
		sh 'nuget restore src/WebApplication1.sln'
		sh "\"${tool 'MSBuild'}\" src/WebApplication1.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

		echo 'built done'
}
