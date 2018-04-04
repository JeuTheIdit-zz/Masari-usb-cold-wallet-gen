##### JeuTheIdit

# Masari-usb-cold-wallet-gen

## What is this?

A zip file that contains the open sourced files that you need to create a secure Masari cold wallet on a fresh Linux OS free of malware.

This idea came from taushet's [Monero USB Cold Wallet Generator](https://np.reddit.com/r/Monero/comments/5limu9/taushet_usb_monero_cold_wallet_generator_release/).

## Why should I use this?

A fresh OS and hash check is NOT required when making a cold wallet, but is best practice to make sure that your private keys are completely secure.  Rather than researching what files are needed and checking the individual hashes, new users can save considerable time by downloading this one zip file and following the included instructions, where only one hash check is needed.

## What you need:

- Masari-usb-cold-wallet-gen.zip
- USB drives (only 1 is required, but 3 is helpful)
- Paper
- Pen
- Hash utility.  I used the [built in Windows 10 utility](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/certutil#BKMK_hashfile).  A well known GUI utility is [QuickHash](https://sourceforge.net/projects/quickhash/).

## Download:

You can find the latest releases and contained files on GitHub under [Releases](https://github.com/JeuTheIdit/Masari-usb-cold-wallet-gen/releases).

## Instructions:

1. Download the zip.
2. Physically disconnect from the internet.
3. Check that the SHA256 sum on GitHub under [Releases](https://github.com/JeuTheIdit/Masari-usb-cold-wallet-gen/releases) matches.
4. Extract the zip file.
5. Make a bootable USB of the ISO using Rufus (this is now your *first* USB drive). Agree to all the default settings in the dialog boxes.
6. Drag the masari-wallet-generator-master directory to the *first* USB drive.
7. Reboot using the USB into PuppyLinux (hold down F12 during boot to select boot drive).
8. Open masari-wallet-generator.html in the directory. Generate the wallet seed and keys.
9. Save the seed, address and keys to the *second* USB drive.  Copy/paste, don’t type.  This is your digital vault, not to be used until fund extraction.
10. Write down the seed three times on a single sheet of paper.  This is your physical vault.
11. Save the address and viewkey to the *third* USB drive.  This is your address vault, which can be used with relative abandon.  You can also use this to create a view-only wallet later.
12. Remove *second* and *third* USB drives.
13. Shut down the computer.
13. Remove *first* USB drive (one used to boot into linux). Wipe it, or even better destroy it.
14. Reboot and reconnect to the internet.

You now have a secure cold wallet!

## Risks:

- I have inserted malicious random seeds into the generator and can predict the keys.
  - Checksum the zip file and individual files.  **I have encouraged a community review to be conducted on the [Masari subreddit](https://www.reddit.com/r/masari/).**
- Your unzipping utility has inserted malicious code in a man-in-the-middle attack and thus can predict the keys.
  - Highley unlikley and extremley complex.  Checksum your unzipper.
- Man-in-the-middle attack during download.
  - Not a realistic risk.  Checksum the download.
- BIOS keylogger, physical keylogger, RAM explorers.
   - Check your PC for inline loggers.  RAM explorers are far above my paygrade.  For the truly paranoid, make the wallet on a computer that is and always will be air-gapped.
- An error is made during transcription of the keys or seed.
  - This is really the greatest risk.  Remove distractions, write down the seed multiple times without referring to previous attempts.
