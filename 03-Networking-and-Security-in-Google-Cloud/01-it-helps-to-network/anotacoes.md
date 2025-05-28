Virtual Private Cloud
VPC is a secure, individual, private cloud-computing model hosted within a public cloud.


Public (external) IP address
  - Can be assigned from pool (ephemeral) or reserved (static).
  - Billed when not attached to a running VM.
  - VM doesn't know the external IP; It's mapped to the internal IP.

Private (internal) IP address
  - Allocated from subnet range to VMs by DHCP (Dynamic Host Configuration Protocol).
  - DHCP lease is renewed every 24 hours.
  - VM name and IP is registered with network-scoped DNS (Domain Name System).


LABS
  - Multiple VPC Networks
    - Create custom mode VPC networks with firewall rules
    - Use Compute Engine to create virtual machine instances
    - Explore the connectivity for virtual machine instances across VPC networks
    - Create a virtual machine instance with multiple network intefaces.

  - VPC Networks - Controlling Access
    - Create an NGINX web server
    - Create a tagged firewall rules
    - Create a service account with IAM roles
    - Explore permissions for the Network Admin and Security Admin roles

  - Application Load Balancer with Google Cloud Armor
    - Create HTTP and health check firewall rules
    - Configure two instance templates
    - Create two managed instance groups
    - Configure an Application Load Balancer with IPv4 and IPv6
    - Stress test an Application Load Balancer
    - Blocklist an IP address to restric access to an Application Load Balancer