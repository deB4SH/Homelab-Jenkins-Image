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
    jenkins-plugin-cli --plugins git-client:3.9.0 && \
    jenkins-plugin-cli --plugins matrix-auth:2.6.8 && \
    jenkins-plugin-cli --plugins cloudbees-folder:6.16
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
    jenkins-plugin-cli --plugins workflow-step-api:2.24
