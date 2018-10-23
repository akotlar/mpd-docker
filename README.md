# mpd-docker

Run mpd-perl inside of a Docker instance. Configured for hg38.

### TL;DR
```sh
git clone https://github.com/akotlar/mpd-docker && cd $_
docker build -t mpd ./

# Assuming you have a /mnt/data and wish to mount it as /data inside of the docker container
# that you have ~/data/markers.txt.bed with your targets, and that you wish to write to ~/data/outdir/outfile.txt
# config/hg38.yml comes installed with this docker image, inside of the image
# if you wish, you can pass in your own config
docker run -v ~/data:/data mpd design.pl -b /data/markers.txt.bed -c config/hg38.yml -d ~/data/outdir -o outfile.txt
```
