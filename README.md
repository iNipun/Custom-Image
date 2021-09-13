

Cloud Custom Image

Getting Debian official cloud images

Debian is distributed [freely](https://www.debian.org/intro/free)[ ](https://www.debian.org/intro/free)over the Internet. You can download all of it from any of our

[mirrors](https://www.debian.org/distrib/ftplist). The [Installation](https://www.debian.org/releases/stable/installmanual)[ ](https://www.debian.org/releases/stable/installmanual)[Manual](https://www.debian.org/releases/stable/installmanual)[ ](https://www.debian.org/releases/stable/installmanual)contains detailed installation instructions. And, the

release notes can be found [here](https://www.debian.org/releases/stable/releasenotes).




**Prerequisites**

    ● **Size**. Images must be 100 GB or less when uncompressed, including

    the files

    ● **cloud-init**. Images must have cloud-init 0.7.7 or higher, cloudbase-init,

    coreos-cloudinit, ignition, or bsd-cloudinit installed and configured

    correctly. If image’s default cloud-init configuration lists the NoCloud

    datasource before the ConfigDrive datasource, Droplets created from the

    image will not function properly.

    ● **SSH configuration**. Images must have sshd installed and configured to

    run on boot.


    ● The following image types are supported natively by the Custom Images upload tool:

        ○ [Raw](https://en.wikipedia.org/wiki/IMG_\(file_format\))[ ](https://en.wikipedia.org/wiki/IMG_\(file_format\))[(](https://en.wikipedia.org/wiki/IMG_\(file_format\))[.img](https://en.wikipedia.org/wiki/IMG_\(file_format\))[)](https://en.wikipedia.org/wiki/IMG_\(file_format\))

        ○ [qcow2](https://en.wikipedia.org/wiki/Qcow)

        ○ [VHDX](https://en.wikipedia.org/wiki/VHD_\(file_format\)#Virtual_Hard_Disk_\(VHDX\))

        ○ [VDI](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)

        ○ [VMDK](https://en.wikipedia.org/wiki/VMDK)

    ● Image must support the ext3 or ext4 ﬁlesystems

    ● Image must have cloud-init 0.7.7, cloudbase-init, coreos-cloudinit,

      iginition, or bsd-cloudinit installed

    ● Images must be less than 100 GB uncompressed.

    ● Must add an SSH key when creating Droplets from a custom image.





**Installation**

Go to official website of Cloud-debian Images (link below) to download the supported format and

prerequisites to directly run on Digital Ocean- Custom Image

<https://cloud.debian.org/images/cloud/>

Use generic images under the directory bullseye/latest/<your\_image.qcow2>

● *generic*: Should run in any environment using cloud-init, for e.g. OpenStack,

DigitalOcean and also on bare metal.

*Upload Images*

To upload a custom image of an [accepted](https://docs.digitalocean.com/products/images/custom-images/#image-requirements)[ ](https://docs.digitalocean.com/products/images/custom-images/#image-requirements)[format](https://docs.digitalocean.com/products/images/custom-images/#image-requirements):

1. From the [control](https://cloud.digitalocean.com/)[ ](https://cloud.digitalocean.com/)[panel](https://cloud.digitalocean.com/), in the **Images** section, click the **Custom**

**images** tab.

2. Click the **Upload Image** button to open a file selector, drag and drop to

upload a file directly, or click the **Import via URL** button to provide a link

to an image. The control panel supports uploads from HTTP, HTTPS,

and FTP URLs.

3. Fill in the details of your image, like the name, datacenter region, any

[tags](https://docs.digitalocean.com/products/droplets/how-to/tag/)[ ](https://docs.digitalocean.com/products/droplets/how-to/tag/)you want to use, and notes. Then, click **Upload Image**.

*Create Droplets from Custom Images*

1. From the [Droplet](https://cloud.digitalocean.com/droplets/new)[ ](https://cloud.digitalocean.com/droplets/new)[create](https://cloud.digitalocean.com/droplets/new)[ ](https://cloud.digitalocean.com/droplets/new)[page](https://cloud.digitalocean.com/droplets/new), under **Choose an image**, click **Custom**

**images**.

2. Choose the custom image you want to use.

3. Fill out the rest of the choices on the create page, then click **Create**.

   Add Custom Images to Additional Regions

   You can create Droplets from custom images in the region in which the

   custom image is available. To add a custom image to additional regions:

4. From the [control](https://cloud.digitalocean.com/)[ ](https://cloud.digitalocean.com/)[panel](https://cloud.digitalocean.com/), in the **Images** section, click the **Custom**

**images** tab.

5. From a custom image’s **More** menu, click **Add to region**.

6. In the **Custom image availability** window that opens, select the

   regions you want to add the custom image to.





**Known Issues**

● You cannot see the total storage used by custom images.

● The image upload window does not correctly display the size of the

image.

● Cannot use [IPv6](https://docs.digitalocean.com/products/networking/ipv6/)[ ](https://docs.digitalocean.com/products/networking/ipv6/)with Droplets created from custom images.

● Cannot enable [monitoring](https://docs.digitalocean.com/products/monitoring/)[ ](https://docs.digitalocean.com/products/monitoring/)automatically during Droplet creation when

using a custom image. Instead, [enable](https://docs.digitalocean.com/products/monitoring/how-to/install-agent/#manually)[ ](https://docs.digitalocean.com/products/monitoring/how-to/install-agent/#manually)[monitoring](https://docs.digitalocean.com/products/monitoring/how-to/install-agent/#manually)[ ](https://docs.digitalocean.com/products/monitoring/how-to/install-agent/#manually)[manually](https://docs.digitalocean.com/products/monitoring/how-to/install-agent/#manually).





