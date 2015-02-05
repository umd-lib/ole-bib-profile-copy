# ole-bib-profile-copy

Perl script for copying OLE bibliographic profiles.

The script interacts directly with the database tables to create a new OLE
bibliographic profile from an existing profile.

The script does not currently copy every single piece of information in the
profile -- see the comments in the script regarding which profile-related
tables it does and does not handle. The script currently copies:

* Constants and default values
* Mappings
* Match points,
* Globally protected fields
* Deleted fields
* Renamed fields.

The script has been tested in the following environment:

* MySQL v5.6.21
* Perl v5.8.8
* Red Hat Enterprise Linux Server v5.11

## Requirements

* Perl
* Perl DBI/DBD modules

## Usage

Before using the script, the appropriate database, username, and password
should be configured in the "setup_sql" function.

Copy the script to your OLE server, and run using the following command:

```
./profile_copy [old id] [new name]
```

where [old id] is the "Batch Process Profile Id" of the bibliographic profile
to copy, and [new name] is the name for the new profile.

## License

This software is provided under the CC0 1.0 Universal license
(http://creativecommons.org/publicdomain/zero/1.0/).