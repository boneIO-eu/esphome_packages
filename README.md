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

### Sofar Inverter KTL

Code snippet:
```yaml
  sofar_inverter:
    url: https://github.com/boneIO-eu/esphome-packages/
    files:
      - path: sofar-inverter.yaml
        vars: 
          modbus_controller_id: 'sofar_modbus'
          name: 'Sofar'
          modbus_device_id: 'sofar_modbus'
          modbus_device_address: '0x01' #CHANGE THIS
          modbus_id: 'boneio_modbus'
          update_interval: '60s'
```

### Liquid sensor measuring depth of liquid / RS485

Code snippet:
```yaml
  liquid_sensor:
    url: https://github.com/boneIO-eu/esphome-packages/
    files:
      - path: liquid-sensor.yaml
        vars: 
          modbus_controller_id: 'liquid_modbus'
          name: 'Liquid sensor'
          modbus_device_id: 'liquid_modbus'
          modbus_device_address: '0x01' #CHANGE THIS
          modbus_id: 'boneio_modbus'
          update_interval: '60s'
          width: '10'
          length: '10'
```

### SDM630 Energy Meter

Code snippet:
```yaml
  sdm630:
    url: https://github.com/boneIO-eu/esphome-packages/
    files:
      - path: sdm630.yaml
        vars: 
          modbus_controller_id: 'sdm630_modbus'
          name: 'SDM630'
          modbus_device_id: 'sdm630_modbus'
          modbus_device_address: '0x01' #CHANGE THIS
          modbus_id: 'boneio_modbus'
          update_interval: '60s'
```

### Thessla Green Airpack 4

Code snippet:
```yaml
  thessla_green_airpack_4:
    url: https://github.com/boneIO-eu/esphome-packages/
    files:
      - path: thessla-green-airpack-4.yaml
        vars: 
          modbus_controller_id: 'thessla_green_airpack_4_modbus'
          name: 'Thessla Green Airpack 4'
          modbus_device_id: 'thessla_green_airpack_4_modbus'
          modbus_device_address: '0x01' #CHANGE THIS
          modbus_id: 'boneio_modbus'
          update_interval: '60s'
```

## Contributing

Contributions are welcome! Feel free to submit pull requests with new packages or improvements to existing ones.

## License

GPL License.
See the LICENSE file for details.
