# Workflow AI

Note: these instructions may look technical, but they don't require any specialized knowledge. If you have any problems or concerns, please reach out to raymond [at] valuebetventures.com

Or feel free to open an issue on this repo!

## Getting started with the Private PDF Extractor:

1. Download Docker Desktop. This allows you to run software locally, securely, and for free.
2. Open Docker Desktop. Click on the search bar on the top, and type `workflowai/private-pdf-extractor`
3. Click on the Images tab, and you should see the `workflowai/private-pdf-extractor` image as the first result. Click on it, click Run, and expand the optional settings. In the Host port section, type 8080
4. Click on Run! It'll take several minutes to get started the first time, but every subsequent run will be fast. Once you see the Logs output say something like "NiceGUI ready to go on http://localhost:8080, and http://172.17.0.2:8080", then open http://localhost:8080 in your favorite browser.
5. Congratulations! You should be up and running.

Please note that the first PDF will be slow to process and requires an active internet connection: the software needs to download the latest AI models to parse the file. Every PDF after the first one should be processed in a few seconds.

At this point, feel free to turn off the internet if you'd like to guarantee your most sensitive files will be secure. Doing this is only for your peace of mind; with or without internet, no data ever leaves your computer at any time.

## Troubleshooting

### linux/arm64 incompatible

We originally built the image with `linux/arm64` only; this caused issues for some users. Now we've deployed with a multi-platform image. Affected users can pull the latest image and try again!

### Windows Hypervisor is not present

If you see an error like `Docker Desktop — Windows Hypervisor is not present`, try following the steps [described here](https://levelup.gitconnected.com/how-to-enable-virtualization-docker-installation-error-46587f1e2686?gi=2a26c4a5687b).
