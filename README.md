# virtualbox

Install Oracle VirtualBox.

## Requirements

None

## Role Variables

### REQUIRED

None

### OPTIONAL

* virtualbox_repo: The yum repository to download VirtualBox from. 
  Defaults to the publicly available one for rpms. 
  Can override to use Artifactory remote repository.
* virtualbox_version: The major version of VirtualBox to install.
* virtualbox_user: The user to which will run VirtualBox.
  Defaults to 'jenkins' as this role was intended to run through CI/CD.

## Dependencies

None

## Example Playbook

    - hosts: servers
      vars:
        virtualbox_version: "6.0"
        virtualbox_repo: "http://artifactory.COMPANY.com/artifactory/download.virtualbox.org/virtualbox/rpm/el/$releasever/$basearch"
      roles:
         - role: virtualbox

## License

BSD

## Author Information

Jeremy Cornett <jeremy.cornett@forcepoint.com>
