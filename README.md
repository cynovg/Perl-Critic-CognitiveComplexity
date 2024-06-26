[![Build Status](https://travis-ci.org/cynovg/Perl-Critic-CognitiveComplexity.svg?branch=master)](https://travis-ci.org/cynovg/Perl-Critic-CognitiveComplexity) [![MetaCPAN Release](https://badge.fury.io/pl/Perl-Critic-CognitiveComplexity.svg)](https://metacpan.org/release/Perl-Critic-CognitiveComplexity)
# NAME

Perl::Critic::CognitiveComplexity - Cognitive Complexity, Because Testability != Understandability

# DESCRIPTION

Perl::Critic::Policy::CognitiveComplexity::ProhibitExcessCognitiveComplexity is a rule that checks the
cognitive complexity score of your subroutines. It is based on a new scoring algorithm introduced by
SonarSource. See [SonarSource blog entry](https://blog.sonarsource.com/cognitive-complexity-because-testability-understandability/).

## Rules

- [CognitiveComplexity::ProhibitExcessCognitiveComplexity](https://metacpan.org/pod/Perl%3A%3ACritic%3A%3APolicy%3A%3ACognitiveComplexity%3A%3AProhibitExcessCognitiveComplexity) - Avoid code that is nested, and thus difficult to grasp. 
Examples can be seen in the Policy POD.

## Configuration

The default complexity score before code starts to be reported with medium severity, is 10. This can be changed by changing the `warn_level` parameter.
By default all subroutines with complexity level of more than 0 are reported in lowest severity level. This allows third-party tools to pick up these 
values as code metrics.

    [Perl::Critic::Policy::CognitiveComplexity::ProhibitExcessCognitiveComplexity]
    warn_level = 10
    info_level = 1

# SEE ALSO

[Perl::Critic](https://metacpan.org/pod/Perl%3A%3ACritic)

# COPYRIGHT

Copyright (C) 2017 Oliver Trosien

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

Oliver Trosien <cpan@pocket-design.de>
