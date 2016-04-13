# Opencast System Installation for PUO, Malaysia

Opencast system installation for Mini Lecture Theatre, Politeknik Ungku Omar, Malaysia.

## Getting Started

These instructions will show you how to setup lecture video recording using Opencast system.
Details on Opencast system can be accessed on 
```
http://www.opencast.org.
```

The development and testing still undergoing.

## Version
```
1.0.0
```
### Specifications

Opencast server
```
Currently running on latest version of Centos 7 Linux.
Basic requirements: 2GHz, 4GB+ RAM, 20GB HDD, Internet connection.
```
NAS Server
```
HP Proliant NAS Storage 4TB (To be confirmed)
```
Capture agent
```
Currently we are testing TheRec and MHRI capture agent running on latest version of Debian 7 Linux.
```
### Prerequisites

For Opencast server, a fresh install of Centos 7 Minimal is required.
The ISO image can be downloaded on http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1511.iso.

You will need to have a login credential in order to download Opencast RPM Repository.
Sign up at http://repo.virtuos.uos.de/. Use those login credential during installation later.

### Installing Opencast Server

Make sure you already have a fresh install of Centos 7 Minimal.

On terminal:
```
cd /etc/yum.repos.d
curl -O http://repo.virtuos.uos.de/opencast.repo -d os=el -d version=7 -u rpm-user:rpm-password
cd /etc/yum.repos.d
```
*where rpm-user and rpm-password is your login credential for Opencast RPM Repository.*

Then continue with:

```
yum install epel-release
yum install ffmpeg tesseract hunspell sox
yum install activemq-dist
yum install opencast21-allinone
```
```
cp /usr/share/opencast/docs/scripts/activemq/activemq.xml /etc/activemq/activemq.xml
activemq start
service opencast start
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* Opencast (http://opencast.org)
* TheRec (https://elan-ev.de/produkte_av_therec_english.php)
* MHRI (http://zentrum.virtuos.uos.de/mhri)

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Main Contributors

* **Mohd Assidiq Bin Che Ahmad** - *Opencast System Installation and Testing*
* **Dr. Hasnim** - *Capture Agent Installation and Testing*

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

None

## Acknowledgments

* Politeknik Ungku Omar, Malaysia
