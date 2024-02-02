pipeline
{
    agent any
        stages
        {
            stage('continuous download')
            {
                steps
                {
                    git 'https://github.com/vivekkumargangam/newgit.git'
                }
            }
            stage('copying the file to root directory')
            {
                steps
                {
                    sh 'sudo -S cp -r  /var/lib/jenkins/workspace/multibranch_pipeline_master/ /root'
                }
            }
            stage('bulding the docker image')
            {
                steps
                {
                    sh 'sudo -S docker build -t jalm-2.3.5 -f Dockerfile /root/multibranch_pipeline_master/'
                }
            }
        }
}
