Release Process
===
## Working Schedule
|Date|Event|Description|
|----|-----|-----------|
|T-10 Days|PR Cutoff|Deadline for Pull Request submission. Non-urgent features completed after this date are postponed to next release. First internal build submitted to Testflight / Play Store.|
|T-9 Days|Internal Release|Internal build available for testing. Beginning of testing period.|
|T-5 Days|Feedback Cutoff|End of testing period. Non-fatal issues found after this date are postponed to next release.|
|T-3 Days|Production Build|Production build submitted to App Store / Play Store.|
|T+0 Day|Production Release|Production build released to public.|

Release day is preferred to be Wed.

## Release PIC
One PIC should be chosen for each platform, who will oversee and facilitate the working process of that release.

### Tasks
- Plan and negotiate target release date with feature PICs
- Announce working schedule on #developers
- Notify QA on expected changes and testing schedule
- Handle build submission / releasing (+ tagging commit for each released build)
- Announce releases with changelog on #general
- Bump version number on master after production release
