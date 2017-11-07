#!/usr/bin/env groovy

/* Only keep the 10 most recent builds. */
properties([[$class: 'BuildDiscarderProperty',
             strategy: [$class: 'LogRotator', numToKeepStr: '10']]])


node {
    echo 'Hello World'
}