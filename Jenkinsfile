 node ('faux'){
  stage 'Build and Test'

simpleBuild {
 
    env = [
        FOO : 42,
        BAR : "YASS"
    ]
    
 

    before_script = "echo before"
    script = 'echo after $FOO'
    
    notifications = [
        email : "deasley@cloudbees.com"    
    ]
    
    
}

triggerRemoteJob mode: [$class: 'AwaitResult', timeout: [timeoutStr: '1d'], whenFailure: [$class: 'StopAsFailure'], whenTimeout: [$class: 'ContinueAsFailure'], whenUnstable: [$class: 'ContinueAsUnstable']], remotePathMissing: [$class: 'ContinueAsIs'], remotePathUrl: 'jenkins://d9579bb5698e59da9ff613a977724631/bfolder/goodjob'


}
