# 30094

## Current behavior

Renovate tries to pin `.python-version` which is not working, since there is no pinning for this file.

See `WARN: Error updating branch: update failure (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)` in logs.

This also results in an error message in the dependency dashboard if enabled (not enabled here, because not needed for reproduction in this case).

<details>

```
DEBUG: 3 flattened updates found: renovatebot/github-action, python, python (repository=Rojax/renovate-pin-issue)
DEBUG: Returning 3 branch(es) (repository=Rojax/renovate-pin-issue)
DEBUG: config.repoIsOnboarded=true (repository=Rojax/renovate-pin-issue)
DEBUG: packageFiles with updates (repository=Rojax/renovate-pin-issue, baseBranch=main)
       "config": {
         "github-actions": [
           {
             "deps": [
               {
                 "depName": "actions/checkout",
                 "commitMessageTopic": "{{{depName}}} action",
                 "datasource": "github-tags",
                 "versioning": "docker",
                 "depType": "action",
                 "replaceString": "actions/checkout@692973e3d937129bcbf40652eb9f2f61becf3332 # v4.1.7",
                 "autoReplaceStringTemplate": "{{depName}}@{{#if newDigest}}{{newDigest}}{{#if newValue}} # {{newValue}}{{/if}}{{/if}}{{#unless newDigest}}{{newValue}}{{/unless}}",
                 "currentValue": "v4.1.7",
                 "currentDigest": "692973e3d937129bcbf40652eb9f2f61becf3332",
                 "updates": [],
                 "packageName": "actions/checkout",
                 "warnings": [],
                 "sourceUrl": "https://github.com/actions/checkout",
                 "registryUrl": "https://github.com",
                 "currentVersion": "v4.1.7",
                 "currentVersionTimestamp": "2024-06-12T18:41:43.000Z",
                 "fixedVersion": "v4.1.7"
               },
               {
                 "depName": "actions/setup-node",
                 "commitMessageTopic": "{{{depName}}} action",
                 "datasource": "github-tags",
                 "versioning": "docker",
                 "depType": "action",
                 "replaceString": "actions/setup-node@60edb5dd545a775178f52524783378180af0d1f8 # v4.0.2",
                 "autoReplaceStringTemplate": "{{depName}}@{{#if newDigest}}{{newDigest}}{{#if newValue}} # {{newValue}}{{/if}}{{/if}}{{#unless newDigest}}{{newValue}}{{/unless}}",
                 "currentValue": "v4.0.2",
                 "currentDigest": "60edb5dd545a775178f52524783378180af0d1f8",
                 "updates": [],
                 "packageName": "actions/setup-node",
                 "warnings": [],
                 "sourceUrl": "https://github.com/actions/setup-node",
                 "registryUrl": "https://github.com",
                 "currentVersion": "v4.0.2",
                 "currentVersionTimestamp": "2024-02-07T04:42:16.000Z",
                 "fixedVersion": "v4.0.2"
               },
               {
                 "depName": "renovatebot/github-action",
                 "commitMessageTopic": "{{{depName}}} action",
                 "datasource": "github-tags",
                 "versioning": "docker",
                 "depType": "action",
                 "replaceString": "renovatebot/github-action@259200be4d976a76196ec8985b0dddcaf1733b47 # v40.2.0",
                 "autoReplaceStringTemplate": "{{depName}}@{{#if newDigest}}{{newDigest}}{{#if newValue}} # {{newValue}}{{/if}}{{/if}}{{#unless newDigest}}{{newValue}}{{/unless}}",
                 "currentValue": "v40.2.0",
                 "currentDigest": "259200be4d976a76196ec8985b0dddcaf1733b47",
                 "updates": [
                   {
                     "bucket": "non-major",
                     "newVersion": "v40.2.2",
                     "newValue": "v40.2.2",
                     "newDigest": "042670e39b8d7335e992c3fa526ecbfbd52ef57b",
                     "releaseTimestamp": "2024-07-08T22:04:48.000Z",
                     "newMajor": 40,
                     "newMinor": 2,
                     "newPatch": 2,
                     "updateType": "patch",
                     "branchName": "renovate/renovatebot-github-action-40.x"
                   }
                 ],
                 "packageName": "renovatebot/github-action",
                 "warnings": [],
                 "sourceUrl": "https://github.com/renovatebot/github-action",
                 "registryUrl": "https://github.com",
                 "currentVersion": "v40.2.0",
                 "currentVersionTimestamp": "2024-07-02T11:21:40.000Z",
                 "isSingleVersion": true,
                 "fixedVersion": "v40.2.0"
               },
               {
                 "depName": "ubuntu",
                 "currentValue": "latest",
                 "replaceString": "ubuntu-latest",
                 "depType": "github-runner",
                 "datasource": "github-runners",
                 "autoReplaceStringTemplate": "{{depName}}-{{newValue}}",
                 "skipReason": "invalid-version",
                 "updates": [],
                 "packageName": "ubuntu"
               }
             ],
             "packageFile": ".github/workflows/renovate.yml"
           }
         ],
         "pyenv": [
           {
             "deps": [
               {
                 "depName": "python",
                 "commitMessageTopic": "Python",
                 "currentValue": "3.12.2",
                 "datasource": "docker",
                 "updates": [
                   {
                     "bucket": "non-major",
                     "newVersion": "3.12.4",
                     "newValue": "3.12.4",
                     "newMajor": 3,
                     "newMinor": 12,
                     "newPatch": 4,
                     "updateType": "patch",
                     "newDigest": "sha256:d12b529fba98bcc93e2e2e837c0a60efaa6328775965a43c1b8161cfbd8f10f3",
                     "branchName": "renovate/python-3.x"
                   },
                   {
                     "isPinDigest": true,
                     "updateType": "pinDigest",
                     "newValue": "3.12.2",
                     "newDigest": "sha256:19973e1796237522ed1fcc1357c766770b47dc15854eafdda055b65953fe5ec1",
                     "branchName": "renovate/pin-dependencies"
                   }
                 ],
                 "packageName": "python",
                 "versioning": "docker",
                 "warnings": [],
                 "registryUrl": "https://index.docker.io",
                 "lookupName": "library/python",
                 "currentVersion": "3.12.2",
                 "isSingleVersion": true,
                 "fixedVersion": "3.12.2"
               }
             ],
             "packageFile": ".python-version"
           }
         ]
       }
DEBUG: detectSemanticCommits() (repository=Rojax/renovate-pin-issue)
DEBUG: semanticCommits: returning "enabled" from cache (repository=Rojax/renovate-pin-issue)
DEBUG: processRepo() (repository=Rojax/renovate-pin-issue)
DEBUG: Processing 3 branches: renovate/pin-dependencies, renovate/python-3.x, renovate/renovatebot-github-action-40.x (repository=Rojax/renovate-pin-issue)
DEBUG: Calculating hourly PRs remaining (repository=Rojax/renovate-pin-issue)
DEBUG: currentHourStart=2024-07-09T11:00:00.000+00:00 (repository=Rojax/renovate-pin-issue)
DEBUG: PR hourly limit remaining: 1 (repository=Rojax/renovate-pin-issue)
DEBUG: Calculating prConcurrentLimit (10) (repository=Rojax/renovate-pin-issue)
DEBUG: getBranchPr(renovate/pin-dependencies) (repository=Rojax/renovate-pin-issue)
DEBUG: findPr(renovate/pin-dependencies, undefined, open) (repository=Rojax/renovate-pin-issue)
DEBUG: findPr(renovate/pin-dependencies, undefined, closed) (repository=Rojax/renovate-pin-issue)
DEBUG: getBranchPr(renovate/python-3.x) (repository=Rojax/renovate-pin-issue)
DEBUG: findPr(renovate/python-3.x, undefined, open) (repository=Rojax/renovate-pin-issue)
DEBUG: Found PR #3 (repository=Rojax/renovate-pin-issue)
DEBUG: getBranchPr(renovate/renovatebot-github-action-40.x) (repository=Rojax/renovate-pin-issue)
DEBUG: findPr(renovate/renovatebot-github-action-40.x, undefined, open) (repository=Rojax/renovate-pin-issue)
DEBUG: findPr(renovate/renovatebot-github-action-40.x, undefined, closed) (repository=Rojax/renovate-pin-issue)
DEBUG: 1 PRs are currently open (repository=Rojax/renovate-pin-issue)
DEBUG: PR concurrent limit remaining: 9 (repository=Rojax/renovate-pin-issue)
DEBUG: Calculated maximum PRs remaining this run: 1 (repository=Rojax/renovate-pin-issue)
DEBUG: PullRequests limit = 1 (repository=Rojax/renovate-pin-issue)
DEBUG: Calculating hourly PRs remaining (repository=Rojax/renovate-pin-issue)
DEBUG: currentHourStart=2024-07-09T11:00:00.000+00:00 (repository=Rojax/renovate-pin-issue)
DEBUG: PR hourly limit remaining: 1 (repository=Rojax/renovate-pin-issue)
DEBUG: Calculating branchConcurrentLimit (10) (repository=Rojax/renovate-pin-issue)
DEBUG: 1 already existing branches found: renovate/python-3.x (repository=Rojax/renovate-pin-issue)
DEBUG: Branch concurrent limit remaining: 9 (repository=Rojax/renovate-pin-issue)
DEBUG: Calculated maximum branches remaining this run: 1 (repository=Rojax/renovate-pin-issue)
DEBUG: Branches limit = 1 (repository=Rojax/renovate-pin-issue)
DEBUG: syncBranchState() (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: getBranchPr(renovate/pin-dependencies) (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: findPr(renovate/pin-dependencies, undefined, open) (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: findPr(renovate/pin-dependencies, undefined, closed) (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: branchExists=false (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: dependencyDashboardCheck=undefined (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Check for closed PR because recreating closed PRs is disabled. (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: findPr(renovate/pin-dependencies, chore(deps): pin python docker tag to 19973e1, !open) (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: prAlreadyExisted=false (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Checking schedule(schedule=at any time, tz=null, now=2024-07-09T11:50:28.579Z) (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: No schedule defined (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Branch needs creating (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Using reuseExistingBranch: false (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Setting current branch to main (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: latest commit (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
       "branchName": "main",
       "latestCommitDate": "2024-07-09T13:49:34+02:00"
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: Starting search at index 0 (repository=Rojax/renovate-pin-issue, packageFile=.python-version, branch=renovate/pin-dependencies)
       "depName": "python"
DEBUG: Found match at index 0 (repository=Rojax/renovate-pin-issue, packageFile=.python-version, branch=renovate/pin-dependencies)
       "depName": "python"
DEBUG: Digest is not updated (repository=Rojax/renovate-pin-issue, packageFile=.python-version, branch=renovate/pin-dependencies)
       "manager": "pyenv",
       "expectedValue": "sha256:19973e1796237522ed1fcc1357c766770b47dc15854eafdda055b65953fe5ec1",
       "foundValue": undefined
 WARN: Error updating branch: update failure (repository=Rojax/renovate-pin-issue, branch=renovate/pin-dependencies)
DEBUG: syncBranchState() (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: getBranchPr(renovate/python-3.x) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: findPr(renovate/python-3.x, undefined, open) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Found PR #3 (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: branchExists=true (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: dependencyDashboardCheck=undefined (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: PR rebase requested=false (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Checking if PR has been edited (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: branch.isModified(): using git to calculate (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: branch.isModified() = false (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Found existing branch PR (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Checking schedule(schedule=at any time, tz=null, now=2024-07-09T11:50:28.638Z) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No schedule defined (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Branch already exists (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: GET https://api.github.com/repos/Rojax/renovate-pin-issue/branches/main/protection = (code=ERR_NON_2XX_3XX_RESPONSE, statusCode=404 retryCount=0, duration=98) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No branch protection found for main (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Skipping behind base branch check due to rebaseWhen=auto (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: isBranchConflicted(main, renovate/python-3.x) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: branch.isConflicted(): using git to calculate (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Setting git author name: Renovate Bot (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Setting git author email: renovate@whitesourcesoftware.com (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: branch.isConflicted(): false (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Branch does not need rebasing (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Using reuseExistingBranch: true (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Setting current branch to main (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: latest commit (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
       "branchName": "main",
       "latestCommitDate": "2024-07-09T13:49:34+02:00"
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=true (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Branch dep python in .python-version is already updated (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No content changed (repository=Rojax/renovate-pin-issue, packageFile=.python-version, branch=renovate/python-3.x)
       "depName": "python"
DEBUG: No package files need updating (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No updated lock files in branch (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No changes to package files, skipping post-upgrade tasks (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: No files to commit (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Setting current branch to main (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: latest commit (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
       "branchName": "main",
       "latestCommitDate": "2024-07-09T13:49:34+02:00"
DEBUG: Checking if we can automerge branch (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: mergeStatus=no automerge (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Ensuring PR (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: There are 0 errors and 0 warnings (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: getBranchPr(renovate/python-3.x) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: findPr(renovate/python-3.x, undefined, open) (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Found PR #3 (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: getPrCache() (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Found existing PR (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Processing existing PR (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: setPrCache() (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: Pull Request #3 does not need updating (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
DEBUG: PR is not configured for automerge (repository=Rojax/renovate-pin-issue, branch=renovate/python-3.x)
```

</details>

## Expected behavior

Renovate should not try to pin versions in `.python-version` files.

## Link to the Renovate issue or Discussion

<https://github.com/renovatebot/renovate/discussions/30094>
