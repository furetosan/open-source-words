the php interpreter this is the github mirror of the official php repository located at https git php net pull requests php accepts pull requests via github discussions are done on github but depending on the topic can also be relayed to the official php developer mailing list internals lists php net new features require an rfc and must be accepted by the developers see https wiki php net rfc and https wiki php net rfc voting for more information on the process bug fixes do not require an rfc but require a bugtracker ticket always open a ticket at https bugs php net and reference the bug id using nnnnnn fix 55371 get magic quotes gpc throws deprecation warning after removing magic quotes the get magic quotes gpc function caused a deprecate warning get magic quotes gpc can be used to detected the magic quotes behavior and therefore should not raise a warning at any time the patch removes this warning we do not merge pull requests directly on github all prs will be pulled and pushed through https git php net guidelines for contributors coding standards readme git rules readme mailinglist rules readme release process