# SSH
ssh username@host -p PORT             # Login to remote server
ssh -i keyfile username@host -p PORT  # Login using private key

# File navigation & viewing
ls -la                               # List all files
cd /path/to/dir                       # Change directory
cat filename                           # View file content
less filename                          # Scrollable view
file filename                           # Check file type
head/tail filename                     # View first/last lines

# File search
find /path -name "filename"            # Search by name
grep "pattern" filename                # Search by content
diff file1 file2                        # Compare files

# Text decoding & encoding
xxd -r file.hex > file                 # Hex dump to binary
base64 -d file.b64                     # Base64 decode
tr 'A-Za-z' 'N-ZA-Mn-za-m'            # ROT13

# Permissions
chmod 600 keyfile                       # Restrict SSH key
chmod 700 script.sh                     # Make executable
chown user:group file                    # Change owner

# Networking & port testing
nmap -p 31000-32000 localhost           # Scan ports
openssl s_client -connect localhost:PORT  # Check SSL service
nc localhost PORT                        # Connect to port

# Setuid binaries
./binary                                # Run setuid binary

# Cron jobs
ls /etc/cron.d/                          # List scheduled jobs
man 5 crontab                            # Cron config manual

# Misc
mkdir /tmp/tempdir                        # Create temporary directory
mktemp -d                                 # Create random temp directory
