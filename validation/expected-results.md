# Expected Results

This file documents simple expected results for the load balancer review.

It uses sample values only.

---

## Load Balancer Review

Expected result:

```text
Load balancer exists and is active.
```

If not:

```text
Review provisioning state, compartment, subnet, and load balancer configuration.
```

---

## Load Balancer Health Review

Expected result:

```text
Load balancer health status does not show a critical issue.
```

If not:

```text
Review backend set health, listener configuration, backend health, and network rules.
```

---

## Listener Review

Expected result:

```text
Listener protocol and port match the application access requirement.
```

If not:

```text
Review listener protocol, listener port, and default backend set.
```

---

## Backend Set Review

Expected result:

```text
Backend set has the correct backend servers and health check policy.
```

If not:

```text
Review backend server list, load balancing policy, and health check settings.
```

---

## Backend Set Health Review

Expected result:

```text
Backend set health status is OK or healthy.
```

If not:

```text
Review individual backend health, health checker details, and network rules.
```

---

## Backend Health Review

Expected result:

```text
Backend health status is OK or healthy.
```

If not:

```text
Review backend application status, health check port, health check path, backend port, and network security rules.
```

---

## Network Rule Review

Expected result:

```text
Load balancer can reach the backend server on the required port.
```

If not:

```text
Review security lists, NSGs, route rules, and backend application listener.
```

---

## Final Review

The load balancer setup should be reviewed as a full path:

```text
User request -> Load Balancer -> Listener -> Backend Set -> Healthy Backend Server -> Application Response
```

If one part of the path is wrong, the application may not be reachable even when other parts look correct.
