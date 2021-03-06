# vmware-tools Cookbook

## Scope

Chef cookbook for installing [VMware tools](https://docs.vmware.com/en/VMware-Tools/index.html).

## Attributes

- `default['vmware-tools']['update']` - default set to `true`, you know you want
  the newest _always_.
- `default['vmware-tools']['windows_reboot']` - default set to `true`, and if
  put at the first cookbook you'll reboot then run the rest of the `run_list`.
- `default['vmware-tools']['url']` - The location to get the Windows VMware-Tools
  executable from.
- `default['vmware-tools']['version']` - The version of the Windows VMware-Tools.

## Usage

### vmware-tools::default

The default recipe will install [open-vm-tools](https://github.com/vmware/open-vm-tools)
  of on a CentOS/Debian based machine. If you run this on Windows it installs the
  public VMware Tools executable from [packages.vmware.com](https://packages.vmware.com).

If you have a specific place you want to install your Windows based VMware Tools
  from, override the `default['vmware-tools']['url']`
  and `default['vware-tools']['version']` in the default attributes.

## Testing

For more details look at the [TESTING.md](./TESTING.md).

## License & Authors

**Author:** tecRacer Opensource Team ([opensource@tecracer.de](mailto:opensource@tecracer.de))
**Original Author:** JJ Asghar [GitHub](https://github.com/jjasghar)
**Original Author:** Andrew Fraley [GitHub](https://github.com/andrewfraley/)

**Copyright:** 2020, tecRacer Group

```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
