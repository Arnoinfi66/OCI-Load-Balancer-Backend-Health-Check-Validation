# Backend Set and Health Check

## Overview

A backend set connects traffic from the listener to backend servers.

The backend set also includes the health check policy used to monitor backend server availability.

---

## Backend Set Review

When reviewing a backend set, these items should be checked:

- Backend set name
- Load balancing policy
- Backend server list
- Backend server port
- Health check protocol
- Health check port
- Health check path if HTTP is used
- Health check interval
- Health check timeout
- Backend health status
- Backend set health status

---

## Health Check Protocol

A health check can be TCP or HTTP.

A TCP health check confirms whether the backend server accepts a TCP connection on the selected port.

An HTTP health check sends a request to a selected path and expects a valid response.

---

## Example HTTP Health Check

```text
Protocol: HTTP
Port: 80
Path: /health
Expected response: 200
```

This is only a sample. The real path should match the application health endpoint and should not be published if it exposes internal details.

---

## Example TCP Health Check

```text
Protocol: TCP
Port: 80
```

A TCP check can be useful when the review is focused on whether the backend port is reachable.

---

## Common Health Check Issues

A backend can show unhealthy when:

- The backend application is not running
- The health check port is wrong
- The health check path is wrong
- The backend security rules block traffic
- The application returns an unexpected response
- The backend server is not listening on the expected port
- The backend server is in the wrong subnet or network path

---

## What I Understood

My main understanding is that backend health should be checked carefully before trusting the load balancer setup.

If the health check does not match the actual backend application behavior, the backend may show unhealthy even when the server is running.
