Confirm the following are included in your repo, checking each box:

 - [ ] completed README.md file with the necessary information
 - [ ] shim.efi to be signed
 - [ ] public portion of your certificate(s) embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [ ] binaries, for which hashes are added to vendor_db ( if you use vendor_db and have hashes allow-listed )
 - [ ] any extra patches to shim via your own git tree or as files
 - [ ] any extra patches to grub via your own git tree or as files
 - [ ] build logs
 - [ ] a Dockerfile to reproduce the build of the provided shim EFI binaries

*******************************************************************************
### What is the link to your tag in a repo cloned from rhboot/shim-review?
*******************************************************************************
`https://github.com/user/shim-review/tree/myorg-shim-arch-YYYYMMDD`

*******************************************************************************
### What is the SHA256 hash of your final SHIM binary?
*******************************************************************************

Output from sha256sum:

$ sha256sum shimia32.efi

7620c859572a45524f36ef89bedaa05b05f0f3a9daefca4566b19516cef4ae9c  ./shimia32.efi

$ sha256sum shimx64.efi

36b17db9300b8e90c11e86ec646b5b3975bfaf834ec10ecb2954bd49136fa8c1  ./shimx64.efi

Output from pesign:

$ pesign --hash --padding --in=shimia32.efi

hash: 800377346f8461fa5f85a41aebc1c41f4dab86f7356f3b43f82277f26a4c622d

$ pesign --hash --padding --in=shimx64.efi

hash: 8ed0ca1a25fd7bf38f03a9cdb350673f3dc62ea9e18daee365c9024df381abf1

*******************************************************************************
### What is the link to your previous shim review request (if any, otherwise N/A)?
*******************************************************************************
https://github.com/rhboot/shim-review/issues/183

*******************************************************************************
### If no security contacts have changed since verification, what is the link to your request, where they've been verified (if any, otherwise N/A)?
*******************************************************************************
https://github.com/rhboot/shim-review/issues/419
