# CPSC352-Signed-Software-Release-Project

# Team Members

| Name | Contributions |
|-----|-----|
| Joshua Pavon | Github Repo configuration (hello.cpp, README.md) |
| Brandon Cheng | Enter Contributions |
| Brian Nguuyen | Enter Contributions |
| Loi Tran | Enter Contributions |
| Mike Truong | Enter Contributions |

---

# Instructions

### Prerequisites
- GPG
- Git Bash

## Creating a New Release

1. Make and commit changes
  
3. Create a signed tag:
git tag -s vX.X -m "Example version"

4. Push tag to Github:
git push origin vX.X

4. Github Actions automatically builds, signs, and publishes the release

## Verifying Digital Signatures

1. Download release assets from the Releases page:
  - 'hello.exe'
  - 'SHA25SUMS'
  - 'SHA256SUMS.asc'
    
2. Import developer's public key:
gpg --import developer_public.asc

3. Verify signature on SHA256SUMS:
gpg --verify SHA256SUMS.asc SHA256SUMS

4. Verify if binary matches checksum:
sha256sum --check SHA256SUMS
