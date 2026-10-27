## Description
<!-- What changed and why, in your own words — the user-facing story and the technical one. Link the work: the ticket ("XNAT-1234"), "Closes #123" (auto-closes on merge, so only if this PR fully resolves it), "Related to #123", or the merge order if this is stacked on another PR. Detail meant to outlive this PR belongs in the code, the docs, or the ticket. If you used AI to help draft this, read it and edit it before you post. -->

## Release note
<!-- Write this yourself, for the people who install, administer, and use this software rather than for reviewers: it may be copied into the release notes as written. In a few sentences, say what changed from their point of view, who it affects, and anything they need to do about it, such as a configuration change or a step before or after upgrading. Call out any change to existing behavior, even a fix. If nothing is user-visible (a refactor, or a build-, CI-, or test-only change), write "None" so we know it wasn't skipped. -->

## Risks and impact
<!-- Every change carries some risk; this is where you name the risks you know about. Answer the sections that apply and delete the rest. How much attention each deserves is your call. -->

### PHI and de-identification
<!-- Does this touch anonymization, DicomEdit scripts, an importer, the prearchive, or anything that writes into the archive? Could an identifier survive a path that used to scrub it? Does this send imaging data or its metadata out of XNAT — to a container, a remote XNAT or PACS, or another service — or into a log? -->

### Security, authentication, and authorization
<!-- Do your changes add or modify roles, or change what data a user can see or what actions they can take? If you added a REST endpoint, who is allowed to call it? Could a user edit a REST path and reach a project they aren't a member of? If this handles credentials for another system, such as passwords, tokens, or keys, are they kept out of logs, the UI, and API responses? Were you mindful of least privilege? See the [OWASP checklist](https://github.com/0xRadi/OWASP-Web-Checklist). -->

### Input data
<!-- Which edge cases did you consider? DICOM type 2 elements are required to be present but may be empty; private tags, multiframe objects, and non-conforming data from real scanners all show up in the wild. Settings that admins enter and responses from external systems count as input too, including a system that doesn't answer. On bad data, does this fail loudly or quietly? -->

### Upgrade and compatibility
<!-- Only a major release may break backward compatibility; if this PR does and the release it's headed for isn't one, raise it with the maintainers before it merges. Plugins and other libraries follow semantic versioning, where only a change to the first number is major. XNAT numbers its versions differently: the leading 1 never changes and the second number is the major version, so 1.11 and 1.12 are major releases and 1.10.x is not. Does this change which XNAT versions the plugin builds against or runs on? If so, say which ones it supports now, so the [compatibility matrix](https://github.com/NrgXnat/xnat-compatibility) can be updated at release. How do you know a site already running this can take the upgrade? Say what you checked in data types and their schemas, database tables, settings, the REST API, and dependencies, and whether scripts, clients, and other plugins that call this one still work. If something does break, name it and say who has to change. If there is a schema or data migration, how long does it run on a large archive, and does the site need to be down for it? -->

### Performance and scale
<!-- At what scale do we expect this to run — study size, session or project count, concurrent uploads or jobs? How have you verified that it holds up? -->

## Testing
<!-- Please don't delete this section. At a minimum, show proof that this change was deployed and executed successfully: a green build is not sufficient. Show the evidence — commands and their output, screenshots, before/after values, log lines, the data you threw at it — and reference the areas of impact above. A model writing a test is not the same as you confirming the behavior. Not every subsection below applies to every change; where one doesn't, say so in a line rather than leaving it blank. -->

### Unit tests
<!-- The tests in this repository's build. Which did you add or change, what behavior does each one pin, and how does a reviewer run them (for most plugins, `./gradlew test --tests "..."`)? For a bugfix, does the new test fail without your change? -->

### REST integration tests
<!-- End-to-end coverage lives in [NrgXnat/xnat-rest-tests](https://github.com/NrgXnat/xnat-rest-tests), which exercises a running server over the REST API and covers core XNAT and several common plugins. If this change is observable through the API, link the companion PR there. If the suite already covers it, say which test. If it needs coverage you haven't written, say so and link the ticket. -->

### Manual verification
<!-- Your test plan, in enough detail that a reviewer could repeat it: the deployment you started from (the XNAT version and any other plugins installed) and its data, the steps you took, and what you observed at each one. Screenshots for anything with a UI. What did you deliberately try to break — the edge cases you named above, empty or malformed input, the large case, the concurrent case? And what did you exercise that you didn't change, to show you haven't regressed the paths around this one? Where automated coverage doesn't exist for what you changed, this section carries the proof. -->

### Gaps
<!-- If there's something a reviewer would expect you to have tested and you didn't, say so: a named gap is more useful than a blank section. Coverage you decided against is worth a line too, with the reason. -->

## Note for reviewers
<!-- Where to look first, what you're unsure about, what you deliberately left out of scope, decisions you'd like a second opinion on. -->
