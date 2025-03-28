# Ansible role for setting up fileserver and clients

Support file sharing for different operating systems

## Types of file shares

### public_file_shares

    * provide readonly access for anonymous users
    * provide read/write access to authenticated users

### public_readonly_file_shares

    * provide readonly access for anonymous users
    * provide read access for authenticated users
    * provide write access for file owners
    * authenticated users can not change files of each other

### private_file_shares

    * access for anonymous users is prohibted
    * provide read/write access to authenticated users
    * authenticated users can change files of each other

### private_readonly_file_shares

    * access for anonymous users is prohibted
    * provide readonly access to authenticated users
    * authenticated users can read files of each other

## Types of services

### SMB

This network file protocol is used by windows client. Samba is used as file server and configuration
of file shares take care of the different security models of the file share types.
