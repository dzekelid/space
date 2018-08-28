---
name: AWS WorkSpaces
x-slug: aws-workspaces
description: Amazon WorkSpaces is a fully managed, secure desktop computing service
  which runs on the AWS cloud. Amazon WorkSpaces allows you to easily provision cloud-based
  virtual desktops and provide your users access to the documents, applications, and
  resources they need from any supported device, including Windows and Mac computers,
  Chromebooks, iPads, Fire tablets, Android tablets, and Chrome and Firefox web browsers.
  With just a few clicks in the AWS Management Console, you can deploy high-quality
  cloud desktops for any number of users. With Amazon WorkSpaces, you pay either monthly
  or hourly just for the Amazon WorkSpaces you launch, which helps you save money
  when compared to traditional desktops and on-premises Virtual Desktop Infrastructure
  (VDI) solutions.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Space
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/apis.md
specificationVersion: "0.14"
apis:
- name: AWS WorkSpaces Service API - Create Tags
  x-api-slug: actioncreatetags-get
  description: Creates tags for a WorkSpace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actioncreatetags-get-openapi.md
- name: AWS WorkSpaces Service API - Create Workspaces
  x-api-slug: actioncreateworkspaces-get
  description: Creates one or more WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actioncreateworkspaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actioncreateworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Delete Tags
  x-api-slug: actiondeletetags-get
  description: Deletes tags from a WorkSpace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondeletetags-get-openapi.md
- name: AWS WorkSpaces Service API - Describe Tags
  x-api-slug: actiondescribetags-get
  description: Describes tags for a WorkSpace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondescribetags-get-openapi.md
- name: AWS WorkSpaces Service API - Describe Workspace Bundles
  x-api-slug: actiondescribeworkspacebundles-get
  description: Obtains information about the WorkSpace bundles that are available
    to your account in the specified region.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondescribeworkspacebundles-get-openapi.md
- name: AWS WorkSpaces Service API - Describe Workspace Directories
  x-api-slug: actiondescribeworkspacedirectories-get
  description: Retrieves information about the AWS Directory Service directories in
    the region that are registered with Amazon WorkSpaces and are available to your
    account.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondescribeworkspacedirectories-get-openapi.md
- name: AWS WorkSpaces Service API - Describe Workspaces
  x-api-slug: actiondescribeworkspaces-get
  description: Obtains information about the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondescribeworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Describe Workspaces Connection Status
  x-api-slug: actiondescribeworkspacesconnectionstatus-get
  description: Describes the connection status of a specified WorkSpace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actiondescribeworkspacesconnectionstatus-get-openapi.md
- name: AWS WorkSpaces Service API - Modify Workspace Properties
  x-api-slug: actionmodifyworkspaceproperties-get
  description: Modifies the WorkSpace properties, including the running mode and AutoStop
    time.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionmodifyworkspaceproperties-get-openapi.md
- name: AWS WorkSpaces Service API - Reboot Workspaces
  x-api-slug: actionrebootworkspaces-get
  description: Reboots the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionrebootworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Rebuild Workspaces
  x-api-slug: actionrebuildworkspaces-get
  description: Rebuilds the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionrebuildworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Start Workspaces
  x-api-slug: actionstartworkspaces-get
  description: Starts the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionstartworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Stop Workspaces
  x-api-slug: actionstopworkspaces-get
  description: Stops the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionstopworkspaces-get-openapi.md
- name: AWS WorkSpaces Service API - Terminate Workspaces
  x-api-slug: actionterminateworkspaces-get
  description: Terminates the specified WorkSpaces.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Enterprise-Applications_AmazonWorkSpaces.png
  humanURL: https://aws.amazon.com/workspaces/
  baseURL: :///
  tags: Amazon Web Services, Desktops, Stack Network, API Service Provider, API Service
    Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/aws-workspaces/actionterminateworkspaces-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.workdocs.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.workspaces.stack.network
- type: x-documentation
  url: http://docs.aws.amazon.com/workspaces/latest/api/api-reference.html
- type: x-faq
  url: https://aws.amazon.com/workspaces/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=164
- type: x-pricing
  url: https://aws.amazon.com/workspaces/pricing/
- type: x-testimonials
  url: https://aws.amazon.com/workspaces/testimonials/
- type: x-webinars
  url: https://aws.amazon.com/workspaces/resources/#webinars
- type: x-website
  url: https://aws.amazon.com/workspaces/
- type: x-white-papers
  url: https://aws.amazon.com/workspaces/resources/#whitepapers
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---