# Sophos
sophos Installation with ansible on linux

Download : https://www.sophos.com/en-us/products/free-tools/sophos-antivirus-for-linux.aspx tar

# Follow below steps:
- tar -xzvf sav-linux-free-9.tgz
- ./sophos-av/install.sh
- Y (accept license)
- /opt/sophos-av
- Y (on-access scanning)
- Sophos to autoupdate (s)
- free (f)
- Proxy (N)
- ./sophos-av/install.sh --acceptlicense --instdir=/opt/sophos-av --enableOnAccess=true --sophos --update-type=s --update-source-username=(yoursusername) --update-source-password=(your password) --extra-options="--preferFree" --automatic --enableOnBoot=True

template reference:

truefalsefalsefalse600003000010000talpa_vfshook25true560falsetruefalsefalsefalsefalsetrue/dev/sophos-vc10004096true20000200051020000UTF-8EUC-JPISO-8859-10100./lib/sav./lib/savfalse00010203nix.sophosxl.netext3ext4ext2tmpfsdevtmpfsiso9660udfxfsreiserfsjfsvfatmsdosntfshfsminixramfsromfsufsumsdosxenixcramfsenabledisablefalse/1000060000truefalsefalsetrueFalse50True./logsavd100log.errorlog.threatTrueDAEMONenabledTrueTrueenabledlocalhost:25truetruetrueFATALfalsetrueEnglishUSING_BACKUP_CONFIGURATIONALL_UPDATE_SOURCES_FAILEDRESPAWN-LIMITVIRUS-DATA-OLDTALPA-FAILURETALPA-COMPILEDroot@localhosttruetruetrue8081adminsdds:SOPHOSfalsefalsetruerecommendedtrue8192fileupload.sophosxl.netfileupload.sophosxl.netfalse011{{ hostvars[groups['common'][0]]['sophos_source_username'] }}/opt/sophos-av/update/cache/Primary0sophos:{{ hostvars[groups['common'][0]]['sophos_source_password'] }}600
The credentials are fetched from https://amicreds.sophosupd.com/freelinux/creds.dat

Notes: ■ To run an on-demand scan of the computer, type: savscan / #Added extra files

./sophos-av/./install.sh --acceptlicense --instdir=/opt/sophos-av --enableOnAccess=true --sophos --update-type=s --update-source-username=yourusername --update-source-password=yourpassword --AllDistros=0 --Source=sophos: --automatic --enableOnBoot=True
