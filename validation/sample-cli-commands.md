# Sample CLI Commands

These commands are sample review commands only.

Replace all placeholder values before using them in an OCI environment.

Do not publish real OCIDs, backend IPs, compartment names, public IPs, DNS names, or application URLs.

---

## List Load Balancers

```bash
oci lb load-balancer list \
  --compartment-id <compartment_ocid>
```

Purpose:

```text
Review available load balancers in the selected compartment.
```

---

## Get Load Balancer Details

```bash
oci lb load-balancer get \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review load balancer details and current status.
```

---

## Get Load Balancer Health

```bash
oci lb load-balancer-health get \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review the overall health status of the load balancer.
```

---

## List Listeners

```bash
oci lb listener list \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review listeners configured on the load balancer.
```

---

## List Backend Sets

```bash
oci lb backend-set list \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review backend sets connected to the load balancer.
```

---

## Get Backend Set Health

```bash
oci lb backend-set-health get \
  --backend-set-name <backend_set_name> \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review health status details for the backend set.
```

---

## Get Health Checker Details

```bash
oci lb health-checker get \
  --backend-set-name <backend_set_name> \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review the health check policy configured for the backend set.
```

---

## List Backend Servers

```bash
oci lb backend list \
  --backend-set-name <backend_set_name> \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review backend servers attached to the backend set.
```

---

## Get Backend Server Health

```bash
oci lb backend-health get \
  --backend-name <backend_private_ip>:<backend_port> \
  --backend-set-name <backend_set_name> \
  --load-balancer-id <load_balancer_ocid>
```

Purpose:

```text
Review the health status of a specific backend server.
```

---

## Simple Endpoint Check

```bash
curl -I http://<load_balancer_public_ip_or_dns_name>
```

Purpose:

```text
Check whether the load balancer endpoint responds.
```

Do not publish real public IPs, DNS names, or application URLs in GitHub.
