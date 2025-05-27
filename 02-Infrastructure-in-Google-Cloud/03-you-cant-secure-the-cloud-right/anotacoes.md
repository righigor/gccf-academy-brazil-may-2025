Infrascture security design
  Operational security
  Internet communication
  Storage services
  Service deployment
  Hardware infrastructure


Customer-managed encryption keys (CMEK)
  Manage keys in a cloud-hosted solution
  Encrypt and decrypt via API
  Automated and at-will key rotation
  Symmetric and asymmetric key support

Customer-supplied encryption keys (CSEK)
  Gives users more control over their keys, but with greater management complexity
  Users use their own AES-256-bit encryption keys and are responsible for generating them
  Users are responsible for storing the keys and providing them as aprt of Google Cloud API calls
  Google cloud will use the provided key to encrypt the data before saving it

Persistent disk encryption with CSEK
  Data is encrypted before it leaves the instance
  System defined or customer supplied keys
  The deletion process renders data irrecoverable


LABS
  User Authentication: Identity-Aware Proxy
    - Use Python to write and deploy a simple App Engine app
    - Enable and disable IAP to restrict access to the app
    - Get user identify information from IAP into your app
    - Cryptographically verify information from IAP to protect against spoofing

  IAM: Qwik Start
    - Explore editor roles
    Prepare a resource for access testing
    Remove project access
    Add Storage permissions
    Verify access