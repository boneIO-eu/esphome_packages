# boneIO ESPHome Community Packages

This repository contains a collection of ESPHome packages created by the boneIO community. These packages are designed to be easily imported into your ESPHome configurations using the packages section.

## Usage

To use these packages in your ESPHome configuration, add them to the `packages:` section of your YAML configuration file:

```yaml
packages:
  my_package:
    url: https://github.com/boneIO-eu/esphome-packages/
    files:
      - path: package_name.yaml
        vars: 
```

Replace `package_name.yaml` with the name of the specific package you want to use.
Check inside `package_name.yaml` for the available variables.

For modbus devices we require following variables:

- `modbus_controller_id` - ID of the modbus controller
- `name` - Name of the device
- `modbus_device_id` - ID of the modbus device
- `modbus_device_address` - Address of the modbus device
- `modbus_id` - ID of the modbus bus
- `update_interval` - Update interval of the device

## Compatibility

These packages are compatible with ESPHome version 2025.3 and newer.

## Available Packages

- List of available packages will be updated as they are added to the repository

### Modbus devices

- Sofar Inverter KTL
- Liquid sensor measuring depth of liquid / RS485
- SDM630 Energy Meter
- Thessla Green Airpack 4

## Contributing

Contributions are welcome! Feel free to submit pull requests with new packages or improvements to existing ones.

## License

See the LICENSE file for details.
