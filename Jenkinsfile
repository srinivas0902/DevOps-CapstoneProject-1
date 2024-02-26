pipeline{
    
    agent any
    
    stages{
        stage('Clone the repo')
        {
            steps{
                git branch: 'main', url: 'https://github.com/srinivas0902/DevOps-CapstoneProject-1.git'
            }
        }
        
        stage('Execute Playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'ansiblehost', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'playbookdocker.yml', vaultTmpPath: ''
            }
        }
        
    }
    
    
}
