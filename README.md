# checkROMs
Generate and check md5 checksums for ROM images.
```
Usage: checkROMs [OPTIONS]

OPTIONS
 -h|--help                         :    Display this output.
 -n|--now                          :    Check ROM's now.
 -c|--check FILENAME               :    Check checksums from the specified checksum file.
 -g|--generate FILESPEC[,FILESPEC] :    Create ROM checksums using the specified FILESPEC.
 -p|--path PATH                    :    Base path used when generating checksums.
 -d|--days NUMDAYS                 :    Number of days since last check.

Usage Examples
Generate a checksum file for ZIP files located under /home/pi.
 ./checkROMs -p /home/pi -g *.zip > checksum.md5

Check generated checksum file. If a check has been performed
within the default 30 days or specified number of days, no check is performed.
 ./checkROMs -c checksum.md5

Check generated checksum file only is 10 days has passed since it was last checked.
 ./checkROMs -c checksum.md5 -d 10

Force check of generated checksum file.
 ./checkROMs -c checksum.md5 -n
```
