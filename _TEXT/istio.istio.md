istio an open platform to connect manage and secure microservices introduction repositories issue management in addition here are some other documents you may wish to read istio community describes how to get involved and contribute to the istio project istio developers guide explains how to set up and use an istio development environment project conventions describes the conventions we use within the code base creating fast and lean code performance oriented advice and guidelines for the code base youll find many other useful documents on our wiki introduction istio is an open platform for providing a uniform way to integrate microservices manage traffic flow across microservices enforce policies and aggregate telemetry data istios control plane provides an abstraction layer over the underlying cluster management platform such as kubernetes mesos etc visit istio io for in depth information about using istio istio is composed of these components envoy sidecar proxies per microservice to handle ingress egress traffic between services in the cluster and from a service to external services the proxies form a secure microservice mesh providing a rich set of functions like discovery rich layer 7 routing circuit breakers policy enforcement and telemetry recording reporting functions note the service mesh is not an overlay network it simplifies and enhances how microservices in an application talk to each other over the network provided by the underlying platform mixer central component that is leveraged by the proxies and microservices to enforce policies such as authorization rate limits quotas authentication request tracing and telemetry collection pilot a component responsible for configuring the proxies at runtime citadel a centralized component responsible for certificate issuance and rotation node agent a per node component responsible for certificate issuance and rotation broker a component implementing the open service broker api for istio based services under development istio currently supports kubernetes consul and eureka based environments we plan support for additional platforms such as cloud foundry and mesos in the near future repositories the istio project is divided across a few github repositories istio istio this is the main repository that you are currently looking at it hosts istios core components and also the sample programs and the various documents that govern the istio open source project it includes security this directory contains security related code including citadel acting as certificate authority node agent etc pilot this directory contains platform specific code to populate the abstract service model dynamically reconfigure the proxies when the application topology changes as well as translate routing rules into proxy specific configuration istioctl this directory contains code for the istioctl command line utility mixer this directory contains code to enforce various policies for traffic passing through the proxies and collect telemetry data from proxies and services there are plugins for interfacing with various cloud platforms policy management services and monitoring services broker this directory contains code for istios implementation of the open service broker api istio api this repository defines component level apis and common configuration formats for the istio platform istio mixerclient client libraries currently supports c for mixers api istio proxy the istio proxy contains extensions to the envoy proxy in the form of envoy filters that allow the proxy to delegate policy enforcement decisions to mixer issue management we use github combined with zenhub to track all of our bugs and feature requests each issue we track has a variety of metadata epic an epic represents a feature area for istio as a whole epics are fairly broad in scope and are basically product level things each issue is ultimately part of an epic milestone each issue is assigned a milestone this is 0 1 0 2 or nebulous future the milestone indicates when we think the issue should get addressed priority pipeline each issue has a priority which is represented by the pipeline field within github priority can be one of p0 p1 p2 or p2 the priority indicates how important it is to address the issue within the milestone p0 says that the milestone cannot be considered achieved if the issue isnt resolved we dont annotate issues with releases milestones are used instead we dont use github projects at all that support is disabled for our organization