# Console Review Checklist

This checklist is used to review the OCI Load Balancer backend health check flow from the OCI Console.

## Load Balancer Review

- Confirm the load balancer exists
- Confirm whether it is public or private
- Confirm the load balancer subnet
- Confirm the current load balancer health status
- Confirm the load balancer is in the expected compartment

## Listener Review

- Confirm listener protocol
- Confirm listener port
- Confirm default backend set
- Confirm the listener matches the application access need

## Backend Set Review

- Confirm backend set name
- Confirm load balancing policy
- Confirm health check protocol
- Confirm health check port
- Confirm health check path if HTTP is used
- Confirm backend server list
- Confirm backend set health status

## Backend Server Review

- Confirm backend private IP and port
- Confirm backend server is reachable from the load balancer path
- Confirm application is running on the expected port
- Confirm backend health status

## Network Rule Review

- Confirm backend security rules allow required traffic
- Confirm health check port is not blocked
- Confirm NSG and security list rules are aligned, if used
- Confirm no public documentation contains real IPs, OCIDs, DNS names, or URLs

## What I Understood

The main point of this checklist is to review the load balancer as a full flow.

A listener, backend set, backend server, health check, and network rule all need to work together.
