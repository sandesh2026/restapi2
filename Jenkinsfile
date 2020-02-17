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
    stage('Code review'){
        withMaven(maven:'mymaven')
        {
            sh 'mvn pmd:pmd'
        }
        //
    }
    stage('AB Package'){
        withMaven(maven:'mymaven')
        {
        sh 'mvn package'
        }
    }
}
