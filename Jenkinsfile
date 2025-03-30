pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git credentialsId: 'pyTorch', url: 'https://github.com/juliousmulumba23/jenkins_ansible_series.git'
            }
        }
        stage('Execute Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, extras: '-e hosts=all', installation: 'Ansible', inventory: 'hosts', playbook: 'test_reboot.yml', vaultTmpPath: ''
            }
        }
    }
}
