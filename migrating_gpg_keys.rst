# Export keys
$ gpg --output pubkey.gpg --export {KEY ID}

# export secret key securely using password, merge with public key
$ gpg --output - --export-secret-key {KEY ID} | cat pubkey.gpg - | gpg --armor --ouput pubkeys.asc --symmetric --cipher-algo AES256

# import on other computer
$ gpg --no-use-agent --output - pubkeys.asc | gpg --import

# source: http://montemazuma.wordpress.com/2010/03/01/moving-a-gpg-key-privately/

# trust keys
gpg --edit-key {KEY ID}
gpg> trust

