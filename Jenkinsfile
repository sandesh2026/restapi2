#!/usr/bin/env groovy
import java.net.URL

node{
    stage('Git Checkout'){
        git 'https://github.com/sandesh2026/DevOpsClassCodes.git'
    }
    stage('AB compile'){
        withMaven(maven:'mymaven')
        {
        sh 'mvn compile'
        }
    }
    stage('AB Package'){
        withMaven(maven:'mymaven')
        {
        sh 'mvn package'
        }
    }
}
