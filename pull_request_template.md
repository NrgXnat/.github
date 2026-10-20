## Description
<!-- What changed and why, in your own words — the user-facing story and the technical one. Link the work: the ticket (e.g. "XNAT-1234"), "Closes #123" (auto-closes on merge, so only if this PR fully resolves it), "Related to #123", or the merge order if this is stacked on another PR. Detail meant to outlive this PR belongs in the code, the docs, or the ticket. If you used AI to help draft this, read it and edit it before you post. -->

## Release note
<!-- Write this yourself, for the people who install, administer, and use this software rather than for reviewers: it may be copied into the release notes as written. In a few sentences, say what changed from their point of view, who it affects, and anything they need to do about it, such as a configuration change or a step before or after upgrading. Call out any change to existing behavior, even a fix. If nothing is user-visible (a refactor, or a build-, CI-, or test-only change), write "None" so we know it wasn't skipped. -->

## Risks and impact
<!-- Every change carries some risk; this is where you name the risks you know about. Answer the sections that apply and delete the rest. How much attention each deserves is your call. -->

### PHI and de-identification
<!-- Does this touch anonymization or de-identification, or any path that reads, writes, logs, or exports imaging data or its metadata? Could an identifier survive a path that used to scrub it, or end up somewhere it shouldn't, like a log line, an error message, or a file outside the archive? -->

### Security, authentication, and authorization
<!-- Do your changes add or modify roles, or change what data a user can see or what actions they can take? Could a user edit a URL or request and reach data they aren't allowed to? Were you mindful of least privilege? See the [OWASP checklist](https://github.com/0xRadi/OWASP-Web-Checklist). -->

### Input data
<!-- Which edge cases did you consider? Empty, missing, oversized, and malformed input all show up in the wild. For DICOM, type 2 elements are required to be present but may be empty; private tags, multiframe objects, and non-conforming data from real scanners are common. On bad data, does this fail loudly or quietly? -->

### Upgrade and compatibility
<!-- Only a major release may break backward compatibility; if this PR does and its milestone isn't one, raise it with the maintainers before it merges. In XNAT versions the leading 1 never changes and the second number is the major version, so 1.11 and 1.12 are major releases and 1.10.x is not. Plugins and other libraries follow semantic versioning, where only a change to the first number is major. How do you know an existing installation can take this upgrade? Say what you checked in public APIs, REST endpoints, configuration, data formats and schemas, and dependencies, and whether code built against the previous release (plugins, scripts, client tools) still works. If something does break, name it and say who has to change. If there is a data or schema migration, how long does it run on a large site, and does the site need to be down for it? -->

### Performance and scale
<!-- At what scale do we expect this to run — data volume, study or session count, concurrent users or uploads? How have you verified that it holds up? -->

## Testing
<!-- Please don't delete this section. At a minimum, show proof that this change was deployed and executed successfully: a green build is not sufficient. Show the evidence — commands and their output, screenshots, before/after values, log lines, the data you threw at it — and reference the areas of impact above. A model writing a test is not the same as you confirming the behavior. Not every subsection below applies to every change; where one doesn't, say so in a line rather than leaving it blank. -->

### Automated tests
<!-- Which tests did you add or change, what behavior does each one pin, and how does a reviewer run them? For a bugfix, does the new test fail without your change? -->

### Integration tests
<!-- Tests that exercise the change against a running system. For XNAT and its plugins, end-to-end coverage lives in [NrgXnat/xnat-rest-tests](https://github.com/NrgXnat/xnat-rest-tests), which exercises a running server over the REST API. If this change is observable that way, link the companion PR or name the existing test that covers it. If it needs coverage you haven't written, say so and link the ticket. -->

### Manual verification
<!-- Your test plan, in enough detail that a reviewer could repeat it: the deployment and data you started from, the steps you took, and what you observed at each one. Screenshots for anything with a UI. What did you deliberately try to break — the edge cases you named above, empty or malformed input, the large case, the concurrent case? And what did you exercise that you didn't change, to show you haven't regressed the paths around this one? Where automated coverage doesn't exist for what you changed, this section carries the proof. -->

### Gaps
<!-- If there's something a reviewer would expect you to have tested and you didn't, say so: a named gap is more useful than a blank section. Coverage you decided against is worth a line too, with the reason. -->

## Note for reviewers
<!-- Where to look first, what you're unsure about, what you deliberately left out of scope, decisions you'd like a second opinion on. -->
