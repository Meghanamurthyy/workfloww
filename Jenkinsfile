pipeline
{
    agent any
    environment
    {
        dockerimage = "meghaa"
        registry = "meghanamurthyy/meghv"
        registryCredential = "docker_hub_cred"
    }
    stages
    {
        stage('Checkout')
        {
            steps
            {
                checkout scmGit(branches:[[name:'*/master']],extensions:[],userRemoteConfigs:[[url:'https://github.com/Meghanamurthyy/workfloww.git']])
            }
        }
        stage('Build docker image')
        {
            steps
            {
                script
                {
                    dockerimage = docker.build registry
                }
            }
        }
    }
}