# Linux User Creation and Basic Configuration (Ansible Role)

## Description

This is used to create and configure a user. At the moment it does the following

 * Creates a named user and group
 * Adds dot files
 * Uploads a public key to allow key based SSH access

## Role Variables

| Name               | Default Value                      | Description                                                       |
| ------------------ | ---------------------------------- | ----------------------------------------------------------------- |
| users_name         | `ansibleUser`                      | The name of the user to be created and configured                 |
| users_group        | `ansibleUser`                      | The group the the user will use                                   |
| users_password     | `ChangeMe!!`                       | The password for the user                                         |
| users_home         | `"/home/{{ users_name }}"`         | The home directory for the user                                   |
| uploadPublicKey    | `true`                             | Should we add our SSH public key the to the users authorized_keys |
| local_public_key   | ``                                 | The path to our public key                                        |
