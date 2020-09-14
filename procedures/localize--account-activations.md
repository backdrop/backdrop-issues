Use case: A person wants to contribute to the Backdrop translation of a specific
language.

## (1) Prospective contributor registers for user account

- The prospective contributor goes to https://localize.backdropcms.org/user/register.
- They fill the form with User name, Mail address and a Message. The latter is
  to let the moderators know about the kind of contribution and the language
  they're interested in. (Example: "I'd like to submit translation suggestions
  for Spanish.")

## (2) Site manager activates the account

- The new account triggers the action "Send e-mail about new account to a site
  manager". Recipients of the action (currently [Olaf](https://github.com/olafgrabienski)
  and [Greg](https://github.com/klonos)) receive an email containing user
  information (and, in theory, the message, see https://github.com/backdrop-ops/localize.backdropcms.org/issues/35).
- The site manager goes to localize.backdropcms.org/user?destination=admin/people,
  looks for the new account, and (until https://github.com/backdrop-ops/localize.backdropcms.org/issues/35
  is fixed) looks for the message of the prospective contributor.
- If the registration and the message look good, the site manager activates the
  account.

## (3) Site manager checks for language and translation group

Depending on the contributor message, there are two possible situations: the
language of interest exists on the translation server, or it doesn't exist yet.
If it doesn't exist, the language and the respective translation group have to
be created first:

- Go to https://localize.backdropcms.org/admin/config/regional/language/add, and
  add a new language.
- Go to https://localize.backdropcms.org/node/add/l10n-group, and add a
  translation group for the language.

Note: As node author, you are the first member of this group, and you'll reveive
group application messages (see below).

## (4) Site manager gets in touch with the contributor

Assumption: Language and translation group exist.

Go to the newly activated user account (double check if it has been enabled,
and enable it if not), switch to the "Contact" tab, and send a welcome message
to the contributor. The text details will depend on the situation (new vs.
existing language, etc.). Here's an example regarding a contributor who wants to
contribute to a new language:

> Subject: [LANGUAGE] translation group
>
> Hello [USER NAME],
>
> Thanks for registering an account on https://localize.backdropcms.org!
>
> You wrote, you'd like to translate Backdrop to [LANGUAGE]. I've created the
> [LANGUAGE] group and activated your user account. As a next step, please visit
> https://localize.backdropcms.org/translate/languages/[LANGUAGE-CODE], look for
> the group block at the bottom of the right sidebar, and apply for group
> membership.
>
> As we're not able to evaluate translations into [LANGUAGE], it would make
> sense to provide your account then with the role of a "Translation
> supervisor". As a user with that role, you'd be able to translate right away,
> and import language files without the need of another member to confirm your
> suggestions. Are you fine with being assigned that role?
>
> All the best,
> [NAME]

## (5) Manage new group membership

When the new contributor applies for group membership, the group author
receives an email notification.

- Go to `group/node/NID/admin/people`, set the Status of the new member to
  "Active", and update the membership.
- (optional) Edit the group account again, and choose an additional role,
  usually "translations supervisor".
- Go to the user account contact tab, and send a message with instructions.
  Example:

> Subject: [LANGUAGE] translation instructions
>
> Hello [NAME],
> Thanks for your group application! I've enabled your membership and updated
> your role for the [LANGUAGE] group. You can translate single language single
> strings on the page https://localize.backdropcms.org/translate/languages/[LANGUAGE]-CODE/translate,
> or import .po language files with translations on the page
> https://localize.backdropcms.org/translate/languages/[LANGUAGE]-CODE/import.
>
> By the way, if you have translation files of Drupal core, or of Drupal modules
> that have been included in Backdrop core (like Views or CKEditor), you can
> also import these.
>
> Please send me a message when you've done any import(s), or whenever you've
> completed a larger quantity of translations. To make sure that these strings
> show up in the download files, we have to 'repackage' the releases on the
> translation server.
>
> All the best, and happy translating,
> [NAME]

## (6) Repackage language release

When a contributor has imported or translated many language strings, the files
have to be repackaged.

- Go to https://localize.backdropcms.org/admin/l10n_server/packager
- Choose a project (usually Backdrop)
- Select a language
- Click "Repackage now"
- Flush the "Page and else" cache
