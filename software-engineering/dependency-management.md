# [Dependency Management](https://semver.org/)

In the world of software management there exists a dreaded place called “dependency hell.” The bigger your system grows and the more packages you integrate into your software, the more likely you are to find yourself, one day, in this pit of despair.

**Version Lock**: the inability to upgrade a package without having to release new versions of every dependent package

**Version Promiscuity**: assuming compatibility with more future versions than is reasonable

**Depenedency Hell**: Dependency hell is where you are when version lock and/or version promiscuity prevent you from easily and safely moving your project forward.

**[Semantic versioning (aka SemVer)](https://en.wikipedia.org/wiki/Software_versioning)**: is a widely-adopted version scheme that encodes a version by a three-part version number (Major.Minor.Patch), an optional pre-release tag, and an optional build meta tag. In this scheme, risk and functionality are the measures of significance. Breaking changes are indicated by increasing the major number (high risk); new, non-breaking features increment the minor number (medium risk); and all other non-breaking changes increment the patch number (lowest risk). The presence of a pre-release tag (-alpha, -beta) indicates substantial risk, as does a major number of zero (0.y.z), which is used to indicate a work-in-progress that may contain any level of potentially breaking changes (highest risk). As an example of inferring compatibility from a SemVer version, software which relies on version 2.1.5 of an API is compatible with version 2.2.3, but not necessarily with 3.2.4.S

 Consider a version format of X.Y.Z (Major.Minor.Patch): Bug fixes not affecting the API increment the patch version, backward compatible API additions/changes increment the minor version, and backward incompatible API changes increment the major version.

## [Key words for use in RFCs to Indicate Requirement Levels](https://datatracker.ietf.org/doc/html/rfc2119)

[Request for Comments](https://en.wikipedia.org/wiki/Request_for_Commentshttps://en.wikipedia.org/wiki/Request_for_Comments): a publication in a series from the principal technical development and standards-setting bodies for the Internet, most prominently the Internet Engineering Task Force (IETF). An RFC is authored by individuals or groups of engineers and computer scientists in the form of a memorandum describing methods, behaviors, research, or innovations applicable to the working of the Internet and Internet-connected systems. It is submitted either for peer review or to convey new concepts, information, or, occasionally, engineering humor.

1. **MUST**:   This word, or the terms "REQUIRED" or "SHALL", mean that the
   definition is an absolute requirement of the specification.

2. **MUST NOT**:   This phrase, or the phrase "SHALL NOT", mean that the
   definition is an absolute prohibition of the specification.

3. **SHOULD**:   This word, or the adjective "RECOMMENDED", mean that there
   may exist valid reasons in particular circumstances to ignore a
   particular item, but the full implications must be understood and
   carefully weighed before choosing a different course.

4. **SHOULD NOT**:   This phrase, or the phrase "NOT RECOMMENDED" mean that
   there may exist valid reasons in particular circumstances when the
   particular behavior is acceptable or even useful, but the full
   implications should be understood and the case carefully weighed
   before implementing any behavior described with this label.
   
5. **MAY**:   This word, or the adjective "OPTIONAL", mean that an item is
   truly optional.  One vendor may choose to include the item because a
   particular marketplace requires it or because the vendor feels that
   it enhances the product while another vendor may omit the same item.
   An implementation which does not include a particular option MUST be
   prepared to interoperate with another implementation which does
   include the option, though perhaps with reduced functionality. In the
   same vein an implementation which does include a particular option
   MUST be prepared to interoperate with another implementation which
   does not include the option (except, of course, for the feature the
   option provides.)

### Guidance in the use of these Imperatives

   Imperatives of the type defined in this memo must be used with care
   and sparingly.  In particular, they MUST only be used where it is
   actually required for interoperation or to limit behavior which has
   potential for causing harm (e.g., limiting retransmisssions)  For
   example, they must not be used to try to impose a particular method
   on implementors where the method is not required for
   interoperability.

### Security Considerations

   These terms are frequently used to specify behavior with security
   implications.  The effects on security of not implementing a MUST or
   SHOULD, or doing something the specification says MUST NOT or SHOULD
   NOT be done may be very subtle. Document authors should take the time
   to elaborate the security implications of not following
   recommendations or requirements as most implementors will not have
   had the benefit of the experience and discussion that produced the
   specification.

<!--
https://en.wikipedia.org/wiki/Software_versioning

make notes for software versioning
-->