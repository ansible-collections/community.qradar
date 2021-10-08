# Ansible Collection - community.qradar

[![Run Status](https://api.shippable.com/projects/5e6068ebe4b17a000756145d/badge?branch=master)](https://app.shippable.com/github/ansible-collections/community.qradar/dashboard/jobs) 

**This repository has been archived. Refer to the [ibm.qradar collection repository](https://github.com/ansible-collections/ibm.qradar) instead.**

This repo hosts the `community.qradar` Ansible Collection.

The collection includes the community plugins to help the automation of IBM QRadar SIEM Platform.


## Installation and Usage

### Installing the Collection from Ansible Galaxy

Before using the Community IBM QRadar collection, you need to install it with the `ansible-galaxy` CLI:

    ansible-galaxy collection install community.qradar

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml` using the format:

```yaml
collections:
- name: community.qradar
```


## Testing and Development

If you want to develop new content for this collection or improve what's already here, the easiest way to work on the collection is to clone it into one of the configured [`COLLECTIONS_PATHS`](https://docs.ansible.com/ansible/latest/reference_appendices/config.html#collections-paths), and work on it there.

### Testing with `ansible-test`

The `tests` directory contains configuration for running sanity and integration tests using [`ansible-test`](https://docs.ansible.com/ansible/latest/dev_guide/testing_integration.html).

You can run the collection's test suites with the commands:

    ansible-test sanity
    ansible-test network-integration --inventory /path/to/inventory


## Publishing New Version

The current process for publishing new versions of the IBM QRadar Community Collection is manual, and requires a user who has access to the `community` namespace on Ansible Galaxy to publish the build artifact.

  1. Ensure `CHANGELOG.md` contains all the latest changes.
  2. Update `galaxy.yml` with the new `version` for the collection.
  3. Create a release in GitHub to tag the commit at the version to build.
  4. Run the following commands to build and release the new version on Galaxy:

     ```
     ansible-galaxy collection build
     ansible-galaxy collection publish ./community-qradar-$VERSION_HERE.tar.gz
     ```

After the version is published, verify it exists on the [IBM QRadar Community Collection Galaxy page](https://galaxy.ansible.com/community/qradar).


## More Information

For more information about Ansible's IBM QRadar integration, join the `#ansible-security` IRC channel on [irc.libera.chat](https://libera.chat/), and browse the resources in the [Security Automation Working Group](https://github.com/ansible/community/wiki/Security-Automation) Community wiki page.


## License

GNU General Public License v3.0 or later

See [COPYING](COPYING) to see the full text.

