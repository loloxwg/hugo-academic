---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
#  - title: CEO
#    company: GenCoin
#    company_url: ''
#    company_logo: org-gc
#    location: California
#    date_start: '2021-01-01'
#    date_end: ''
#    description: |2-
#        Responsibilities include:
#        
#        * Analysing
#        * Modelling
#        * Deploying
#
  - title: Software Engineer Intern
    company: SenseTime
    company_url: 'https://www.sensetime.com/en'
    company_logo: st1
    location: Shanghai
    date_start: '2021-08-19'
    date_end: '2022-06-15'
    description: |2-
      Responsibilities include:
      * Design and develop backend services of the storage management system for the internal datasets using Golang, Gin, and Gorm. 
      * Responsible for packaging FSclient, writing tool modules, and processing data gateways.Configure Ceph OSS lifecycle permissions. 
      * Create various file management modules for the FS data gateway to ensure the stability and reliability of file operations. 
      * Package Docker images and deploy on servers. Use Kubectl to manage containers. Write unit test and regression tests. Design microservices that are scalable and secure.
  - title: Research Assistant
    company:  School of Automation
    company_url: ''
    company_logo: cqupt
    location: Chongqing
    date_start: '2020-10-19'
    date_end: '2022-06-01'
    description: |2-
      Responsibilities include:
      * Design an IoT MQTT message distribution and storage system based on micro-services for school research project. Used emqx rules engine for processing data into the Kafka message queue through kong gateway reverse proxy.
      * Implement micro-services to expose external APIs interface for different storage engines. 
      * Use RPC for internal communication and ensure structured data and unstructured data persistence.
      * Use Grafana for data visualization and monitoring.
  - title: Member of Organization
    company: Red Rock Programming Organization
    company_url: 'https://redrock.team/'
    company_logo: redrock
    location: Chongqing
    date_start: '2020-10-15'
    date_end: '2021-03-20'
    description: |2-
      Responsibilities include:
      * Participated in the testing and maintenance of the school website with a DAU of 5000+ users.
      * Develop back-end code according to the requirements of the product manager
    

design:
  columns: '2'
---
