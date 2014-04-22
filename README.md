# NAME

mddeliver - deliver a message to a Maildir with optional flags

# DESCRIPTION

Mail filtering tools such as [maildrop(1)](http://man.he.net/man1/maildrop) provide an effective way to
determine which mailbox a message should be delivered to, but provide no way to
automatically process that message once delivered.

For example, it may be desirable to automatically set all spam messages to be
"seen" so that they don't appear in an unread message count.

`mddeliver` is a simple Perl script which accepts an RFC2822-formatted message
on its standard input, delivers it to a given Maildir directory, and then sets
the status of the message according to the arguments provided.

# USAGE

        cat message | mddeliver [OPTIONS]

# OPTIONS

- --help

    Display usage and options.

- --dir=DIRECTORY

    The location of the Maildir directory.

- --draft

    The message is a draft.

- --flagged

    The message has been _flagged_ for some purpose, for instance as result of a
    search for spam in a folder.

- --passed

    The message was bounced or forwarded to someone else.

- --replied

    The message has been replied to.

- --seen

    The message has been seen, i.e. it is not "unread".

# SEE ALSO

- [Mail::Message](https://metacpan.org/pod/Mail::Message)
- [Mail::Box::Maildir](https://metacpan.org/pod/Mail::Box::Maildir)

# COPYRIGHT

Copyright 2014 Gavin Brown. This program is Free Software; you can use it and/or
modify it under the same terms as Perl itself.
