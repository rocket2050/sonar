# Ansible Role: SonarQube


An Ansible Role that installs [SonarQube] on RedHat/CentOS and Debian/Ubuntu Linux servers.

## Requirements

Requirements:

  - SonarQube 5.0-5.5 requires Java 1.7+
  - SonarQube 5.6+ requires Java 1.8+
  - Mysql Version-5.6
## Role Variables

Available variables are listed below, along with default values:


Directory where downloaded files will be temporarily stored.

    sonar_download_url: http://dist.sonar.codehaus.org/sonarqube-5.6.zip
    sonar_version_directory: sonarqube-5.6

    sonar_mysql_username: sonar
    sonar_mysql_password: sonar
    
    sonar_mysql_host: localhost
    sonar_mysql_port: "3306"
    sonar_mysql_database: sonar
    
    sonar_mysql_allowed_hosts:
      - 127.0.0.1
      - ::1
      - localhost

JDBC settings for a connection to a MySQL database. Defaults presume the database resides on localhost and is only accessible on the SonarQube server itself.

## Dependencies

  - java
  - mysql

## Example Playbook

    - hosts: all
      roles:
        - sonar

SonarQube home at `http://localhost:9000/` (default System administrator credentials are `admin`/`admin`).
