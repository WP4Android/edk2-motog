# edk2-motog
UEFI port for Motorola Moto G Power, Moto G Stylus, Moto G Pro, Moto G Power, Moto G8, and Moto G Fast

## Supported Devices (WIP)

Motorola G Power = sofia

Motorola G Stylus = sofiap

Motorola G Pro = sofiap_ao

Motorola G8 Power = sofiar

Motorola G8 = rav

Motorola G Fast = rav_t

## Building

sudo apt update

sudo apt upgrade

sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git

mkdir edk2-porting && cd edk2-porting

git clone https://github.com/tianocore/edk2.git --recursive

git clone https://github.com/tianocore/edk2-platforms.git

git clone https://github.com/AndroidDevice-Porting/edk2-motog.git

cd edk2 && make -C Basetools/

source edksetup.sh

cd ../edk2-motog

chmod +x build.sh

chmod +x build_common.sh

bash build.sh

## Status

More than likely not working. There might be some messed up memory maps, Maybe something else is messed up? But definately not ready. It is only public __in case someone can help us work on it.__ From what I have heard, devices with a Qualcomm Snapdragon 665 processor are supposedly impossible to use EDK2, but from my 18 years of hearing things are "impossible," that is dumb. I mean, people said things like portable electronics (phones, etc.) and some types of aircraft would be impossible, but here we are today. So lesson is, nothing is impossible.

## Device specs?

__All Phone Models__
> SoC = Qualcomm Snapdragon 665
> 
> RAM = 4GB

## Device Specifics?

**Looking at some of the other device specs online, the storage size differs. But the storage type seems the same. Some also have the Android 11 update, while some don't. Lastly, the screen resolution on the Moto G8 is 720x1560. So keep these in mind when you are trying to use this / help with it.**
