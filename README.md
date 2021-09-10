# balena-frigate

[Frigate](https://blakeblackshear.github.io/frigate/) is a complete and local NVR designed for Home Assistant with AI object detection.
It uses OpenCV and Tensorflow to perform realtime object detection locally for IP cameras.

## Hardware Required

<https://blakeblackshear.github.io/frigate/hardware>

- Intel NUC
- Generic x86-64 w/ Google Coral USB Accelerator
- NVIDIA Jetson Nano w/ Google Coral USB Accelerator
- NVIDIA Jetson TX2 w/ Google Coral USB Accelerator

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![Deploy with balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-frigate&defaultDeviceType=intel-nuc)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application,
flashing a device, downloading the project and pushing it via the [balena CLI](https://github.com/balena-io/balena-cli).

### Environment Variables

| Name                    | Description                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `FRIGATE_RTSP_PASSWORD` | Default password for RTSP camera streams.                                                                         |
| `TZ`                    | Inform services of the [timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) in your location. |
| `SET_HOSTNAME`          | Set a custom hostname on application start. Default is `frigate`.                                                 |

## Usage/Examples

Once your device joins the fleet you'll need to allow some time for it to download the application and start the services.

When it's done you should be able to access the access the app at <http://frigate.local>.

You can use the included `code-server` to modify your `frigate.yml` directly on the device at <http://frigate.local:8080>.

Additional usage instructions for Frigate can be found here: <https://blakeblackshear.github.io/frigate/>.

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.
