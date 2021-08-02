FROM jenkins/jenkins:2.289.3-centos
MAINTAINER deB4SH <github@b4sh.de>

# Infrastructure as code plugin
RUN jenkins-plugin-cli --plugins configuration-as-code:1.51
# Credential Plugins
RUN jenkins-plugin-cli --plugins credentials:2.5 &&  \
    jenkins-plugin-cli --plugins ssh-credentials:1.19 &&  \
    jenkins-plugin-cli --plugins plain-credentials:1.7
# Jenkins general Plugins
RUN jenkins-plugin-cli --plugins matrix-project:1.19 && \
    jenkins-plugin-cli --plugins junit:1.51 && \
    jenkins-plugin-cli --plugins dashboard-view:2.17 && \
    jenkins-plugin-cli --plugins build-name-setter:2.2.0 && \
    jenkins-plugin-cli --plugins git-client:3.9.0 && \
    jenkins-plugin-cli --plugins matrix-auth:2.6.8 && \
    jenkins-plugin-cli --plugins cloudbees-folder:6.16 && \
    jenkins-plugin-cli --plugins config-file-provider:3.8.1 && \
    jenkins-plugin-cli --plugins embeddable-build-status:2.0.3 && \
    jenkins-plugin-cli --plugins ssh-agent:1.23 && \
    jenkins-plugin-cli --plugins cobertura:1.16
# WORKFLOW
RUN jenkins-plugin-cli --plugins workflow-aggregator:2.6 && \
    jenkins-plugin-cli --plugins workflow-multibranch:2.25 && \
    jenkins-plugin-cli --plugins workflow-api:2.46 && \
    jenkins-plugin-cli --plugins workflow-scm-step:2.13 && \
    jenkins-plugin-cli --plugins workflow-step-api:2.24 && \
    jenkins-plugin-cli --plugins workflow-basic-steps:2.23 && \
    jenkins-plugin-cli --plugins workflow-job:2.41 && \
    jenkins-plugin-cli --plugins workflow-durable-task-step:2.39 && \
    jenkins-plugin-cli --plugins docker-workflow:1.26 && \
    jenkins-plugin-cli --plugins workflow-step-api:2.24 && \
    jenkins-plugin-cli --plugins conditional-buildstep:1.4.1 && \
    jenkins-plugin-cli --plugins jenkins-multijob-plugin:1.36 && \
    jenkins-plugin-cli --plugins parameterized-trigger:2.41 && \
    jenkins-plugin-cli --plugins copyartifact:1.46.1
