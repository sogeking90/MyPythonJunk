import os
import time

#1. The files and directories to be backed up are
#specified in a list.
source = ['/home/nharper/Downloads/']

#2. backup must be stored in a main backup directory
#for example:
target_dir = '/home/nharper/Downloads_backup'
#the files are backed up into a .zip
#the name of the zip is the current date and time.
target = target_dir + os.sep + \
    time.strftime('%Y%m%d%H%M%S' + '.zip')

#create the directory if it doesn't already exist.
if not os.path.exists(target_dir):
    os.mkdir(target_dir)  # Make directory

#5. we use the zip command
zip_command = "zip -r {0} {1}".format(target, ' '.join(source))

#run the backup
print 'zip command is:'
print zip_command
print 'Running'

if os.system(zip_command) == 0:
    print "Successful backup to", target
else:
    print 'Backup FAILED'
