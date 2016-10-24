# qlik-sense-automated-install
Installation of Qlik Sense via Powershell

This script installs Qlik Sense 3.1.1 with the following:

1. Central Node
2. Domain account as Service Account
3. PostgresDB password on

Utilises Qlik-CLI (https://github.com/ahaydon/Qlik-Cli) to perform license step.

## User Account
Note: Does not create the service account, please create within Domain or Local system before running.

## Usage
install-qs.ps1 -serial '' -control '' -name '' -organization '' -serviceAccount '' -serviceAccount2 '' -serviceAccountPass '' -PostgresAccountPass '' -hostname ''

### Parameter Examples
1. Serial = Qlik Sense serial number
2. Control = Qlik Sense control number
3. name = Name of licensee
4. organization = Organization of licensee
5. serviceaccount = service account to run Qlik services (computername\username) or (domain\username)
6. serviceaccount2 = service account to run Qlik services (computername/username) or (domain/username)
7. serviceaccountpass = password of service account
8. postgresAccountPass = password for postgres super user

### Usage Example
install-qs.ps1 -serial '883213213' -control '32134' -name 'Qlik' -organization 'Qlik' -serviceAccount 'QS1\Qservice' -serviceAccount2 'QS1/Qservice' -serviceAccountPass 'Pass@word1' -PostgresAccountPass 'Pass@word1' -hostname 'QS1'

# License

This software is made available "AS IS" without warranty of any kind. Qlik support agreement does not cover support for this script.
