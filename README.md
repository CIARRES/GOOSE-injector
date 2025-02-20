# GOOSE-injector

A simple tool to inject GOOSE (Generic Object-Oriented Substation Event) packets into a substation local network.

## Building

To build the Docker image locally, run:

```sh
docker build . -t goose-injector:latest
```

Alternatively, you can pull the pre-built image from Docker Hub:

```sh
docker pull javiersande/goose-injector:latest
```

## Deployment

Run the container with the following command:

```sh
docker run -it --name goose-injector --network <network_name> --ip <ip> goose-injector:latest
```

### Deployment Notes:
- `<network_name>` should be a custom Docker network that allows communication with the target devices.
- `<ip>` is the desired static IP address within the network. Ensure it does not conflict with other devices.

## Usage

Once deployed, the tool will inject GOOSE packets into the specified network. Ensure you have the necessary permissions to run packet injection tools in your environment.
