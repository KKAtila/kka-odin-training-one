# Author Commit Audit Report

## Audit Parameters

* Root directory: `/Users/brianjhurst/Code`
* Repository list file: `/Users/brianjhurst/Code/REPOS.md`
* Target author: `Andrew Burnes\|andrew\.burnes\|apburnes`
* Date range: All time
* Scan date: 2026-06-24
* Number of repositories listed: 23
* Number of repositories scanned: 23

## Executive Summary

* Total repositories listed in `REPOS.md`: 23
* Total repositories successfully scanned: 23
* Repositories with matching commits: 21
* Total matching commits: 1366
* Suspicious commits found: 52
* Highest severity finding: High
* Most affected repositories: `pages-core` (29 findings), `pages-editor` (13 findings), `pages-images` (8 findings), `pages-cf-build-tasks` (5 findings), `pages-build-container` (3 findings)

This audit found review-worthy indicators, but no commit is labeled malicious solely from these automated checks. Findings are evidence-based pattern matches from commit diffs and should be reviewed in repository context.

## Global Commit Summary

| Repository | Matching Commits | First Commit | Latest Commit | Files Changed | Insertions | Deletions | Suspicious Commits |
|---|---:|---:|---:|---:|---:|---:|---:|
| `pages-core` | 589 | 2019-03-20 | 2026-06-18 | 6341 | 378739 | 255761 | 23 |
| `pages-bot` | 29 | 2024-06-26 | 2026-03-17 | 100 | 2607 | 607 | 1 |
| `pages-editor` | 164 | 2025-04-23 | 2026-06-16 | 1537 | 1804094 | 101457 | 12 |
| `eleventy-preset` | 1 | 2026-06-17 | 2026-06-17 | 4 | 901 | 1136 | 0 |
| `docs` | 4 | 2026-04-14 | 2026-05-21 | 52 | 28 | 28 | 0 |
| `pages-example-spa` | 3 | 2025-10-02 | 2026-06-10 | 4 | 18 | 14 | 0 |
| `pages-example-website-api` | 2 | 2025-10-02 | 2025-10-02 | 2 | 2 | 0 | 0 |
| `pages-example-api-website` | 2 | 2025-10-02 | 2025-10-02 | 2 | 2 | 0 | 0 |
| `pages-proxy` | 113 | 2019-04-23 | 2026-06-03 | 346 | 15001 | 5117 | 0 |
| `pages-cf-build-tasks` | 35 | 2024-05-22 | 2026-06-03 | 121 | 1612 | 5157 | 4 |
| `pages-build-container` | 99 | 2019-05-10 | 2026-06-03 | 211 | 3185 | 3026 | 2 |
| `pages-site-gantry` | 66 | 2025-05-23 | 2026-06-03 | 762 | 39149 | 24265 | 3 |
| `pages-pipeline-tasks` | 29 | 2024-06-24 | 2026-03-17 | 53 | 538 | 71 | 0 |
| `pages-gpg-keys` | 12 | 2023-04-18 | 2026-03-17 | 12 | 84 | 32 | 0 |
| `pages-studio-crawler` | 0 | - | - | 0 | 0 | 0 | 0 |
| `pages-redirects` | 105 | 2021-01-27 | 2026-03-17 | 290 | 9796 | 8676 | 1 |
| `pages-mailer` | 34 | 2021-11-22 | 2026-03-17 | 63 | 22736 | 28283 | 0 |
| `pages-example-staff-dir` | 2 | 2025-10-02 | 2025-10-02 | 2 | 2 | 0 | 0 |
| `pages-uswds-11ty` | 54 | 2022-03-18 | 2026-05-20 | 279 | 89276 | 42897 | 2 |
| `dsd` | 0 | - | - | 0 | 0 | 0 | 0 |
| `pages-images` | 20 | 2023-12-20 | 2026-03-17 | 52 | 2635 | 31 | 4 |
| `pages-research-spider` | 1 | 2026-03-17 | 2026-03-17 | 1 | 0 | 8 | 0 |
| `pages-404-page` | 2 | 2025-10-02 | 2025-10-02 | 2 | 2 | 0 | 0 |

## Suspicious Findings

| Severity | Confidence | Repository | Commit | Date | Category | Summary | Recommended Review |
|---|---|---|---|---:|---|---|---|
| High | High | `pages-core` | `44c9ef71c68b` | 2021-03-09 | credential exposure | Add local uaa for development and clean up uaa user verification | `git -C pages-core show 44c9ef71c68bf1cd65266ae6aca96c99fc583b30` |
| High | Medium | `pages-build-container` | `c761a8e5eaa6` | 2026-01-05 | CI/CD risk | feat: Add Node.js v24 as the default node version | `git -C pages-build-container show c761a8e5eaa635bdb9ff08c0206f4a500e8d67e8` |
| Medium | Medium | `pages-bot` | `6cf1293629a2` | 2024-06-26 | auth weakening | Initial Commit | `git -C pages-bot show 6cf1293629a2f15a7c7808bace8a57e3aff5f204` |
| Medium | Medium | `pages-cf-build-tasks` | `c94c42f12e6a` | 2026-04-16 | suspicious system execution | test: Different chromium install type | `git -C pages-cf-build-tasks show c94c42f12e6a87345b3f426e65eb8f640f49d79e` |
| Medium | Medium | `pages-core` | `87fdbd0fd1d8` | 2019-03-22 | credential exposure | Add authentication and api client for Cloud Foundry | `git -C pages-core show 87fdbd0fd1d8790912a46093901f718bbb7ec6c2` |
| Medium | Medium | `pages-core` | `26137c7edce6` | 2019-03-27 | credential exposure | Update SQS client to query CF API for site bucket credentials | `git -C pages-core show 26137c7edce684218d8986d9080fde22ed443b8d` |
| Medium | Medium | `pages-core` | `f4c63e608201` | 2019-04-15 | credential exposure | Merge branch 'staging' into apburnes/query-cf-bucket | `git -C pages-core show f4c63e60820144b45e23dea0c7e251fa39bb1214` |
| Medium | Medium | `pages-core` | `a692106326fd` | 2021-03-05 | credential exposure | Add uaa_identity table to support auth | `git -C pages-core show a692106326fdc240c3968d9512fec6688b9ada24` |
| Medium | Medium | `pages-core` | `44c9ef71c68b` | 2021-03-09 | credential exposure | Add local uaa for development and clean up uaa user verification | `git -C pages-core show 44c9ef71c68bf1cd65266ae6aca96c99fc583b30` |
| Medium | Medium | `pages-core` | `d58e4e79b247` | 2021-04-16 | credential exposure | Update org element views with hasOrgs and add org select validation | `git -C pages-core show d58e4e79b2473ee9bf3d8052d612631ab9ef101c` |
| Medium | Medium | `pages-core` | `727308031af6` | 2021-05-26 | credential exposure | Merge with staging | `git -C pages-core show 727308031af632b34e624517a8f7903e20e377fe` |
| Medium | Medium | `pages-core` | `16518fbe271f` | 2022-12-19 | credential exposure | Add additional event logging around authentication | `git -C pages-core show 16518fbe271f0ecf570decbb3e3a991decb2f745` |
| Medium | Medium | `pages-core` | `8032a3be43b9` | 2023-06-09 | credential exposure | feat: Restructure site model with site branch config relation | `git -C pages-core show 8032a3be43b9cc675ddcb4392a9bd3285c4d6c9d` |
| Medium | Medium | `pages-core` | `7417e38b5437` | 2023-07-31 | credential exposure | feat: Added site custom domains page \| Updated domain model and admin \| #4199 | `git -C pages-core show 7417e38b5437c7e53ee76cf19df5ca2adc267cc6` |
| Medium | Medium | `pages-core` | `5293be4a3e62` | 2024-01-10 | auth weakening | fix(ci): Run db migrations in CI task container with SSL #4354 | `git -C pages-core show 5293be4a3e622f8a961ebe45bbad5c33564eeae1` |
| Medium | Medium | `pages-core` | `c0290556a068` | 2024-06-13 | credential exposure | fix: Only encrypt site build param values based on defined keys | `git -C pages-core show c0290556a0680077280a5cccdcc8a5b0701c2802` |
| Medium | Medium | `pages-core` | `b3116474b0db` | 2024-10-29 | credential exposure | chore: Run prettier formatting on codebase | `git -C pages-core show b3116474b0db1e2cbd7dea2f4652866d9c77e6ba` |
| Medium | Medium | `pages-core` | `d106f75851ac` | 2024-11-14 | credential exposure | fix: Site build polling and latest build branch | `git -C pages-core show d106f75851ac9a034dc7bc82792ae94f00e5e23c` |
| Medium | Medium | `pages-core` | `242d8e7343e5` | 2025-04-17 | credential exposure | feat: Add webhook to create an editor site | `git -C pages-core show 242d8e7343e5119847c41570a4f76405f5dbd2ac` |
| Medium | Medium | `pages-core` | `fed05f015e78` | 2025-04-25 | credential exposure | feat: Add webhook to create editor site builds | `git -C pages-core show fed05f015e78261edc3cab5a2761d3cf630346a2` |
| Medium | Medium | `pages-core` | `69718e6e4892` | 2026-06-09 | credential exposure | fix(admin): Correct the asset paths for nested routes | `git -C pages-core show 69718e6e4892cac861404f8b4b3987b4380e0c7b` |
| Medium | Medium | `pages-core` | `a84817fd0643` | 2026-06-17 | suspicious system execution | chore: Remove build status notifications and dependencies | `git -C pages-core show a84817fd0643a1e8158f7ef42c5c2197b07521ef` |
| Medium | Medium | `pages-editor` | `e9da62437a87` | 2025-10-29 | credential exposure | chore: Unify live preview for collections based on site slug | `git -C pages-editor show e9da62437a87c96391d4458a515e76ce18322b56` |
| Medium | Medium | `pages-editor` | `cee20b65d7f3` | 2026-05-21 | credential exposure | feat: Add theme group to site identity config | `git -C pages-editor show cee20b65d7f3e4b04673e27764d3f3409a5af6b8` |
| Medium | Medium | `pages-editor` | `d5bdd7d92b7d` | 2026-06-08 | suspicious system execution | feat: Add forms collection to allow users to create forms for sites | `git -C pages-editor show d5bdd7d92b7d0dd44c4d55532d23fee593abc7b4` |
| Medium | Medium | `pages-site-gantry` | `82d44a09013f` | 2025-07-23 | credential exposure | feat: Add reports pages | `git -C pages-site-gantry show 82d44a09013fd87e02cac9e80ae6be08dbc5ec60` |
| Medium | Low | `pages-build-container` | `cfd669ddfbb7` | 2024-09-11 | exfiltration | test without hardening | `git -C pages-build-container show cfd669ddfbb74f0382315b1f572964ede887bcae` |
| Medium | Low | `pages-build-container` | `c761a8e5eaa6` | 2026-01-05 | exfiltration | feat: Add Node.js v24 as the default node version | `git -C pages-build-container show c761a8e5eaa635bdb9ff08c0206f4a500e8d67e8` |
| Medium | Low | `pages-cf-build-tasks` | `96805ff8a53d` | 2025-09-17 | exfiltration | chore: Update reporter npm dependencies for Q4 FY25 | `git -C pages-cf-build-tasks show 96805ff8a53d15cff998e637edf4fe7ca6a0d7d5` |
| Medium | Low | `pages-cf-build-tasks` | `e2eee66cfe39` | 2026-06-01 | exfiltration | chore: Explicitly install chrome driver version for a11y tasks | `git -C pages-cf-build-tasks show e2eee66cfe395f6469da37af269a86a58d952aa2` |
| Medium | Low | `pages-core` | `44c9ef71c68b` | 2021-03-09 | exfiltration | Add local uaa for development and clean up uaa user verification | `git -C pages-core show 44c9ef71c68bf1cd65266ae6aca96c99fc583b30` |
| Medium | Low | `pages-core` | `242d8e7343e5` | 2025-04-17 | exfiltration | feat: Add webhook to create an editor site | `git -C pages-core show 242d8e7343e5119847c41570a4f76405f5dbd2ac` |
| Medium | Low | `pages-core` | `fed05f015e78` | 2025-04-25 | exfiltration | feat: Add webhook to create editor site builds | `git -C pages-core show fed05f015e78261edc3cab5a2761d3cf630346a2` |
| Medium | Low | `pages-core` | `9ec7aa01f741` | 2025-12-05 | exfiltration | feat: Add site delete webhook for publisher site | `git -C pages-core show 9ec7aa01f74182f141be959dbc91267fc1697355` |
| Medium | Low | `pages-editor` | `b04e24afca56` | 2025-04-23 | exfiltration | fix: Create site Pages webhook endpoint path | `git -C pages-editor show b04e24afca567fca1e5a8a4c8e7e55208bb892e7` |
| Medium | Low | `pages-editor` | `032619726583` | 2025-05-15 | exfiltration | feat: Add Media collection type | `git -C pages-editor show 0326197265839429632ab60e822960689efe60ef` |
| Medium | Low | `pages-editor` | `3cc63456d934` | 2025-08-12 | exfiltration | feat: Add S3 site media sync to site Pages bucket | `git -C pages-editor show 3cc63456d93479e66d3312434fbb47250af25dd0` |
| Medium | Low | `pages-editor` | `93cc0e67d99f` | 2025-12-05 | exfiltration | feat: Add afterDelete hook for site to call delete webhook to Pages core | `git -C pages-editor show 93cc0e67d99f0a2dd0f456d88d039dda304ae5ee` |
| Medium | Low | `pages-editor` | `23d848d98dfc` | 2026-03-12 | exfiltration | feat: Add build site hook on record unpublish or delete | `git -C pages-editor show 23d848d98dfcb8c263ec5094140f62b2b11f29a7` |
| Medium | Low | `pages-images` | `cb2b81af472c` | 2024-01-30 | exfiltration | feat: Create images for dind and node | `git -C pages-images show cb2b81af472ce8741fb4056e0959421506060f6b` |
| Medium | Low | `pages-images` | `0a8a1d11e5c8` | 2024-02-07 | exfiltration | feat: Add Python base image | `git -C pages-images show 0a8a1d11e5c857c1a78afa5668585e60cb0e5bb2` |
| Medium | Low | `pages-images` | `9bc49ef3aba8` | 2025-10-08 | exfiltration | feat: Add Nodejs v22 | `git -C pages-images show 9bc49ef3aba87db6e5387370c523e8a8c79b59d1` |
| Medium | Low | `pages-images` | `45546ef83371` | 2026-01-12 | exfiltration | feat: Add nodejs v24 and update to latest for node v20 and v22 | `git -C pages-images show 45546ef8337127c08ddb9e955cc2e3dac6e1eded` |
| Medium | Low | `pages-redirects` | `d45c3a112959` | 2022-09-30 | exfiltration | chore: Update circleci docker-compose version | `git -C pages-redirects show d45c3a1129591e1f779205051f54cd8b21e1be93` |
| Low | Medium | `pages-cf-build-tasks` | `96805ff8a53d` | 2025-09-17 | credential exposure | chore: Update reporter npm dependencies for Q4 FY25 | `git -C pages-cf-build-tasks show 96805ff8a53d15cff998e637edf4fe7ca6a0d7d5` |
| Low | Medium | `pages-cf-build-tasks` | `e0dc5861167f` | 2025-09-18 | credential exposure | Merge pull request #85 from cloud-gov/chore-update-report-deps-q4fy25 | `git -C pages-cf-build-tasks show e0dc5861167f5c2e6fe54f4ed07803ae688dca59` |
| Low | Medium | `pages-core` | `9b31afcdbaba` | 2026-05-20 | credential exposure | Merge pull request #4911 from cloud-gov/chore-Update-core-to-use-NPM-install-with-improved-security-config-2949 | `git -C pages-core show 9b31afcdbaba0f7a7be3081fd755598026f3658a` |
| Low | Medium | `pages-editor` | `8e55be9080fb` | 2026-06-01 | credential exposure | Merge pull request #308 from cloud-gov/feat-add-theme-to-site-config | `git -C pages-editor show 8e55be9080fb320dbae79a9eab6444b4eb0aa5cf` |
| Low | Medium | `pages-editor` | `a04e86640799` | 2026-06-01 | credential exposure | chore: Update to Nodejs v24 with NPM v11.10 | `git -C pages-editor show a04e866407990815190b5b8f8f6c1e304a972c36` |
| Low | Medium | `pages-site-gantry` | `9060d63a6219` | 2026-05-26 | credential exposure | chore: Refactor site theming styles config | `git -C pages-site-gantry show 9060d63a6219186ee1482837bbdd884519ddaf88` |
| Low | Medium | `pages-site-gantry` | `4738bcbb39d9` | 2026-06-01 | credential exposure | Merge pull request #230 from cloud-gov/chore-refactor-site-theming-styles | `git -C pages-site-gantry show 4738bcbb39d9dc0b9838c1d74192139e1fad8b4e` |
| Low | Medium | `pages-uswds-11ty` | `89a6e8c5bfba` | 2026-05-20 | credential exposure | chore: Update to Node v24 and add npmrc rules | `git -C pages-uswds-11ty show 89a6e8c5bfbaa3b0e8fc14ef4867a4f9abea087a` |
| Low | Medium | `pages-uswds-11ty` | `96294a4ab790` | 2026-05-20 | credential exposure | Merge pull request #107 from cloud-gov/chore-update-node-version-and-tighten-npmrc | `git -C pages-uswds-11ty show 96294a4ab790c7a1ad11d9bea119541b63c8cf24` |
| Low | Low | `pages-core` | `87fdbd0fd1d8` | 2019-03-22 | obfuscation | Add authentication and api client for Cloud Foundry | `git -C pages-core show 87fdbd0fd1d8790912a46093901f718bbb7ec6c2` |
| Low | Low | `pages-core` | `1eeebf96cffa` | 2020-09-17 | suspicious system execution | Refactor site delete into SiteDestroyer service | `git -C pages-core show 1eeebf96cffa9deadeeac2d1739ffc74041041dc` |
| Low | Low | `pages-core` | `b3116474b0db` | 2024-10-29 | obfuscation | chore: Run prettier formatting on codebase | `git -C pages-core show b3116474b0db1e2cbd7dea2f4652866d9c77e6ba` |
| Low | Low | `pages-core` | `9aeb74821a54` | 2026-06-03 | suspicious system execution | chore(admin): Vendor page router to allow for dependency updates | `git -C pages-core show 9aeb74821a543d0f04a0587c6b53c89f004a3438` |
| Low | Low | `pages-core` | `c91bdd43d919` | 2026-06-03 | suspicious system execution | chore: Upgrade admin client to svelte v5 | `git -C pages-core show c91bdd43d919b8f95e9c5e3682dea6aab68a4d9b` |
| Low | Low | `pages-editor` | `032619726583` | 2025-05-15 | suspicious system execution | feat: Add Media collection type | `git -C pages-editor show 0326197265839429632ab60e822960689efe60ef` |
| Low | Low | `pages-editor` | `311c843a85d4` | 2026-04-29 | obfuscation | feat: Add nince to CSP headers | `git -C pages-editor show 311c843a85d40047adf8ff9955592ef6aa55c1e6` |
| Low | Low | `pages-editor` | `9e76ce4e1748` | 2026-06-11 | suspicious system execution | feat: Add feature flag to gate forms in env | `git -C pages-editor show 9e76ce4e17480b90f1497e394e9da0fbe7b42fd5` |
| Low | Low | `pages-images` | `cb2b81af472c` | 2024-01-30 | security tooling disabled | feat: Create images for dind and node | `git -C pages-images show cb2b81af472ce8741fb4056e0959421506060f6b` |
| Low | Low | `pages-images` | `0a8a1d11e5c8` | 2024-02-07 | security tooling disabled | feat: Add Python base image | `git -C pages-images show 0a8a1d11e5c857c1a78afa5668585e60cb0e5bb2` |
| Low | Low | `pages-images` | `9bc49ef3aba8` | 2025-10-08 | security tooling disabled | feat: Add Nodejs v22 | `git -C pages-images show 9bc49ef3aba87db6e5387370c523e8a8c79b59d1` |
| Low | Low | `pages-images` | `45546ef83371` | 2026-01-12 | security tooling disabled | feat: Add nodejs v24 and update to latest for node v20 and v22 | `git -C pages-images show 45546ef8337127c08ddb9e955cc2e3dac6e1eded` |

### `pages-core` `44c9ef71c68b`

* Repository: `pages-core`
* Commit SHA: `44c9ef71c68bf1cd65266ae6aca96c99fc583b30`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2021-03-09
* Files changed: `Dockerfile-uaa`, `config/local.sample.js`, `uaa/uaa.yml`
* Why it is suspicious: credential exposure (High/High), credential exposure (Medium/Medium), exfiltration (Medium/Low)
* Evidence from the diff:
  * `uaa/uaa.yml: +    -----BEGIN [REDACTED PRIVATE KEY]-----`
  * `config/local.sample.js: +          clientSecret: '[REDACTED]',`
  * `Dockerfile-uaa: +RUN wget -q https://archive.apache.org/dist/tomcat/tomcat-8/v8.0.28/bin/apache-tomcat-8.0.28.tar.gz`
  * `Dockerfile-uaa: +RUN wget -qO- https://archive.apache.org/dist/tomcat/tomcat-8/v8.0.28/bin/apache-tomcat-8.0.28.tar.gz.md5 \| md5sum -c -`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 44c9ef71c68bf1cd65266ae6aca96c99fc583b30` and verify the change is expected.

### `pages-build-container` `c761a8e5eaa6`

* Repository: `pages-build-container`
* Commit SHA: `c761a8e5eaa635bdb9ff08c0206f4a500e8d67e8`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-01-05
* Files changed: `Dockerfile`, `Dockerfile-exp`
* Why it is suspicious: CI/CD risk (High/Medium), exfiltration (Medium/Low)
* Evidence from the diff:
  * `Dockerfile: +RUN curl https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh \| bash \`
  * `Dockerfile-exp: +RUN curl https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh \| bash \`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-build-container show c761a8e5eaa635bdb9ff08c0206f4a500e8d67e8` and verify the change is expected.

### `pages-bot` `6cf1293629a2`

* Repository: `pages-bot`
* Commit SHA: `6cf1293629a2f15a7c7808bace8a57e3aff5f204`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-06-26
* Files changed: `src/db/client.js`
* Why it is suspicious: auth weakening (Medium/Medium)
* Evidence from the diff:
  * `src/db/client.js: +        rejectUnauthorized: false,`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-bot show 6cf1293629a2f15a7c7808bace8a57e3aff5f204` and verify the change is expected.

### `pages-cf-build-tasks` `c94c42f12e6a`

* Repository: `pages-cf-build-tasks`
* Commit SHA: `c94c42f12e6a87345b3f426e65eb8f640f49d79e`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-04-16
* Files changed: `tasks/a11y/definition.py`
* Why it is suspicious: suspicious system execution (Medium/Medium)
* Evidence from the diff:
  * `tasks/a11y/definition.py: +                subprocess.run(['pkill', '-f', 'chromedriver'])`
  * `tasks/a11y/definition.py: +                subprocess.run(['pkill', '-f', 'chrome'])`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-cf-build-tasks show c94c42f12e6a87345b3f426e65eb8f640f49d79e` and verify the change is expected.

### `pages-core` `87fdbd0fd1d8`

* Repository: `pages-core`
* Commit SHA: `87fdbd0fd1d8790912a46093901f718bbb7ec6c2`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2019-03-22
* Files changed: `test/api/bootstrap.test.js`, `test/api/support/cfAuthNock.js`
* Why it is suspicious: credential exposure (Medium/Medium), obfuscation (Low/Low)
* Evidence from the diff:
  * `test/api/bootstrap.test.js: +process.env.DEPLOY_USER_PASSWORD = '[REDACTED]';`
  * `test/api/support/cfAuthNock.js: +    password: '[REDACTED]',`
  * `test/api/support/cfAuthNock.js: +      authorization: `Basic ${Buffer.from('cf:').toString('Base64')}`,`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 87fdbd0fd1d8790912a46093901f718bbb7ec6c2` and verify the change is expected.

### `pages-core` `26137c7edce6`

* Repository: `pages-core`
* Commit SHA: `26137c7edce684218d8986d9080fde22ed443b8d`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2019-03-27
* Files changed: `config/env/test.js`, `test/api/support/cfAuthNock.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `config/env/test.js: +    password: '[REDACTED]',`
  * `test/api/support/cfAuthNock.js: +      password: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 26137c7edce684218d8986d9080fde22ed443b8d` and verify the change is expected.

### `pages-core` `f4c63e608201`

* Repository: `pages-core`
* Commit SHA: `f4c63e60820144b45e23dea0c7e251fa39bb1214`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2019-04-15
* Files changed: `scripts/create-dev-data.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `scripts/create-dev-data.js: +           token: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show f4c63e60820144b45e23dea0c7e251fa39bb1214` and verify the change is expected.

### `pages-core` `a692106326fd`

* Repository: `pages-core`
* Commit SHA: `a692106326fdc240c3968d9512fec6688b9ada24`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2021-03-05
* Files changed: `test/api/support/cfUAANock.js`, `test/api/unit/services/uaaStrategy.test.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `test/api/support/cfUAANock.js: +function getUser(userId, profile, accessToken = '[REDACTED]') {`
  * `test/api/unit/services/uaaStrategy.test.js: +    const refreshToken = '[REDACTED]';`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show a692106326fdc240c3968d9512fec6688b9ada24` and verify the change is expected.

### `pages-core` `d58e4e79b247`

* Repository: `pages-core`
* Commit SHA: `d58e4e79b2473ee9bf3d8052d612631ab9ef101c`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2021-04-16
* Files changed: `scripts/create-dev-data.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `scripts/create-dev-data.js: +        githubAccessToken: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show d58e4e79b2473ee9bf3d8052d612631ab9ef101c` and verify the change is expected.

### `pages-core` `727308031af6`

* Repository: `pages-core`
* Commit SHA: `727308031af632b34e624517a8f7903e20e377fe`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2021-05-26
* Files changed: `config/local.sample.js`, `test/api/unit/services/organization.test.js`, `test/api/unit/utils/uaaClient.test.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `config/local.sample.js: +  clientSecret: '[REDACTED]',`
  * `config/local.sample.js: +          clientSecret: '[REDACTED]',`
  * `test/api/unit/services/organization.test.js: +        accessToken: '[REDACTED]',`
  * `test/api/unit/services/organization.test.js: +        refreshToken: '[REDACTED]',`
  * `test/api/unit/services/organization.test.js: +        const userToken = '[REDACTED]';`
  * `test/api/unit/utils/uaaClient.test.js: +    const clientToken = '[REDACTED]';`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 727308031af632b34e624517a8f7903e20e377fe` and verify the change is expected.

### `pages-core` `16518fbe271f`

* Repository: `pages-core`
* Commit SHA: `16518fbe271f0ecf570decbb3e3a991decb2f745`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2022-12-19
* Files changed: `api/models/event.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `api/models/event.js: +    AUTHENTICATION_PAGES_GH_TOKEN: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 16518fbe271f0ecf570decbb3e3a991decb2f745` and verify the change is expected.

### `pages-core` `8032a3be43b9`

* Repository: `pages-core`
* Commit SHA: `8032a3be43b9cc675ddcb4392a9bd3285c4d6c9d`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <apburnes@gmail.com>
* Date: 2023-06-09
* Files changed: `test/api/unit/services/SiteBuildQueue.test.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `test/api/unit/services/SiteBuildQueue.test.js: +        .user({ githubAccessToken: '[REDACTED]' })`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 8032a3be43b9cc675ddcb4392a9bd3285c4d6c9d` and verify the change is expected.

### `pages-core` `7417e38b5437`

* Repository: `pages-core`
* Commit SHA: `7417e38b5437c7e53ee76cf19df5ca2adc267cc6`
* Author/committer: Andrew Burnes <apburnes@gmail.com> / Andrew Burnes <apburnes@gmail.com>
* Date: 2023-07-31
* Files changed: `scripts/create-dev-data.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `scripts/create-dev-data.js: +      githubAccessToken: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 7417e38b5437c7e53ee76cf19df5ca2adc267cc6` and verify the change is expected.

### `pages-core` `5293be4a3e62`

* Repository: `pages-core`
* Commit SHA: `5293be4a3e622f8a961ebe45bbad5c33564eeae1`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-01-10
* Files changed: `ci/tasks/configure-database-migrations.js`
* Why it is suspicious: auth weakening (Medium/Medium)
* Evidence from the diff:
  * `ci/tasks/configure-database-migrations.js: +    rejectUnauthorized: false,`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 5293be4a3e622f8a961ebe45bbad5c33564eeae1` and verify the change is expected.

### `pages-core` `c0290556a068`

* Repository: `pages-core`
* Commit SHA: `c0290556a0680077280a5cccdcc8a5b0701c2802`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-06-13
* Files changed: `test/api/unit/services/Encryptor.test.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `test/api/unit/services/Encryptor.test.js: +      const password = '[REDACTED]';`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show c0290556a0680077280a5cccdcc8a5b0701c2802` and verify the change is expected.

### `pages-core` `b3116474b0db`

* Repository: `pages-core`
* Commit SHA: `b3116474b0db1e2cbd7dea2f4652866d9c77e6ba`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-10-29
* Files changed: `api/controllers/build.js`, `api/utils/site.js`, `scripts/create-dev-data.js`, `test/api/requests/build.test.js`, `test/api/unit/services/S3Helper.test.js`, `test/api/workers/Mailer.test.js`
* Why it is suspicious: credential exposure (Medium/Medium), obfuscation (Low/Low)
* Evidence from the diff:
  * `api/utils/site.js: +      password: '[REDACTED]',`
  * `scripts/create-dev-data.js: +        githubAccessToken: '[REDACTED]',`
  * `test/api/requests/build.test.js: +          token: '[REDACTED]',`
  * `test/api/requests/build.test.js: +        token: '[REDACTED]',`
  * `test/api/requests/build.test.js: +            buildToken: '[REDACTED]',`
  * `test/api/unit/services/S3Helper.test.js: +          ContinuationToken: '[REDACTED]',`
  * `api/controllers/build.js: +const decodeb64 = (str) => Buffer.from(str, 'base64').toString('utf8');`
  * `test/api/requests/build.test.js: +    const encode64 = (str) => Buffer.from(str, 'utf8').toString('base64');`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show b3116474b0db1e2cbd7dea2f4652866d9c77e6ba` and verify the change is expected.

### `pages-core` `d106f75851ac`

* Repository: `pages-core`
* Commit SHA: `d106f75851ac9a034dc7bc82792ae94f00e5e23c`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-11-14
* Files changed: `test/frontend/support/data/builds.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `test/frontend/support/data/builds.js: +        token: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show d106f75851ac9a034dc7bc82792ae94f00e5e23c` and verify the change is expected.

### `pages-core` `242d8e7343e5`

* Repository: `pages-core`
* Commit SHA: `242d8e7343e5119847c41570a4f76405f5dbd2ac`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-04-17
* Files changed: `test/api/requests/webhook.test.js`, `test/api/workers/jobProcessors/createEditorSite.test.js`
* Why it is suspicious: credential exposure (Medium/Medium), exfiltration (Medium/Low)
* Evidence from the diff:
  * `test/api/workers/jobProcessors/createEditorSite.test.js: +      const apiKey = '[REDACTED]';`
  * `test/api/requests/webhook.test.js: +      await request(app).post('/webhook/site').send(payload).expect(400);`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 242d8e7343e5119847c41570a4f76405f5dbd2ac` and verify the change is expected.

### `pages-core` `fed05f015e78`

* Repository: `pages-core`
* Commit SHA: `fed05f015e78261edc3cab5a2761d3cf630346a2`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-04-25
* Files changed: `test/api/requests/webhook.test.js`
* Why it is suspicious: credential exposure (Medium/Medium), exfiltration (Medium/Low)
* Evidence from the diff:
  * `test/api/requests/webhook.test.js: +      const apiKey = '[REDACTED]';`
  * `test/api/requests/webhook.test.js: +      await request(app).post('/webhook/site').send(payload).expect(200);`
  * `test/api/requests/webhook.test.js: +      await request(app).post('/webhook/site/build').send(payload).expect(200);`
  * `test/api/requests/webhook.test.js: +      await request(app).post('/webhook/site/build').send(payload).expect(400);`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show fed05f015e78261edc3cab5a2761d3cf630346a2` and verify the change is expected.

### `pages-core` `69718e6e4892`

* Repository: `pages-core`
* Commit SHA: `69718e6e4892cac861404f8b4b3987b4380e0c7b`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-09
* Files changed: `scripts/create-dev-data.js`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `scripts/create-dev-data.js: +      token: '[REDACTED]',`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 69718e6e4892cac861404f8b4b3987b4380e0c7b` and verify the change is expected.

### `pages-core` `a84817fd0643`

* Repository: `pages-core`
* Commit SHA: `a84817fd0643a1e8158f7ef42c5c2197b07521ef`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-17
* Files changed: `ci/tasks/check-audit.js`
* Why it is suspicious: suspicious system execution (Medium/Medium)
* Evidence from the diff:
  * `ci/tasks/check-audit.js: +const { spawnSync } = require('node:child_process');`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show a84817fd0643a1e8158f7ef42c5c2197b07521ef` and verify the change is expected.

### `pages-editor` `e9da62437a87`

* Repository: `pages-editor`
* Commit SHA: `e9da62437a87c96391d4458a515e76ce18322b56`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-10-29
* Files changed: `docker-compose.yml`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `docker-compose.yml: +      PAYLOAD_API_KEY: '[REDACTED]'`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show e9da62437a87c96391d4458a515e76ce18322b56` and verify the change is expected.

### `pages-editor` `cee20b65d7f3`

* Repository: `pages-editor`
* Commit SHA: `cee20b65d7f3e4b04673e27764d3f3409a5af6b8`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-05-21
* Files changed: `src/fields/styles/tokens.ts`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#f8eff1', family: 'Red Cool' },`
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#f3e1e4', family: 'Red Cool' },`
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#ecbec6', family: 'Red Cool' },`
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#e09aa6', family: 'Red Cool' },`
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#e16b80', family: 'Red Cool' },`
  * `src/fields/styles/tokens.ts: +  { token: '[REDACTED]', hex: '#cd425b', family: 'Red Cool' },`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show cee20b65d7f3e4b04673e27764d3f3409a5af6b8` and verify the change is expected.

### `pages-editor` `d5bdd7d92b7d`

* Repository: `pages-editor`
* Commit SHA: `d5bdd7d92b7d0dd44c4d55532d23fee593abc7b4`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-08
* Files changed: `package.json`
* Why it is suspicious: suspicious system execution (Medium/Medium)
* Evidence from the diff:
  * `package.json: +    "dc:migrate:up": "docker compose run --rm app sh -c 'yes \| npx payload migrate'",`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show d5bdd7d92b7d0dd44c4d55532d23fee593abc7b4` and verify the change is expected.

### `pages-site-gantry` `82d44a09013f`

* Repository: `pages-site-gantry`
* Commit SHA: `82d44a09013fd87e02cac9e80ae6be08dbc5ec60`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-07-23
* Files changed: `.env.example`
* Why it is suspicious: credential exposure (Medium/Medium)
* Evidence from the diff:
  * `.env.example: +PAYLOAD_API_KEY='[REDACTED]'`
  * `.env.example: +PAYLOAD_SECRET='[REDACTED]'`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-site-gantry show 82d44a09013fd87e02cac9e80ae6be08dbc5ec60` and verify the change is expected.

### `pages-build-container` `cfd669ddfbb7`

* Repository: `pages-build-container`
* Commit SHA: `cfd669ddfbb74f0382315b1f572964ede887bcae`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-09-11
* Files changed: `Dockerfile`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `Dockerfile: +# RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub \| apt-key add - \`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-build-container show cfd669ddfbb74f0382315b1f572964ede887bcae` and verify the change is expected.

### `pages-cf-build-tasks` `96805ff8a53d`

* Repository: `pages-cf-build-tasks`
* Commit SHA: `96805ff8a53d15cff998e637edf4fe7ca6a0d7d5`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-09-17
* Files changed: `tasks/a11y/.env`, `tasks/a11y/build.sh`, `tasks/a11y/reporter/package-lock.json`, `tasks/example/.env`, `tasks/owasp-zap/.env`, `tasks/owasp-zap/reporter/package-lock.json`
* Why it is suspicious: credential exposure (Low/Medium), exfiltration (Medium/Low)
* Evidence from the diff:
  * `tasks/a11y/build.sh: +wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub \| gpg --dearmor -o /usr/share/keyrings/google-linux-signing-key.gpg \`
  * `Sensitive-looking path changed: tasks/a11y/.env, tasks/example/.env, tasks/owasp-zap/.env`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-cf-build-tasks show 96805ff8a53d15cff998e637edf4fe7ca6a0d7d5` and verify the change is expected.

### `pages-cf-build-tasks` `e2eee66cfe39`

* Repository: `pages-cf-build-tasks`
* Commit SHA: `e2eee66cfe395f6469da37af269a86a58d952aa2`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-01
* Files changed: `tasks/a11y/build.sh`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `tasks/a11y/build.sh: +CHROME_DATA=$(curl -s "https://googlechromelabs.github.io/chrome-for-testing/last-known-good-versions-with-downloads.json")`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-cf-build-tasks show e2eee66cfe395f6469da37af269a86a58d952aa2` and verify the change is expected.

### `pages-core` `9ec7aa01f741`

* Repository: `pages-core`
* Commit SHA: `9ec7aa01f74182f141be959dbc91267fc1697355`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-12-05
* Files changed: `test/api/requests/webhook.test.js`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `test/api/requests/webhook.test.js: +      await request(app).delete('/webhook/site').send(payload).expect(200);`
  * `test/api/requests/webhook.test.js: +      await request(app).delete('/webhook/site').send(payload).expect(400);`
  * `test/api/requests/webhook.test.js: +      await request(app).delete('/webhook/site').send(payload).expect(422);`
  * `test/api/requests/webhook.test.js: +      await request(app).delete('/webhook/site').send(payload).expect(404);`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 9ec7aa01f74182f141be959dbc91267fc1697355` and verify the change is expected.

### `pages-editor` `b04e24afca56`

* Repository: `pages-editor`
* Commit SHA: `b04e24afca567fca1e5a8a4c8e7e55208bb892e7`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-04-23
* Files changed: `src/collections/Sites/hooks/index.ts`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `src/collections/Sites/hooks/index.ts: +      await fetch(`${process.env.PAGES_URL}/webhook/site`, {`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show b04e24afca567fca1e5a8a4c8e7e55208bb892e7` and verify the change is expected.

### `pages-editor` `032619726583`

* Repository: `pages-editor`
* Commit SHA: `0326197265839429632ab60e822960689efe60ef`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-05-15
* Files changed: `docker-compose.yml`
* Why it is suspicious: exfiltration (Medium/Low), suspicious system execution (Low/Low)
* Evidence from the diff:
  * `docker-compose.yml: +      test: [ "CMD", "curl", "-I", http://storage:9000/minio/health/live ]`
  * `docker-compose.yml: +      sh -c "mc alias set localminio http://storage:9000 pages-editor-access-key pages-editor-secret-key && mc mb localminio/pages-editor-bucket"`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 0326197265839429632ab60e822960689efe60ef` and verify the change is expected.

### `pages-editor` `3cc63456d934`

* Repository: `pages-editor`
* Commit SHA: `3cc63456d93479e66d3312434fbb47250af25dd0`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-08-12
* Files changed: `docker-compose.yml`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `docker-compose.yml: +      test: ['CMD', 'curl', '-I', http://storage:9000/minio/health/live]`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 3cc63456d93479e66d3312434fbb47250af25dd0` and verify the change is expected.

### `pages-editor` `93cc0e67d99f`

* Repository: `pages-editor`
* Commit SHA: `93cc0e67d99f0a2dd0f456d88d039dda304ae5ee`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-12-05
* Files changed: `src/collections/Sites/hooks/index.ts`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `src/collections/Sites/hooks/index.ts: +    await fetch(`${process.env.PAGES_URL}/webhook/site`, {`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 93cc0e67d99f0a2dd0f456d88d039dda304ae5ee` and verify the change is expected.

### `pages-editor` `23d848d98dfc`

* Repository: `pages-editor`
* Commit SHA: `23d848d98dfcb8c263ec5094140f62b2b11f29a7`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-03-12
* Files changed: `src/hooks/buildSite.ts`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `src/hooks/buildSite.ts: +    return fetch(`${process.env.PAGES_URL}/webhook/site/build`, {`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 23d848d98dfcb8c263ec5094140f62b2b11f29a7` and verify the change is expected.

### `pages-images` `cb2b81af472c`

* Repository: `pages-images`
* Commit SHA: `cb2b81af472ce8741fb4056e0959421506060f6b`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-01-30
* Files changed: `dind/v25/Dockerfile`, `node/v20/Dockerfile`
* Why it is suspicious: exfiltration (Medium/Low), security tooling disabled (Low/Low)
* Evidence from the diff:
  * `dind/v25/Dockerfile: +	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; \`
  * `node/v20/Dockerfile: +    && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz" \`
  * `node/v20/Dockerfile: +    && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc" \`
  * `node/v20/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz" \`
  * `node/v20/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc" \`
  * `dind/v25/Dockerfile: +# Set to skip prompt during USG audit`
  * `node/v20/Dockerfile: +# Set to skip prompt during USG audit`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-images show cb2b81af472ce8741fb4056e0959421506060f6b` and verify the change is expected.

### `pages-images` `0a8a1d11e5c8`

* Repository: `pages-images`
* Commit SHA: `0a8a1d11e5c857c1a78afa5668585e60cb0e5bb2`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2024-02-07
* Files changed: `python/v3.11/Dockerfile`
* Why it is suspicious: exfiltration (Medium/Low), security tooling disabled (Low/Low)
* Evidence from the diff:
  * `python/v3.11/Dockerfile: +RUN wget -O python.tgz "https://www.python.org/ftp/python/$PYTHON_VERSION/Python-$PYTHON_VERSION.tgz"; \`
  * `python/v3.11/Dockerfile: +# Set to skip prompt during USG audit`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-images show 0a8a1d11e5c857c1a78afa5668585e60cb0e5bb2` and verify the change is expected.

### `pages-images` `9bc49ef3aba8`

* Repository: `pages-images`
* Commit SHA: `9bc49ef3aba87db6e5387370c523e8a8c79b59d1`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2025-10-08
* Files changed: `node/v22/Dockerfile`
* Why it is suspicious: exfiltration (Medium/Low), security tooling disabled (Low/Low)
* Evidence from the diff:
  * `node/v22/Dockerfile: +  && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz" \`
  * `node/v22/Dockerfile: +  && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc" \`
  * `node/v22/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz" \`
  * `node/v22/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc" \`
  * `node/v22/Dockerfile: +# Set to skip prompt during USG audit`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-images show 9bc49ef3aba87db6e5387370c523e8a8c79b59d1` and verify the change is expected.

### `pages-images` `45546ef83371`

* Repository: `pages-images`
* Commit SHA: `45546ef8337127c08ddb9e955cc2e3dac6e1eded`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-01-12
* Files changed: `node/v24/Dockerfile`
* Why it is suspicious: exfiltration (Medium/Low), security tooling disabled (Low/Low)
* Evidence from the diff:
  * `node/v24/Dockerfile: +  && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz" \`
  * `node/v24/Dockerfile: +  && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc" \`
  * `node/v24/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz" \`
  * `node/v24/Dockerfile: +  && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc" \`
  * `node/v24/Dockerfile: +# Set to skip prompt during USG audit`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-images show 45546ef8337127c08ddb9e955cc2e3dac6e1eded` and verify the change is expected.

### `pages-redirects` `d45c3a112959`

* Repository: `pages-redirects`
* Commit SHA: `d45c3a1129591e1f779205051f54cd8b21e1be93`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2022-09-30
* Files changed: `.circleci/config.yml`
* Why it is suspicious: exfiltration (Medium/Low)
* Evidence from the diff:
  * `.circleci/config.yml: +            curl -L "https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-$(uname -s)-$(uname -m)" -o ~/docker-compose`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-redirects show d45c3a1129591e1f779205051f54cd8b21e1be93` and verify the change is expected.

### `pages-cf-build-tasks` `e0dc5861167f`

* Repository: `pages-cf-build-tasks`
* Commit SHA: `e0dc5861167f5c2e6fe54f4ed07803ae688dca59`
* Author/committer: Andrew Burnes <apburnes@gmail.com> / GitHub <noreply@github.com>
* Date: 2025-09-18
* Files changed: `tasks/a11y/.env`, `tasks/a11y/build.sh`, `tasks/a11y/reporter/package-lock.json`, `tasks/example/.env`, `tasks/owasp-zap/.env`, `tasks/owasp-zap/reporter/package-lock.json`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: tasks/a11y/.env, tasks/example/.env, tasks/owasp-zap/.env`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-cf-build-tasks show e0dc5861167f5c2e6fe54f4ed07803ae688dca59` and verify the change is expected.

### `pages-core` `9b31afcdbaba`

* Repository: `pages-core`
* Commit SHA: `9b31afcdbaba0f7a7be3081fd755598026f3658a`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / GitHub <noreply@github.com>
* Date: 2026-05-20
* Files changed: `.cloudgov/manifest.yml`, `.github/pull_request_template.md`, `.gitignore`, `.npmrc`, `.nvmrc`, `Dockerfile-app`, `Dockerfile-pw`, `Makefile`, `admin-client/.gitignore`, `admin-client/.npmrc`, `admin-client/.nvmrc`, `admin-client/Dockerfile-admin`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc, admin-client/.npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 9b31afcdbaba0f7a7be3081fd755598026f3658a` and verify the change is expected.

### `pages-editor` `8e55be9080fb`

* Repository: `pages-editor`
* Commit SHA: `8e55be9080fb320dbae79a9eab6444b4eb0aa5cf`
* Author/committer: Andrew Burnes <apburnes@gmail.com> / GitHub <noreply@github.com>
* Date: 2026-06-01
* Files changed: `.npmrc`, `Dockerfile`, `ci/pipeline.yml`, `docker/Dockerfile-pages-site-gantry`, `package-lock.json`, `package.json`, `src/app/(payload)/admin/importMap.js`, `src/fields/styles/UswdsColorSelect.tsx`, `src/fields/styles/index.scss`, `src/fields/styles/tokens.ts`, `src/fields/styles/uswdsColors.ts`, `src/globals/SiteConfig.ts`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 8e55be9080fb320dbae79a9eab6444b4eb0aa5cf` and verify the change is expected.

### `pages-editor` `a04e86640799`

* Repository: `pages-editor`
* Commit SHA: `a04e866407990815190b5b8f8f6c1e304a972c36`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-01
* Files changed: `.npmrc`, `Dockerfile`, `ci/pipeline.yml`, `docker/Dockerfile-pages-site-gantry`, `package-lock.json`, `package.json`, `src/app/(payload)/admin/importMap.js`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show a04e866407990815190b5b8f8f6c1e304a972c36` and verify the change is expected.

### `pages-site-gantry` `9060d63a6219`

* Repository: `pages-site-gantry`
* Commit SHA: `9060d63a6219186ee1482837bbdd884519ddaf88`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-05-26
* Files changed: `.lintstylesignore`, `.npmrc`, `.nvmrc`, `astro.config.ts`, `ci/pipeline.yml`, `docs/STYLING.md`, `package-lock.json`, `package.json`, `scripts/lint-styles.sh`, `scripts/setTheme.ts`, `src/components/Footer.astro`, `src/components/Identifier.astro`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-site-gantry show 9060d63a6219186ee1482837bbdd884519ddaf88` and verify the change is expected.

### `pages-site-gantry` `4738bcbb39d9`

* Repository: `pages-site-gantry`
* Commit SHA: `4738bcbb39d9dc0b9838c1d74192139e1fad8b4e`
* Author/committer: Andrew Burnes <apburnes@gmail.com> / GitHub <noreply@github.com>
* Date: 2026-06-01
* Files changed: `.lintstylesignore`, `.npmrc`, `.nvmrc`, `astro.config.ts`, `ci/pipeline.yml`, `docs/STYLING.md`, `package-lock.json`, `package.json`, `scripts/lint-styles.sh`, `scripts/setTheme.ts`, `src/components/Footer.astro`, `src/components/Identifier.astro`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-site-gantry show 4738bcbb39d9dc0b9838c1d74192139e1fad8b4e` and verify the change is expected.

### `pages-uswds-11ty` `89a6e8c5bfba`

* Repository: `pages-uswds-11ty`
* Commit SHA: `89a6e8c5bfbaa3b0e8fc14ef4867a4f9abea087a`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-05-20
* Files changed: `.npmrc`, `package-lock.json`, `package.json`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-uswds-11ty show 89a6e8c5bfbaa3b0e8fc14ef4867a4f9abea087a` and verify the change is expected.

### `pages-uswds-11ty` `96294a4ab790`

* Repository: `pages-uswds-11ty`
* Commit SHA: `96294a4ab790c7a1ad11d9bea119541b63c8cf24`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / GitHub <noreply@github.com>
* Date: 2026-05-20
* Files changed: `.npmrc`, `package-lock.json`, `package.json`
* Why it is suspicious: credential exposure (Low/Medium)
* Evidence from the diff:
  * `Sensitive-looking path changed: .npmrc`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-uswds-11ty show 96294a4ab790c7a1ad11d9bea119541b63c8cf24` and verify the change is expected.

### `pages-core` `1eeebf96cffa`

* Repository: `pages-core`
* Commit SHA: `1eeebf96cffa9deadeeac2d1739ffc74041041dc`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2020-09-17
* Files changed: `api/utils/index.js`
* Why it is suspicious: suspicious system execution (Low/Low)
* Evidence from the diff:
  * `api/utils/index.js: +  const result = /^\d+$/.exec(val);`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 1eeebf96cffa9deadeeac2d1739ffc74041041dc` and verify the change is expected.

### `pages-core` `9aeb74821a54`

* Repository: `pages-core`
* Commit SHA: `9aeb74821a543d0f04a0587c6b53c89f004a3438`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-03
* Files changed: `admin-client/src/lib/page/index.js`
* Why it is suspicious: suspicious system execution (Low/Low)
* Evidence from the diff:
  * `admin-client/src/lib/page/index.js: +    m = this.regexp.exec(decodeURIComponent(pathname));`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show 9aeb74821a543d0f04a0587c6b53c89f004a3438` and verify the change is expected.

### `pages-core` `c91bdd43d919`

* Repository: `pages-core`
* Commit SHA: `c91bdd43d919b8f95e9c5e3682dea6aab68a4d9b`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-03
* Files changed: `admin-client/rollup.config.js.backup`
* Why it is suspicious: suspicious system execution (Low/Low)
* Evidence from the diff:
  * `admin-client/rollup.config.js.backup: +      server = require('child_process').spawn('npm', ['run', 'start'], {`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-core show c91bdd43d919b8f95e9c5e3682dea6aab68a4d9b` and verify the change is expected.

### `pages-editor` `311c843a85d4`

* Repository: `pages-editor`
* Commit SHA: `311c843a85d40047adf8ff9955592ef6aa55c1e6`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-04-29
* Files changed: `src/middleware.ts`
* Why it is suspicious: obfuscation (Low/Low)
* Evidence from the diff:
  * `src/middleware.ts: +  const nonce = Buffer.from(crypto.randomUUID()).toString('base64')`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 311c843a85d40047adf8ff9955592ef6aa55c1e6` and verify the change is expected.

### `pages-editor` `9e76ce4e1748`

* Repository: `pages-editor`
* Commit SHA: `9e76ce4e17480b90f1497e394e9da0fbe7b42fd5`
* Author/committer: Andrew Burnes <andrew.burnes@gsa.gov> / Andrew Burnes <andrew.burnes@gsa.gov>
* Date: 2026-06-11
* Files changed: `test/utils/globalSetup.ts`
* Why it is suspicious: suspicious system execution (Low/Low)
* Evidence from the diff:
  * `test/utils/globalSetup.ts: +        await exec('yes \| FEATURE_FORMS=enabled DATABASE_URI=$TEST_DATABASE_URI npm run payload migrate:fresh')`
* Safer explanation or possible false positive: This is a pattern-based review signal from a defensive audit; legitimate tests, local dev fixtures, or platform integration code may explain it.
* Recommended next step: Inspect with `git -C pages-editor show 9e76ce4e17480b90f1497e394e9da0fbe7b42fd5` and verify the change is expected.

## Per-Repository Details

### `pages-core`

* Path: `/Users/brianjhurst/Code/pages-core`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/KKAtila-patch-1, origin/chore-localstack, origin/chore-no-dev-on-release, origin/chore-test-rspack, origin/dependabot/npm_and_yarn/admin-client/npm_and_yarn-0a6d3f2c61, origin/dependabot/npm_and_yarn/npm_and_yarn-45e9ac6fd3, origin/dependabranch, origin/feat-New-Site-UI-with-the-addition-of-Workshop-4899, origin/feat-add-asr-rule-suppressionn-from-report, origin/feat-add-task-report-rendering (+6 more)
* Remotes: `origin	https://github.com/cloud-gov/pages-core.git (fetch)`; `origin	https://github.com/cloud-gov/pages-core.git (push)`
* Matching commit count: 589
* Suspicious commit count: 23
* Timeline: 2019-03-20 to 2026-06-18
* Total files changed across matching commits: 6341
* Total insertions/deletions: 378739 / 255761
* Top changed file paths: `package.json` (123), `yarn.lock` (76), `ci/pipeline.yml` (64), `.cloudgov/manifest.yml` (57), `docker-compose.yml` (48), `scripts/create-dev-data.js` (46), `test/api/requests/site.test.js` (46), `test/api/unit/services/SiteCreator.test.js` (43)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-18 | `4aa6314546a6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4928 from cloud-gov/release | 3 | 15 | 5 | No |
| 2026-06-18 | `2d9f1bcb928b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4929 from cloud-gov/chore-remove-build-status-notifier | 29 | 412 | 1293 | No |
| 2026-06-17 | `a84817fd0643` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove build status notifications and dependencies | 29 | 412 | 1293 | Yes |
| 2026-06-17 | `f12855a095a7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4927 from cloud-gov/fix-admin-error-logging | 6 | 94 | 1116 | No |
| 2026-06-17 | `a17f2af2c566` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(admin): Fix event body rendering in admin UI | 6 | 94 | 1116 | No |
| 2026-06-10 | `5bdffc151a36` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4925 from cloud-gov/release | 3 | 19 | 3 | No |
| 2026-06-10 | `1efb0fc1a0d9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4926 from cloud-gov/fix-admin-asset-bundles | 22 | 255 | 156 | No |
| 2026-06-09 | `69718e6e4892` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(admin): Correct the asset paths for nested routes | 22 | 255 | 156 | Yes |
| 2026-06-08 | `5e578cf022bb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4908 from cloud-gov/release | 3 | 43 | 5 | No |
| 2026-06-08 | `a637d8329c8b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4922 from cloud-gov/chore-ci-add-package-lock-to-prettierignore | 39 | 3509 | 2132 | No |
| 2026-06-03 | `9aeb74821a54` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(admin): Vendor page router to allow for dependency updates | 20 | 918 | 63 | Yes |
| 2026-06-03 | `c91bdd43d919` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Upgrade admin client to svelte v5 | 27 | 2588 | 2003 | Yes |
| 2026-06-03 | `2c52a23838a2` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Update .prettierignore to ignore package-lock.json | 2 | 27 | 90 | No |
| 2026-05-21 | `909bd8c7ad84` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4914 from cloud-gov/chore-remove-gatsby-template | 3 | 3 | 16 | No |
| 2026-05-21 | `69cb7ac24f2d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove archived gatsby template from site choices | 3 | 3 | 16 | No |
| 2026-05-21 | `f6414b4636a9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4912 from cloud-gov/feat-default-to-large-container-at-10gb | 4 | 5 | 2 | No |
| 2026-05-20 | `9b31afcdbaba` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4911 from cloud-gov/chore-Update-core-to-use-NPM-install-with-improved-security-config-2949 | 40 | 31669 | 16097 | Yes |
| 2026-05-20 | `e6f9ae06fbb5` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Site defaults to large container with new 10GB disk space | 4 | 5 | 2 | No |
| 2026-05-14 | `eeac33b21bae` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4904 from cloud-gov/release | 2 | 11 | 1 | No |
| 2026-05-14 | `b33d4b6ea2cf` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4906 from cloud-gov/chore-remove-public-storage-feature-flag | 13 | 2220 | 2254 | No |
| 2026-05-13 | `5e478c1c3127` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove public file storage feature flag | 13 | 2220 | 2254 | No |
| 2026-05-04 | `dc822bc4da00` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4895 from cloud-gov/release | 2 | 18 | 1 | No |
| 2026-05-04 | `3d7dcfc2ba3b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4896 from cloud-gov/chore-add-webhook-rotation-script | 5 | 187 | 6 | No |
| 2026-04-21 | `e07f3b772bd2` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add webhook rotation script | 5 | 187 | 6 | No |
| 2026-04-16 | `eb53682f63b8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4882 from cloud-gov/release | 2 | 17 | 1 | No |
| 2026-04-16 | `a6f95b578836` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4891 from cloud-gov/fix-public-file-details-modal-button-color | 5 | 40 | 15 | No |
| 2026-04-14 | `1759530f79a0` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: getOwnerAndRepo to return workshop site designation when feature flag is on and off | 4 | 13 | 8 | No |
| 2026-04-14 | `c84130d989b6` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Public File details modal buttons | 3 | 30 | 10 | No |
| 2026-04-14 | `8a03744df50e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4890 from cloud-gov/fix-file-storage-button-colors | 8 | 22 | 11 | No |
| 2026-04-13 | `6d37aaea3294` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Ouptut config for e2e tests | 1 | 0 | 1 | No |
| 2026-04-13 | `86fb8ecf4b46` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Button colors and contrast on the public file storage views | 7 | 22 | 10 | No |
| 2026-04-02 | `fa26120bf080` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4881 from cloud-gov/fix-clamav-rest-image | 7 | 3718 | 3958 | No |
| 2026-04-01 | `74f8a84caa27` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): ClamAV REST image source | 7 | 3718 | 3958 | No |
| 2026-04-01 | `0b484adb0175` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4839 from cloud-gov/release | 2 | 32 | 1 | No |
| 2026-03-19 | `d4cab96e1333` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4861 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-core | 4 | 1177 | 1425 | No |
| 2026-03-18 | `17c654cf7b22` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4862 from cloud-gov/feat-create-workshop-site-build-flow-4856 | 56 | 870 | 197 | No |
| 2026-03-05 | `a3f2cc7e5371` | William Zujkowski <william.zujkowski@gsa.gov> | chore: Remove deprecated security-considerations automation files | 4 | 1177 | 1425 | No |
| 2026-03-03 | `1e3f3e497edb` | Andrew Burnes <andrew.burnes@gsa.gov> | Temp branch for dev deploy | 1 | 0 | 0 | No |
| 2026-01-30 | `95a3c7cd9e5b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4846 from cloud-gov/chore-update-new-branding-logos-colors | 15 | 258 | 31 | No |
| 2026-01-27 | `777bcf3b94e5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4841 from cloud-gov/feat-update-apps-to-node-v22-and-update-dependencies | 6 | 1617 | 1596 | No |
| 2026-01-05 | `557bff9d4f06` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Update app to Node v22 and update the dependencies | 6 | 1617 | 1596 | No |
| 2025-12-09 | `d65a9501df48` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4840 from cloud-gov/fix-publisher-endpoint-host-var | 7 | 9 | 6 | No |
| 2025-12-09 | `bc94e4ea120c` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Publisher endpoint host environment variable | 7 | 9 | 6 | No |
| 2025-12-09 | `c8b07cd536f3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4837 from cloud-gov/fix-bound-route-service-domain-name | 1 | 1 | 1 | No |
| 2025-12-05 | `a7b3e1c8875a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4838 from cloud-gov/feat-add-site-delete-webhook-for-publisher | 6 | 1105 | 693 | No |
| 2025-12-05 | `9ec7aa01f741` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site delete webhook for publisher site | 6 | 1105 | 693 | Yes |
| 2025-12-01 | `660c00117791` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Use the correct bound route service domain by env | 1 | 1 | 1 | No |
| 2025-12-01 | `b7b560ffeda4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4836 from cloud-gov/release | 2 | 7 | 1 | No |
| 2025-12-01 | `9bd752c6003a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4835 from cloud-gov/fix-clamav-ci-resource-for-prod | 1 | 0 | 2 | No |
| 2025-12-01 | `7985e843b39f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI clamav resources for prod deploy | 1 | 0 | 2 | No |
| 2025-12-01 | `15b27c56321e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4803 from cloud-gov/release | 2 | 29 | 1 | No |
| 2025-12-01 | `31cddc573440` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4834 from cloud-gov/feat-enable-file-storage-in-production | 2 | 1 | 4 | No |
| 2025-12-01 | `4258967ca796` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Enable public file storage service in production | 2 | 1 | 4 | No |
| 2025-10-22 | `fe5cf90811a8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4833 from cloud-gov/update-links | 15 | 29 | 26 | No |
| 2025-10-22 | `e0b8a7876df1` | Ephraim-G <ephraim.gross@gsa.gov> | chore: update documentation links | 15 | 29 | 26 | No |
| 2025-10-15 | `5be998ae8389` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4827 from cloud-gov/bh-typo-fix | 1 | 1 | 1 | No |
| 2025-10-02 | `c2c66b0b9199` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4830 from cloud-gov/chore-update-axios-and-delete-derecated-frontend-tests | 97 | 24 | 9172 | No |
| 2025-10-02 | `c47f82fb2382` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4829 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `138102adcd27` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update axios and delete deprecated frontend tests | 97 | 24 | 9172 | No |
| 2025-10-02 | `b524c9339afe` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-09-26 | `f177ef66e1a7` | Brian Hurst <brian.hurst@gsa.gov> | fix: Automated platform build message for new domains | 1 | 1 | 1 | No |
| 2025-09-08 | `8d53a1805445` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4815 from cloud-gov/chore-adjust-file-details-ui | 8 | 69 | 35 | No |
| 2025-09-08 | `b584194a34e8` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Clean up File Details UI with fixed links and button types | 8 | 69 | 35 | No |
| 2025-09-02 | `9ef183b22322` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4812 from cloud-gov/feat-add-route-service-cookie-check | 3 | 71 | 0 | No |
| 2025-08-28 | `06e1a0aadf42` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add route service cookie check for clamav file endpoints | 3 | 71 | 0 | No |
| 2025-08-12 | `c082c752723d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4810 from cloud-gov/ci-fix-resources-for-route-service-envs | 1 | 33 | 4 | No |
| 2025-08-12 | `496319111e6a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4808 from cloud-gov/feat-add-clamav-rest-scan-route-service | 17 | 1053 | 429 | No |
| 2025-08-12 | `917121be8f9f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Properly configure route service resources for non-prod envs | 1 | 33 | 4 | No |
| 2025-07-30 | `5acbf23e8057` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add route-service app | 17 | 1011 | 430 | No |
| 2025-07-21 | `e40e422acb7f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add ClamAV REST scan route service | 1 | 43 | 0 | No |
| 2025-07-07 | `15b2f28ff4fd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4805 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 1 | No |
| 2025-07-07 | `a219b01e2102` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 1 | No |
| 2025-06-30 | `d427cf9e2e4d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4802 from cloud-gov/chore-update-dependencies-20250630 | 4 | 3043 | 3130 | No |
| 2025-06-30 | `aeb38ebb0ff8` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update csurf and app build dependencies | 4 | 3043 | 3130 | No |
| 2025-06-09 | `54624565a011` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4789 from cloud-gov/release | 2 | 19 | 1 | No |
| 2025-06-09 | `6e7f877e94a8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4797 from cloud-gov/chore-update-dependencies | 3 | 25 | 59 | No |
| 2025-06-09 | `9e0e3ca24069` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update multer to v2.0.1 | 2 | 29 | 156 | No |
| 2025-06-09 | `9df850b9cec7` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update FileDetails link to use site domain with file s3 key | 1 | 2 | 1 | No |
| 2025-06-02 | `3854e313a051` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4794 from cloud-gov/update-contrib-20250522220411 | 1 | 13 | 14 | No |
| 2025-05-30 | `f9b3110f0154` | Ephraim-G <ephraim.gross@gsa.gov> | chore: Update dependencies 2025-05-30 | 2 | 103 | 11 | No |
| 2025-05-22 | `ec0f72cff54f` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Update CONTRIBUTING.md | 1 | 13 | 14 | No |
| 2025-04-30 | `ff64d303671e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4792 from cloud-gov/feat-add-bucket-name-to-editor-webhook-response | 5 | 24 | 12 | No |
| 2025-04-29 | `df2087bef214` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add bucket name to Pages Editor webhook response | 5 | 24 | 12 | No |
| 2025-04-28 | `3ebb0916eb48` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4790 from cloud-gov/feat-add-editor-site-build-webhook | 5 | 179 | 17 | No |
| 2025-04-25 | `fed05f015e78` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add webhook to create editor site builds | 5 | 179 | 17 | Yes |
| 2025-04-24 | `52af2bb08158` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4786 from cloud-gov/feat-add-webhook-to-create-editor-site | 32 | 658 | 125 | No |
| 2025-04-21 | `bf7c59d98c81` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4785 from cloud-gov/release | 2 | 9 | 1 | No |
| 2025-04-21 | `3652df9db952` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4787 from cloud-gov/fix-build-tasks-feature-flag | 5 | 10 | 32 | No |
| 2025-04-21 | `276548b78ad3` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Site build tasks feature flag | 5 | 10 | 32 | No |
| 2025-04-17 | `242d8e7343e5` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add webhook to create an editor site | 32 | 658 | 125 | Yes |
| 2025-04-15 | `6dbe28ed90ba` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4765 from cloud-gov/release | 2 | 15 | 1 | No |
| 2025-04-11 | `06546cda57ee` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4782 from cloud-gov/feat-add-file-storage-waitlist-alert | 7 | 39 | 42 | No |
| 2025-04-10 | `185e83cbd4f9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4781 from cloud-gov/fix-auth-callback-500-error | 3 | 29 | 1 | No |
| 2025-04-09 | `c28e23be1931` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add public file storage waitlist alert | 7 | 39 | 42 | No |
| 2025-04-08 | `50f2f5318c45` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Return status 403 for invalid uaa oauth code | 3 | 29 | 1 | No |
| 2025-04-08 | `bc76e51a7f7f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4779 from cloud-gov/fix-file-view-details-alert-flash | 8 | 165 | 93 | No |
| 2025-04-03 | `2ed8065b5cd0` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: File view details alert to not flash on load | 8 | 165 | 93 | No |
| 2025-04-01 | `50cbbc1b105e` | Andrew Burnes <andrew.burnes@gsa.gov> | test: Add file page query files to prime file query | 4 | 38 | 15 | No |
| 2025-03-27 | `e896f378de6f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Create file storage file view | 18 | 483 | 231 | No |
| 2025-03-26 | `ed8c6883e757` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4759 from cloud-gov/feat-create-file-upload-hook-queue | 8 | 412 | 249 | No |
| 2025-03-25 | `39f353c99ccc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4756 from cloud-gov/release | 2 | 15 | 1 | No |
| 2025-03-25 | `669cd4e3c1ea` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4764 from cloud-gov/fix-errant-federalist-api-error-handling | 1 | 6 | 15 | No |
| 2025-03-25 | `89a5ea0295a7` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: UI data fetch error handling #4763 | 1 | 6 | 15 | No |
| 2025-03-20 | `a458a3bef31c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Create a file upload hook to queue uploads | 8 | 412 | 249 | No |
| 2025-03-19 | `8bd48f70ba92` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4755 from cloud-gov/chore-update-file-public-url | 5 | 52 | 103 | No |
| 2025-03-19 | `126f686ad20f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4754 from cloud-gov/confirm-file-storage-dialog-4743 | 3 | 457 | 14 | No |
| 2025-03-19 | `082a30513e3d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update file url to use baseUrl and file key | 5 | 52 | 103 | No |
| 2025-03-18 | `a9693fba8ae3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4723 from cloud-gov/release | 2 | 19 | 1 | No |
| 2025-03-12 | `4c0629478020` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4749 from cloud-gov/feat-add-last-modified-attributes-to-file-query | 12 | 525 | 222 | No |
| 2025-03-12 | `468cd78e772d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4742 from cloud-gov/file-storage-upload-2274 | 14 | 1356 | 778 | No |
| 2025-03-06 | `e35764c77735` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add last modified attributes to file queries | 12 | 525 | 222 | No |
| 2025-03-05 | `655b45da31a4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4741 from cloud-gov/chore-set-file-storage-env-flag-for-ui-build | 3 | 13 | 8 | No |
| 2025-03-04 | `06044ddda2cc` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set file storage feature env flag in UI | 3 | 13 | 8 | No |
| 2025-02-28 | `5b113f9ef488` | Sarah Rudder <sarah.rudder@gsa.gov> | feat: add components, view, and route for file storage ui | 33 | 2778 | 16 | No |
| 2025-02-28 | `9e5299c5a1df` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4740 from cloud-gov/feat-check-for-duplicate-file-storages-keys | 4 | 184 | 7 | No |
| 2025-02-27 | `c97193c44f4a` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Check for duplicate file storage files | 4 | 184 | 7 | No |
| 2025-02-26 | `8099787b7264` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4734 from cloud-gov/chore-add-files-to-seed-data | 12 | 309 | 33 | No |
| 2025-02-26 | `0ae7a20edb9d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add file storage seeding to create-dev-data #4733 | 12 | 309 | 33 | No |
| 2025-02-25 | `ed8395aa678b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4725 from cloud-gov/chor-add-file-storage-for-local-dev-4717 | 14 | 338 | 43 | No |
| 2025-02-18 | `61d0d8f2ca8c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Create services to support file storage local dev | 14 | 338 | 43 | No |
| 2025-02-14 | `4d0f803f4220` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4724 from cloud-gov/feat-feature-branch-file-storage | 9 | 14 | 8 | No |
| 2025-02-13 | `1bc75e9260b6` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add feature flag for file storage #4718 | 9 | 14 | 8 | No |
| 2025-02-13 | `6f5c1417df4d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4715 from cloud-gov/feat-add-api-endoints-for-file-storage-2082 | 55 | 5028 | 70 | No |
| 2025-01-16 | `95b1a1512754` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4673 from cloud-gov/release | 2 | 33 | 1 | No |
| 2025-01-15 | `2a7a687aaf77` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add API endpoints for file storage #2082 | 55 | 5028 | 70 | No |
| 2025-01-14 | `ff1f51d1e892` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4701 from cloud-gov/feat-add-db-migrations-for-file-storage-2077 | 1 | 237 | 0 | No |
| 2025-01-13 | `d146a514551d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add db migrations for file storage service #2077 | 1 | 237 | 0 | No |
| 2024-12-19 | `8499bab23420` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4697 from cloud-gov/chore-reenable-sonarjs-lint-rules-4652 | 19 | 194 | 677 | No |
| 2024-12-19 | `7fbea5243912` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Reenable sonarjs linting rules #4652 | 19 | 194 | 677 | No |
| 2024-12-06 | `1ea40311a927` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4687 from cloud-gov/chore-test-shared/GithubAuthButton-4671 | 4 | 202 | 11 | No |
| 2024-12-04 | `c73ba0e0c322` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Test shared/GithubAuthButton #4671 | 4 | 202 | 11 | No |
| 2024-11-26 | `8b1123377fa9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4684 from cloud-gov/chore-test-shared-user-org-select | 3 | 80 | 15 | No |
| 2024-11-25 | `b5e6e1c8f355` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Test shared user org select #4667 | 3 | 80 | 15 | No |
| 2024-11-20 | `9ed3e84539ea` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4663 from cloud-gov/fix-build-polling-and-latest-build-branch | 22 | 2457 | 879 | No |
| 2024-11-14 | `d106f75851ac` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Site build polling and latest build branch | 22 | 2457 | 879 | Yes |
| 2024-11-12 | `d939a7422c1f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4658 from cloud-gov/chore-enable-eslint-plugin-import-frontend-test | 6 | 23 | 6 | No |
| 2024-11-08 | `37a5c3023c23` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Enable eslint-plugin-import for frontend and tests | 6 | 23 | 6 | No |
| 2024-11-06 | `92aeba1e937b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4655 from cloud-gov/chore-decouple-local-app-builds-4649 | 8 | 309 | 795 | No |
| 2024-11-06 | `934b27953b16` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Decouple local app frontend build #4649 | 8 | 309 | 795 | No |
| 2024-10-30 | `86e576887a82` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4646 from cloud-gov/chore-run-formatting-on-codebase | 666 | 21732 | 12948 | No |
| 2024-10-29 | `b3116474b0db` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Run prettier formatting on codebase | 666 | 21732 | 12948 | Yes |
| 2024-10-29 | `08195977d00c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4639 from cloud-gov/chore-update-linting-and-formatting | 117 | 1270 | 825 | No |
| 2024-10-28 | `78546afcff52` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4638 from cloud-gov/release | 2 | 10 | 1 | No |
| 2024-10-24 | `954d07e88213` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update linting and formatting | 117 | 1270 | 825 | No |
| 2024-10-10 | `644a4efd5d4b` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Test Rspack bundler | 4 | 674 | 13 | No |
| 2024-09-26 | `cd145e6a5f66` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4602 from cloud-gov/release | 2 | 27 | 1 | No |
| 2024-09-19 | `0e1d09a6e887` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4599 from cloud-gov/chore-asr-punchlist | 13 | 406 | 178 | No |
| 2024-09-17 | `0baf49ee7c93` | Sarah Rudder <sarah.rudder@gsa.gov> | chore: usability improvements to reports | 10 | 108 | 37 | No |
| 2024-09-13 | `e60ad4dcb570` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Upgrade admin and app to USWDS V3 | 145 | 1855 | 4603 | No |
| 2024-09-13 | `70036d977a75` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Upgrade admin and app to USWDS V3 | 53 | 3159 | 1775 | No |
| 2024-09-09 | `76561cf2f032` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4594 from cloud-gov/fix-builds-polling-to-visibilityState-4591 | 1 | 1 | 1 | No |
| 2024-09-09 | `1653c63fd5ba` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Site builds polling to use doc visibilityState #4591 | 1 | 1 | 1 | No |
| 2024-09-04 | `dffa594fec70` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4556 from cloud-gov/release | 2 | 29 | 1 | No |
| 2024-09-03 | `83496e0e3619` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4587 from cloud-gov/feat-autorefresh-site-builds-status-updates | 21 | 23883 | 189 | No |
| 2024-08-30 | `47c4e9ef19e4` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Auto refresh site builds statuses | 8 | 75 | 183 | No |
| 2024-08-30 | `65e8d0d035b4` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Improve build task dev experience | 14 | 23809 | 7 | No |
| 2024-08-28 | `f0ec1772f552` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4582 from cloud-gov/feat-admin-site-build-task-config-ui | 17 | 225 | 28 | No |
| 2024-08-28 | `405082cb1e6c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Upgrade dependency axios to v1.7.5 | 4 | 7 | 7 | No |
| 2024-08-28 | `49f62f5d06fa` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(admin): Add edit functionality to site build task run day | 7 | 144 | 9 | No |
| 2024-08-27 | `f28c717a150d` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: API should only update a site build tasks metadata rules | 3 | 8 | 3 | No |
| 2024-08-27 | `9a9f7cb9a576` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(admin): Add runDay input to manage build tasks | 9 | 69 | 12 | No |
| 2024-08-26 | `e5fa2cb8feea` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4580 from cloud-gov/fix-build-task-report-api-error-logging | 1 | 4 | 8 | No |
| 2024-08-26 | `2bdff7f8948f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: API build tasks report logging | 1 | 4 | 8 | No |
| 2024-08-22 | `413022f3080e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4577 from cloud-gov/feat-add-in-app-reporting | 73 | 3586 | 1570 | No |
| 2024-08-21 | `a2b73d67794e` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add in app report rendering | 73 | 3579 | 1570 | No |
| 2024-07-18 | `fd320f93af83` | Andrew Burnes <andrew.burnes@gsa.gov> | Add initial report rendering | 16 | 210 | 172 | No |
| 2024-07-11 | `ce75d04fe444` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4544 from cloud-gov/release | 2 | 12 | 1 | No |
| 2024-07-03 | `750c48c6fc06` | Andrew Burnes <andrew.burnes@gsa.gov> | init commit | 10 | 285 | 34 | No |
| 2024-06-18 | `21406d0637d5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4520 from cloud-gov/release | 2 | 21 | 1 | No |
| 2024-06-17 | `efead7ea2fba` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4537 from cloud-gov/chore-pipeline-fix | 3 | 145 | 133 | No |
| 2024-06-17 | `f03bd80d7cc4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4533 from cloud-gov/fix-site-build-encryption-to-set-param-keys | 4 | 138 | 24 | No |
| 2024-06-17 | `80c8e82e420a` | Drew Bollinger <drew.bollinger@gsa.gov> | chore(ci): Add necessary pipeline OCI image resources to staging and prod | 3 | 145 | 133 | No |
| 2024-06-13 | `c0290556a068` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Only encrypt site build param values based on defined keys | 4 | 138 | 24 | Yes |
| 2024-05-28 | `297bdc137120` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4519 from cloud-gov/chore-encrypt-build-task-task-params | 3 | 104 | 2 | No |
| 2024-05-21 | `83d143c2665a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4517 from cloud-gov/chore-update-release-script | 1 | 7 | 6 | No |
| 2024-05-21 | `6e59a85a845a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Encrypt build task CF task param values #4509 | 3 | 104 | 2 | No |
| 2024-05-20 | `5bee0c1535ce` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4514 from cloud-gov/chore-increase-prod-queue-concurrencies | 2 | 4 | 4 | No |
| 2024-05-20 | `8fb4253fd600` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Increase prod queue concurrencies to max 10 | 2 | 4 | 4 | No |
| 2024-05-15 | `a1dd49b9155b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4513 from cloud-gov/chore-decommission-pages-builder | 3 | 0 | 28 | No |
| 2024-05-15 | `b5d5a60176a3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4505 from cloud-gov/chore-encrypt-site-build-params | 9 | 72 | 29 | No |
| 2024-05-15 | `bd4c0f395cb9` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove decommissioned site build queue related to pages-builder | 3 | 0 | 28 | No |
| 2024-05-14 | `b414ba987c8c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4508 from cloud-gov/release | 2 | 7 | 1 | No |
| 2024-05-14 | `b64dcd486eb5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4494 from cloud-gov/release | 2 | 20 | 1 | No |
| 2024-05-10 | `f5ddd0227cb7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Encrypt site build params #4464 | 9 | 72 | 29 | No |
| 2024-05-08 | `6a31ae26ebd4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4502 from cloud-gov/chore-docs-queue-development | 1 | 8 | 2 | No |
| 2024-05-08 | `66304732522f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4497 from cloud-gov/chore-refactor-build-task-job-processor | 42 | 520 | 589 | No |
| 2024-05-08 | `87aebd90c151` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(docs): Add documentation for working with and creating queues | 1 | 8 | 2 | No |
| 2024-04-30 | `5dc547cf44b8` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor build task queue job processor | 42 | 520 | 589 | No |
| 2024-04-26 | `d201900b126f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4493 from cloud-gov/feat-refactor-site-builds-queue | 28 | 987 | 143 | No |
| 2024-04-23 | `1b3eb84052e2` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor site build queue and worker | 28 | 987 | 143 | No |
| 2024-04-17 | `1b08851eae1a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4478 from cloud-gov/feat/update-build-scan-rollups-4446 | 15 | 402 | 157 | No |
| 2024-04-16 | `b05d585f2c28` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4482 from cloud-gov/feat-add-concurrency-to-build-task-worker | 15 | 2112 | 1632 | No |
| 2024-04-10 | `ef89c4388b4c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add concurrency and polling to build task queue worker | 15 | 2112 | 1632 | No |
| 2024-04-10 | `edda204f52e0` | Sarah Rudder <sarah.rudder@gsa.gov> | feat: Revamp build scan display per #4446 | 15 | 402 | 157 | No |
| 2024-04-02 | `8bcbc245492e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4442 from cloud-gov/docs-define-frontend-conventions | 1 | 57 | 0 | No |
| 2024-04-02 | `2cf62b647f66` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4444 from cloud-gov/fix-old-build-log-fetch-error | 3 | 43 | 15 | No |
| 2024-04-01 | `ec9eef94aead` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Fetch error for old build logs based on build details | 3 | 43 | 15 | No |
| 2024-03-29 | `f958d7469ec4` | Andrew Burnes <andrew.burnes@gsa.gov> | docs: Add frontend conventions to DEVELOPMENT.md | 1 | 57 | 0 | No |
| 2024-03-19 | `d94c39ed2ad2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4420 from cloud-gov/chore-update-deps-remove-deprectated-gh-auth | 25 | 2088 | 2343 | No |
| 2024-03-15 | `3bdfefce23d5` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update passport deps and remove deprecated GH auth | 25 | 2088 | 2343 | No |
| 2024-03-11 | `352c9b3f74d7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4412 from cloud-gov/feat-customize-invite-email-by-origin-4370 | 28 | 125 | 419 | No |
| 2024-03-07 | `a39e52c02aab` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Update email invites based on user UAA origin #4370 | 28 | 125 | 419 | No |
| 2024-02-16 | `3247e99a21a3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4383 from cloud-gov/update-resources | 7 | 437 | 581 | No |
| 2024-02-12 | `84182d9ac38e` | Sven Aas <sven.aas@gsa.gov> | chore: Update resource types to use hardened images | 7 | 437 | 581 | No |
| 2024-01-22 | `73e9ccbf6d6b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4376 from cloud-gov/feat-remove-gh-user-from-invite-4369 | 10 | 1550 | 1450 | No |
| 2024-01-22 | `3474fe9f0c6f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4374 from cloud-gov/feat-add-invite-flowchart | 4 | 190 | 2 | No |
| 2024-01-22 | `8c3b7ec8ead9` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Simplify add org member form | 2 | 30 | 31 | No |
| 2024-01-22 | `a3aaa97a931d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Remove Github username from invite #4369 | 9 | 1520 | 1419 | No |
| 2024-01-19 | `4dd170d0681d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(ops): Add invite flowchart to docs | 4 | 190 | 2 | No |
| 2024-01-11 | `8501ae612ed8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4358 from cloud-gov/fix-ci-remove-erroneous-container-params | 2 | 0 | 2 | No |
| 2024-01-11 | `7a491cecc187` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Remove erroneous container params in stage/prod | 2 | 0 | 2 | No |
| 2024-01-11 | `ad7e78063b3a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4355 from cloud-gov/fix-ci-rework-db-migrations-task | 6 | 122 | 19 | No |
| 2024-01-10 | `5293be4a3e62` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Run db migrations in CI task container with SSL #4354 | 6 | 122 | 19 | Yes |
| 2023-12-21 | `415dc9d62f3c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4347 from cloud-gov/release | 2 | 7 | 1 | No |
| 2023-12-21 | `a86cfc791ed4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4346 from cloud-gov/chore-fix-build-task-feature-flag | 1 | 1 | 1 | No |
| 2023-12-20 | `80104e28d63c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Fix build task feature flag | 1 | 1 | 1 | No |
| 2023-12-20 | `ce44ad54947e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4341 from cloud-gov/chore-switch-commit-summary-state | 9 | 71 | 212 | No |
| 2023-12-19 | `21e5ec13be00` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update CommitSummary commponent data fetch to useState | 9 | 71 | 212 | No |
| 2023-12-19 | `27860d35ecd8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4340 from cloud-gov/fix-site-build-in-progress-load | 1 | 4 | 0 | No |
| 2023-12-19 | `739ceab78679` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Check buildShaLink args if null on site build logs page | 1 | 4 | 0 | No |
| 2023-12-18 | `605f0c1bec7c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4331 from cloud-gov/chore-upgrade-pg-version | 5 | 8 | 11 | No |
| 2023-12-14 | `b833f8dc3e8f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Upgrade local and CI to Postgres v15 | 5 | 8 | 11 | No |
| 2023-11-29 | `2806a0ba9764` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4315 from cloud-gov/fix-add-queue-for-builds | 3 | 6 | 3 | No |
| 2023-11-28 | `6c38708bb3b3` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add queue name for site build and build task  queues | 3 | 6 | 3 | No |
| 2023-11-28 | `0f7fecdcf37b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4314 from cloud-gov/chore-remove-bull-dep | 10 | 542 | 25293 | No |
| 2023-11-28 | `8d8dc1c96f9a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove bull to complete bullmq transition | 10 | 542 | 25293 | No |
| 2023-11-27 | `b8948f00dff1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4309 from cloud-gov/upgrade-major-deps-audit | 7 | 27009 | 3637 | No |
| 2023-11-22 | `6ba12a015779` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: upgrade major deps from audit | 7 | 27009 | 3637 | No |
| 2023-11-16 | `1c55b3ce7c3c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4302 from cloud-gov/chore-limit-branch-length-885 | 8 | 75 | 23 | No |
| 2023-11-16 | `00a2aa4e624f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add length limit validation before branch name regex | 8 | 75 | 23 | No |
| 2023-11-15 | `a15fa7d054ef` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4300 from cloud-gov/fix-ci-staging-audit | 1 | 1 | 1 | No |
| 2023-11-15 | `4bbba287735d` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Update ci staging audit src | 1 | 1 | 1 | No |
| 2023-11-15 | `8075829c696c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4290 from cloud-gov/feat-auto-rotate-bucket-keys-153 | 25 | 602 | 39 | No |
| 2023-10-27 | `34ee66cf1f64` | Andrew Burnes <apburnes@gmail.com> | feat: Auto rotate site bucket keys #153 | 25 | 602 | 39 | No |
| 2023-10-19 | `6531dcc63e3f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4276 from cloud-gov/release | 2 | 7 | 1 | No |
| 2023-10-19 | `f1a2dfc89279` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4275 from cloud-gov/fix-domain-check-provision-status | 2 | 5 | 5 | No |
| 2023-10-19 | `ab4e7f865f93` | Andrew Burnes <apburnes@gmail.com> | fix: Fixes domain checkProvisionStatus with new CF api response | 2 | 5 | 5 | No |
| 2023-10-18 | `27be91e7406d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4274 from cloud-gov/release | 2 | 7 | 1 | No |
| 2023-10-17 | `ca9318094ad8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4273 from cloud-gov/chore-site-repo-migrate-docs | 1 | 11 | 1 | No |
| 2023-10-17 | `5fb6f8e4f95c` | Andrew Burnes <apburnes@gmail.com> | chore: Refine site repo migration docs | 1 | 11 | 1 | No |
| 2023-10-17 | `90bc1930c7bb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4271 from cloud-gov/feat-admin-site-repo-migrator-4237 | 7 | 261 | 5 | No |
| 2023-10-12 | `0fe0c2cc7d1c` | Andrew Burnes <apburnes@gmail.com> | feat(admin): Add site repo migrator script | 7 | 261 | 5 | No |
| 2023-10-04 | `9282d2f306ab` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4257 from cloud-gov/chore-update-deps-4249 | 14 | 3741 | 2376 | No |
| 2023-09-29 | `516c8bacff25` | Andrew Burnes <apburnes@gmail.com> | chore: Update deps using json5 #4249 | 14 | 3741 | 2376 | No |
| 2023-09-28 | `e7e1feb80b62` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4252 from cloud-gov/chore-update-cf-api-endpoints-4112 | 14 | 1324 | 1216 | No |
| 2023-09-21 | `f1d728734a5e` | Andrew Burnes <apburnes@gmail.com> | chore: Update CF API to V3 #4112 | 14 | 1324 | 1216 | No |
| 2023-09-05 | `5a7fceccf39d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4244 from cloud-gov/feat-branch-config-domain-creation-4176 | 18 | 2170 | 254 | No |
| 2023-08-30 | `58cffe8f0183` | Andrew Burnes <apburnes@gmail.com> | feat: Allow users to create custom domains to prepare launch | 18 | 2170 | 254 | No |
| 2023-08-28 | `cfe359a5a739` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4240 from cloud-gov/fix-admin-ui-components-4236 | 5 | 114 | 41 | No |
| 2023-08-24 | `3e4314e0cca2` | Andrew Burnes <apburnes@gmail.com> | fix: Admin UI for updated site branch configs and domains | 5 | 114 | 41 | No |
| 2023-08-22 | `163dcf63e9e0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4239 from cloud-gov/release | 2 | 7 | 1 | No |
| 2023-08-22 | `a3fb0a05d088` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4238 from cloud-gov/perf-scale-up-pages-production-app | 1 | 2 | 2 | No |
| 2023-08-22 | `3dafe472282e` | Andrew Burnes <apburnes@gmail.com> | perf: Update pages production app to 4 instance with 512mb | 1 | 2 | 2 | No |
| 2023-08-15 | `20d6760c04e0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4234 from cloud-gov/fix-site-serializer-picks | 2 | 50 | 3 | No |
| 2023-08-15 | `0da7f7ae113a` | Andrew Burnes <apburnes@gmail.com> | fix: Site serializer domain and branch config pick | 2 | 50 | 3 | No |
| 2023-08-15 | `e4181cfd9f8d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4232 from cloud-gov/fix-site-live-domain-url-4032 | 23 | 216 | 494 | No |
| 2023-08-14 | `a420388df9fb` | Andrew Burnes <apburnes@gmail.com> | fix: Fixed branchViewLink to use branch config and domain model #4032 | 23 | 216 | 494 | No |
| 2023-08-14 | `3f0036fc36b0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4224 from cloud-gov/chore-add-site-branch-config-association-to-domain-4199 | 35 | 2100 | 846 | No |
| 2023-07-31 | `7417e38b5437` | Andrew Burnes <apburnes@gmail.com> | feat: Added site custom domains page \| Updated domain model and admin \| #4199 | 35 | 2100 | 846 | Yes |
| 2023-07-26 | `cded05aea47f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4207 from cloud-gov/chore-add-nightly-build-queue-to-bull-board | 1 | 2 | 0 | No |
| 2023-07-26 | `b855d92a7b06` | Andrew Burnes <apburnes@gmail.com> | chore: Add nightly builds queue to bull board #4198 | 1 | 2 | 0 | No |
| 2023-07-26 | `9a8f20d423c8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4206 from cloud-gov/chore-update-nightly-build-logic-4198 | 8 | 136 | 101 | No |
| 2023-07-25 | `ff160592a898` | Andrew Burnes <apburnes@gmail.com> | chore: Update nightly builds queue query #4198 | 8 | 136 | 101 | No |
| 2023-07-24 | `f81dea19ab77` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4192 from cloud-gov/feat-add-site-branch-config | 50 | 4612 | 1611 | No |
| 2023-06-09 | `8032a3be43b9` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Restructure site model with site branch config relation | 50 | 4612 | 1611 | Yes |
| 2023-05-15 | `4e02ada78a4c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4143 from cloud-gov/staging | 38 | 427 | 715 | No |
| 2023-05-10 | `f54ff10ca060` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4138 from cloud-gov/feat-add-fail-stuck-builds-queue | 11 | 245 | 16 | No |
| 2023-05-10 | `9cbf56efde64` | Andrew Burnes <andrew.burnes@gsa.gov> | Add return values to fail build queue job processor | 1 | 9 | 4 | No |
| 2023-05-10 | `7d82d1118a07` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix logic in fail stuck builds queue logging | 1 | 3 | 3 | No |
| 2023-05-10 | `e3765616b3f3` | Andrew Burnes <andrew.burnes@gsa.gov> | Add queues to bull board | 1 | 4 | 0 | No |
| 2023-05-09 | `f8c32aca6cac` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add fail stuck builds queue and breakout timeout builds queue | 10 | 236 | 16 | No |
| 2023-05-04 | `04448e585ccf` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4131 from cloud-gov/chore-remove-federalist-users-helper-3718 | 15 | 47 | 684 | No |
| 2023-05-04 | `f54f71370fa5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into chore-remove-federalist-users-helper-3718 | 13 | 131 | 13 | No |
| 2023-05-04 | `44e97b452dff` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove UsersHelpers since all admin functions should be on admin routes | 6 | 46 | 205 | No |
| 2023-05-03 | `90a22545ab4f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove deprecated federalistUsersHelpers function | 15 | 21 | 499 | No |
| 2023-05-03 | `8a5dbf0d245a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4126 from cloud-gov/staging | 11 | 39 | 23 | No |
| 2023-04-26 | `911a0b70a142` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4124 from cloud-gov/chore-remove-jekyll-template-4100 | 4 | 8 | 18 | No |
| 2023-04-25 | `90914823b4db` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into chore-remove-jekyll-template-4100 | 1 | 7 | 1 | No |
| 2023-04-25 | `fa6ae2be81d7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove Jekyll template from core | 4 | 8 | 18 | No |
| 2023-04-20 | `e1a0be295ab8` | Andrew Burnes <andrew.burnes@gsa.gov> | Update tests and remove event in GitHubHelpers | 2 | 1 | 4 | No |
| 2023-04-19 | `50df6ca48967` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4116 from cloud-gov/staging | 16 | 616 | 15 | No |
| 2023-04-19 | `a0e1f5404e1a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4115 from cloud-gov/feat-add-site-webhooks-function-to-admin | 9 | 133 | 2 | No |
| 2023-04-19 | `79e2469595a3` | Andrew Burnes <andrew.burnes@gsa.gov> | Add hook id to webhooks table | 1 | 4 | 1 | No |
| 2023-04-19 | `d8a20afd4398` | Andrew Burnes <andrew.burnes@gsa.gov> | Return empty array when webhook response is null | 1 | 1 | 1 | No |
| 2023-04-18 | `1fea6e692d4c` | Andrew Burnes <andrew.burnes@gsa.gov> | Improve create webhook response handling | 4 | 6 | 7 | No |
| 2023-04-18 | `901465ddc7eb` | Andrew Burnes <andrew.burnes@gsa.gov> | Add hooks to SiteFormWebhook component | 1 | 1 | 1 | No |
| 2023-04-18 | `534a3d81f6f3` | Andrew Burnes <andrew.burnes@gsa.gov> | Format webhook info | 1 | 23 | 4 | No |
| 2023-04-18 | `29f9b6d81480` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site webhook functions to admin UI | 8 | 111 | 1 | No |
| 2023-04-17 | `95bf1067e3be` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4114 from cloud-gov/ci-verify-commit-gpg-key | 2 | 2 | 0 | No |
| 2023-04-17 | `baf560d8e995` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4107 from cloud-gov/feat-add-pr-dev-deployment | 6 | 481 | 13 | No |
| 2023-04-17 | `a97e5c4a89ab` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into feat-add-pr-dev-deployment | 2 | 2 | 2 | No |
| 2023-04-17 | `a79798010bec` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 2 | 2 | 0 | No |
| 2023-04-14 | `04a003265801` | Andrew Burnes <andrew.burnes@gsa.gov> | Update GH local Oauth client README | 1 | 1 | 1 | No |
| 2023-04-13 | `bfa467e59ac5` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove GH PR status updates since the staging pipeline does this already | 1 | 0 | 46 | No |
| 2023-04-13 | `5ffa85b99122` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to use staging UAA | 1 | 2 | 2 | No |
| 2023-04-13 | `1655cd1e8386` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4111 from cloud-gov/staging | 2 | 2 | 2 | No |
| 2023-04-13 | `ae0f496ada43` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4110 from cloud-gov/fix-s3-service-plans-request | 2 | 2 | 2 | No |
| 2023-04-12 | `1978390691ed` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Increase cf service plans results to fix S3 request | 2 | 2 | 2 | No |
| 2023-04-11 | `a67989626155` | Andrew Burnes <andrew.burnes@gsa.gov> | Add dev env in deployment docs of README | 1 | 1 | 1 | No |
| 2023-04-11 | `375109112730` | Andrew Burnes <andrew.burnes@gsa.gov> | add docs to README | 1 | 23 | 7 | No |
| 2023-04-11 | `03f2c71c6974` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove depth param for PR resource | 1 | 0 | 5 | No |
| 2023-04-11 | `cfe1cd25fe49` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add dev deployment env for PRs to staging | 5 | 507 | 4 | No |
| 2023-04-05 | `354f84441db3` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix bull board linting | 1 | 2 | 7 | No |
| 2023-04-04 | `9eaab4ccc46f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove federalist references from app | 62 | 140 | 1438 | No |
| 2023-03-22 | `8b8bb6e5f139` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4080 from cloud-gov/feat-switch-to-hardened-container | 3 | 18 | 6 | No |
| 2023-03-22 | `f06130d1adcb` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to hyphens for ecr creds | 3 | 6 | 6 | No |
| 2023-03-21 | `161ce394efc3` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Switch to using harden container for cf-image | 3 | 18 | 6 | No |
| 2023-03-16 | `078cd596a07d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4078 from cloud-gov/feat-enable-org-edit-activation-input | 5 | 86 | 44 | No |
| 2023-03-16 | `1e4cff5e6388` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Enable org status activation in org edit page | 5 | 86 | 44 | No |
| 2023-03-14 | `c890ffdc1067` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4075 from cloud-gov/chore-update-app-stack-cflinuxfs4 | 5 | 7 | 3 | No |
| 2023-03-14 | `28a0a6a4d775` | Andrew Burnes <andrew.burnes@gsa.gov> | update: Parameterize stack with CF_STACK | 5 | 5 | 2 | No |
| 2023-03-13 | `91ed11f1a7fe` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update app stack to cflinuxfs4 | 2 | 4 | 3 | No |
| 2023-01-06 | `9c523aa0aafc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4018 from cloud-gov/staging | 1 | 7 | 1 | No |
| 2022-12-22 | `0460ae7cd1a2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4010 from cloud-gov/fix-env-vars-org-query-4007 | 4 | 106 | 52 | No |
| 2022-12-21 | `e84e98295d0f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into fix-env-vars-org-query-4007 | 2 | 30 | 31 | No |
| 2022-12-21 | `72db9e5039d7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4006 from cloud-gov/chore-move-scheduled-jobs-3991 | 1 | 29 | 30 | No |
| 2022-12-21 | `980222c72c44` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Removes scope from UEV model in favor of Site scope forUser | 4 | 106 | 52 | No |
| 2022-12-21 | `d38f11e8805c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Move relevant worker tasks from Federalist to Pages app | 1 | 29 | 30 | No |
| 2022-12-20 | `1cbc4192dcff` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4003 from cloud-gov/feat-add-auth-event-logging-3987 | 9 | 77 | 13 | No |
| 2022-12-20 | `c5f33b4745d1` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch external auth tests to stub events to run tests consistently | 2 | 16 | 32 | No |
| 2022-12-20 | `b9b0d67a7990` | Andrew Burnes <andrew.burnes@gsa.gov> | Move event audits for UAA auth into uaaVerify service | 3 | 33 | 9 | No |
| 2022-12-19 | `588222b9ba96` | Andrew Burnes <andrew.burnes@gsa.gov> | Rework auth event test support to delete event instance from db | 2 | 14 | 13 | No |
| 2022-12-19 | `ff152e3e198a` | Andrew Burnes <andrew.burnes@gsa.gov> | Put before/after each hooks at top of external auth test | 1 | 3 | 6 | No |
| 2022-12-19 | `16518fbe271f` | Andrew Burnes <andrew.burnes@gsa.gov> | Add additional event logging around authentication | 8 | 70 | 12 | Yes |
| 2022-12-07 | `dbf05b9dff50` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3992 from cloud-gov/fix-admin-build-logs-response | 4 | 74 | 10 | No |
| 2022-12-07 | `8c493de1cb0c` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Admin API build logs response | 4 | 74 | 10 | No |
| 2022-12-06 | `512d632b54e7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3988 from cloud-gov/staging | 60 | 3026 | 4203 | No |
| 2022-12-06 | `3e0bd6b0f125` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3986 from cloud-gov/fix-get-s3-build-logs | 5 | 36 | 20 | No |
| 2022-12-05 | `b4520da063db` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Fixes the offest queries when return logs from s3 | 5 | 36 | 20 | No |
| 2022-12-05 | `6240efeeac74` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3982 from cloud-gov/feat-improve-build-logs-2474 | 60 | 3003 | 4196 | No |
| 2022-12-05 | `805384ed6d92` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: refine auto scroll based on build state | 4 | 20 | 9 | No |
| 2022-12-05 | `4e73cab1bc8b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into feat-improve-build-logs-2474 | 1 | 3 | 1 | No |
| 2022-12-01 | `1138e8dc33eb` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add auto scroll to build logs table | 5 | 43 | 19 | No |
| 2022-12-01 | `aa5a6159d582` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into feat-improve-build-logs-2474 | 3 | 37 | 2 | No |
| 2022-11-30 | `2095df10ae6e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update CI node version 18 | 6 | 8 | 8 | No |
| 2022-11-30 | `331315225e48` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Move site build logs to react hooks | 46 | 10607 | 11744 | No |
| 2022-11-23 | `53eba757665d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Update build logs reducer and remove refresh logs button | 20 | 10387 | 10688 | No |
| 2022-10-05 | `8d49e0fbb09c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3946 from cloud-gov/staging | 4 | 18 | 6 | No |
| 2022-10-04 | `ed9f9f54c651` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3944 from cloud-gov/chore-update-11ty-template-uswds-version | 2 | 5 | 5 | No |
| 2022-10-03 | `75ddadf3aee8` | Andrew Burnes <andrew.burnes@gsa.gov> | Update config/templates.js | 1 | 1 | 1 | No |
| 2022-09-30 | `ca6d2a173c83` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update template urls to custom domains and 11ty thumbnail | 2 | 4 | 4 | No |
| 2022-09-30 | `624f057041d7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update 11ty template metadata to current USWDS version | 1 | 4 | 4 | No |
| 2022-09-13 | `cc25a5da0850` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3931 from cloud-gov/fix-admin-client-css | 1 | 1 | 1 | No |
| 2022-09-13 | `e7629d20685e` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: update admin client rollup config to properly output custom css | 1 | 1 | 1 | No |
| 2022-09-12 | `d2033ff71f8e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3925 from cloud-gov/staging | 17 | 211 | 311 | No |
| 2022-09-12 | `4ddbba53eb28` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3926 from cloud-gov/chore-audit-fix-deps-20220908 | 3 | 204 | 151 | No |
| 2022-09-08 | `fa190025ff2b` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: update rollup-plugin-svelte v6.1.1 for admin client | 2 | 5 | 5 | No |
| 2022-09-08 | `d4882c886c02` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Run yarn-audit-fix for core and admin client | 2 | 200 | 147 | No |
| 2022-09-08 | `3dbdc3aa88c8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3924 from cloud-gov/fix-uaa-origin-for-group-add-member | 3 | 5 | 6 | No |
| 2022-09-08 | `d9dd0e6d7881` | Andrew Burnes <andrew.burnes@gsa.gov> | Set origin to uaa for add member POST request to pages.user | 3 | 5 | 6 | No |
| 2022-09-06 | `6f2e37d51727` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3921 from cloud-gov/fix-uaa-scope-and-site-forUsers | 6 | 38 | 21 | No |
| 2022-09-06 | `b42e655b0f79` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: uaa scope on user invite and Site.forUser filter | 6 | 38 | 21 | No |
| 2022-09-01 | `c8124719209e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3920 from cloud-gov/staging | 9 | 105 | 37 | No |
| 2022-08-31 | `502605f13ca4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3917 from cloud-gov/feat-admin-add-site-to-org-3916 | 8 | 91 | 20 | No |
| 2022-08-31 | `80b5be82930e` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add empty default if no org for site and spell check organization | 2 | 3 | 3 | No |
| 2022-08-30 | `c0bdf4b4cd25` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Allow admins to add site to an org | 8 | 91 | 20 | No |
| 2022-08-30 | `b21e234aa1b1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3914 from cloud-gov/staging | 1 | 2 | 2 | No |
| 2022-08-29 | `03431b7c4967` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3913 from cloud-gov/fix-redis-config-for-federalist | 1 | 2 | 2 | No |
| 2022-08-29 | `4426ef8ca3b3` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update redis config on production to fix federalist prod | 1 | 2 | 2 | No |
| 2022-08-29 | `66cc08e6703c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3912 from cloud-gov/staging | 2 | 2 | 2 | No |
| 2022-08-29 | `76825ebbe972` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3911 from cloud-gov/ci-federalist-prod-to-bull-queue-2091 | 2 | 2 | 2 | No |
| 2022-08-29 | `080bf87c3e2c` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Switch build queue for federalist prod to bull | 2 | 2 | 2 | No |
| 2022-08-25 | `5af36e9dce83` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3906 from cloud-gov/staging | 10 | 280 | 137 | No |
| 2022-08-25 | `e9adfa244e6b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3908 from cloud-gov/fix-new-site-builds-for-pages | 2 | 226 | 103 | No |
| 2022-08-25 | `40827a940f93` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: linting error | 1 | 1 | 1 | No |
| 2022-08-25 | `b75cdcfff4c2` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: allows pages to create new sites without mapping routes | 2 | 226 | 103 | No |
| 2022-08-24 | `86310eb6f215` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3907 from cloud-gov/ci-pages-admin-prod-2114 | 2 | 16 | 15 | No |
| 2022-08-24 | `016b888b486c` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: add pages-production vars for ci deployment | 2 | 16 | 15 | No |
| 2022-08-23 | `9b6e3d6b3f6e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3904 from cloud-gov/apb/add-11ty-template | 7 | 38 | 19 | No |
| 2022-08-23 | `ad75bc615cba` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove unused images for federalist site templates | 2 | 0 | 0 | No |
| 2022-08-23 | `fd52a518a1a8` | Andrew Burnes <andrew.burnes@gsa.gov> | Update conf site templates and their tests | 6 | 29 | 21 | No |
| 2022-08-23 | `e15050b0414e` | Andrew Burnes <andrew.burnes@gsa.gov> | Lintz | 1 | 1 | 1 | No |
| 2022-08-23 | `373181f6ad43` | Andrew Burnes <andrew.burnes@gsa.gov> | Add 11ty template to options | 2 | 13 | 2 | No |
| 2022-08-22 | `d0936023f33e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3903 from 18F/staging | 3 | 5 | 16 | No |
| 2022-08-19 | `5d31f2115a7b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3902 from 18F/apb/add-var-login-to-prod-deploy | 3 | 5 | 16 | No |
| 2022-08-19 | `8936a97f8e7e` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove load and tagging of test docker images | 2 | 0 | 16 | No |
| 2022-08-19 | `7b22fea0c837` | Andrew Burnes <andrew.burnes@gsa.gov> | Add some additionaly netowork pruning for ci tests running in docker | 2 | 4 | 0 | No |
| 2022-08-19 | `43c58a4e0442` | Andrew Burnes <andrew.burnes@gsa.gov> | Add uaa_login_host to production deploy vars | 1 | 1 | 0 | No |
| 2022-08-19 | `53615a3dad5d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3901 from 18F/staging | 22 | 958 | 698 | No |
| 2022-08-19 | `00c165dd3a91` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3899 from 18F/apb/federalist-prod-concourse-2088 | 13 | 623 | 449 | No |
| 2022-08-19 | `7900691cbbd7` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up pr status naming in staging pages pipeline | 1 | 7 | 7 | No |
| 2022-08-19 | `0cf6d3fea341` | Andrew Burnes <andrew.burnes@gsa.gov> | Cleanup pipeline tasks names | 1 | 8 | 8 | No |
| 2022-08-16 | `fa74407587aa` | Andrew Burnes <andrew.burnes@gsa.gov> | Update uaa login and redis queue for staging | 6 | 45 | 44 | No |
| 2022-08-11 | `429d018035cc` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove code climate | 3 | 1 | 33 | No |
| 2022-08-11 | `d36b9dc221f9` | Andrew Burnes <andrew.burnes@gsa.gov> | Move federalist-prod deploys to concourse and remove circleci | 4 | 570 | 365 | No |
| 2022-08-11 | `3d6984bcbb79` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3898 from 18F/apb/staging-queues-ui-2088 | 5 | 75 | 69 | No |
| 2022-08-10 | `e1e47b785d65` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix the lints | 1 | 15 | 12 | No |
| 2022-08-10 | `34c5032af088` | Andrew Burnes <andrew.burnes@gsa.gov> | Bump up memory for staging to 256MB to testing purposes | 1 | 1 | 1 | No |
| 2022-08-09 | `0cd20f701819` | Andrew Burnes <andrew.burnes@gsa.gov> | Add logic for product auth strategy | 2 | 19 | 15 | No |
| 2022-08-09 | `6251b2d95c30` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial commit with staging deployment | 2 | 61 | 62 | No |
| 2022-08-09 | `3c2aedec5f46` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3897 from 18F/apb/fix-metrics-node-version-2088 | 1 | 4 | 2 | No |
| 2022-08-09 | `f2fc18d0e746` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix metrics node version for ci tests and require set-pipeline for tasks | 1 | 4 | 2 | No |
| 2022-08-09 | `9803c48cfa68` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3894 from 18F/apb/staging-concourse-ci-2088 | 5 | 254 | 170 | No |
| 2022-08-09 | `781c3e58048a` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove CircleCI for staging and update staging pipeline for core and metrics | 4 | 31 | 63 | No |
| 2022-08-09 | `0bc3ad0fea31` | Andrew Burnes <andrew.burnes@gsa.gov> | Add metrics pipeline deployment and update README | 3 | 102 | 38 | No |
| 2022-08-04 | `d2b50eddc209` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/staging-concourse-ci-2088 | 6 | 19 | 15 | No |
| 2022-08-02 | `a7d82a54412c` | Andrew Burnes <andrew.burnes@gsa.gov> | Update set-pipeline task with instance vars | 1 | 14 | 8 | No |
| 2022-08-01 | `1cacfebb9a2a` | Andrew Burnes <andrew.burnes@gsa.gov> | Update README with CI vars | 1 | 19 | 1 | No |
| 2022-07-27 | `2eb32261a605` | Andrew Burnes <andrew.burnes@gsa.gov> | Add initial pipeline updates and readme | 2 | 99 | 71 | No |
| 2022-06-30 | `911745c34af3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3890 from 18F/pburkholder-patch-1 | 1 | 0 | 10 | No |
| 2022-05-26 | `9d318da0f27d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3849 from 18F/apb/add-codeql | 1 | 38 | 0 | No |
| 2022-05-04 | `53cfa526afd4` | Andrew Burnes <andrew.burnes@gsa.gov> | Add codeql GH action | 1 | 38 | 0 | No |
| 2022-04-27 | `0040d601693d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3844 from 18F/apb/adjust-memory-3833 | 3 | 6 | 6 | No |
| 2022-04-27 | `f3f9fafd0242` | Andrew Burnes <andrew.burnes@gsa.gov> | Adjust memory for apps | 3 | 6 | 6 | No |
| 2022-02-28 | `5c34aed1039f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3798 from 18F/apb/fix-task-exit | 1 | 5 | 1 | No |
| 2022-02-28 | `8d15eb7c476f` | Andrew Burnes <andrew.burnes@gsa.gov> | Explicitly exit task | 1 | 5 | 1 | No |
| 2022-02-25 | `c7596398a092` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3794 from 18F/apb/builds-queued-check-3318 | 3 | 121 | 13 | No |
| 2022-02-25 | `ea99b05f7dfc` | Andrew Burnes <andrew.burnes@gsa.gov> | Only pull the attributes we need - id | 1 | 1 | 0 | No |
| 2022-02-25 | `c0adae1bb87e` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix pipeline spacing | 1 | 28 | 27 | No |
| 2022-02-25 | `f6a88f3b0529` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/builds-queued-check-3318 | 3 | 30 | 12 | No |
| 2022-02-25 | `662ef21b8ed3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge staging | 1 | 121 | 121 | No |
| 2022-02-23 | `9363d3213649` | Andrew Burnes <andrew.burnes@gsa.gov> | Add builds queued check job in concourse ci | 3 | 119 | 13 | No |
| 2022-02-22 | `53a8e7d18bdc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3786 from 18F/apb/create-domain-from-site-3757 | 4 | 58 | 29 | No |
| 2022-02-18 | `604eb42ec356` | Andrew Burnes <andrew.burnes@gsa.gov> | Lint | 3 | 5 | 5 | No |
| 2022-02-18 | `414d4fa29313` | Andrew Burnes <andrew.burnes@gsa.gov> | Add create domain from admin site page | 4 | 59 | 30 | No |
| 2022-01-28 | `b88006cc7d14` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3762 from 18F/peterb/add-nodesecurity | 1 | 3 | 1 | No |
| 2021-12-14 | `da8aaac64360` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3730 from 18F/apb/fix-new-site-tmpl8-3682 | 4 | 40 | 5 | No |
| 2021-12-14 | `e0101eabb589` | Andrew Burnes <andrew.burnes@gsa.gov> | Add sites props to AddSite test | 1 | 7 | 0 | No |
| 2021-12-14 | `d49e94d2f3e5` | Andrew Burnes <andrew.burnes@gsa.gov> | Watch for add site fetching when creating new sites | 3 | 33 | 5 | No |
| 2021-11-29 | `8c9183d0eee2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3711 from 18F/ar/new-operator | 1 | 1 | 1 | No |
| 2021-11-23 | `a9673ebc01fd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3707 from 18F/apb/add-security-considerations | 1 | 11 | 0 | No |
| 2021-11-22 | `07054dd6cb72` | Andrew Burnes <andrew.burnes@gsa.gov> | Add cg sc action | 1 | 11 | 0 | No |
| 2021-08-13 | `78936b6e6924` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3548 from 18F/apb/add-unique-fk-user-id-3482 | 1 | 7 | 0 | No |
| 2021-08-13 | `9de5a9c3af0c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/add-unique-fk-user-id-3482 | 8 | 19 | 44 | No |
| 2021-08-12 | `b68f3b4a3704` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to add/removeIndex method for constraint | 1 | 3 | 6 | No |
| 2021-08-12 | `b2e5d193885c` | Andrew Burnes <andrew.burnes@gsa.gov> | Alter user_id fk to be unique on uaa_identity | 1 | 10 | 0 | No |
| 2021-08-10 | `da3a1bfd7494` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/admin-mgmt-users-3410 | 2 | 18 | 3 | No |
| 2021-08-10 | `415b5200d069` | Andrew Burnes <andrew.burnes@gsa.gov> | Cleanup admin-client linting | 3 | 13 | 9 | No |
| 2021-08-10 | `65b922e090ff` | Andrew Burnes <andrew.burnes@gsa.gov> | Add admin users role mgmt | 13 | 386 | 18 | No |
| 2021-07-16 | `e974d2eed771` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3497 from 18F/apb/fix-live-url-link | 1 | 1 | 1 | No |
| 2021-07-16 | `06583bc7814a` | Andrew Burnes <andrew.burnes@gsa.gov> | Update the live URL link to documentation | 1 | 1 | 1 | No |
| 2021-06-22 | `cb012bc2ffc7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3453 from 18F/apb/ci-docs | 1 | 27 | 0 | No |
| 2021-06-22 | `cf218d859e9d` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial docs on using a jumpbox | 1 | 27 | 0 | No |
| 2021-06-21 | `0101064d9f0c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3437 from 18F/apb/pages-banner | 6 | 64 | 1 | No |
| 2021-06-21 | `cf1c1f88f339` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/pages-banner | 12 | 69 | 15 | No |
| 2021-06-11 | `43d5ff2ec827` | Andrew Burnes <andrew.burnes@gsa.gov> | Add pages announcement banner | 6 | 64 | 1 | No |
| 2021-06-03 | `de111a46a513` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3327 from 18F/apb-uaa-or-github-3316 | 23 | 549 | 332 | No |
| 2021-06-01 | `1fa21d7ff011` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-uaa-or-github-3316 | 1 | 78 | 63 | No |
| 2021-06-01 | `034f02128457` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove unused AUTH_IDP env references | 7 | 1 | 9 | No |
| 2021-05-28 | `f9cee252fd89` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove UAA login precursor text in views/home.njk | 1 | 0 | 3 | No |
| 2021-05-28 | `179f2bf47b8f` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix github login button text views/navigation.njk | 1 | 1 | 1 | No |
| 2021-05-28 | `af685c306af2` | Andrew Burnes <andrew.burnes@gsa.gov> | Update "Use your github..." lang for views/home.njk | 1 | 1 | 1 | No |
| 2021-05-28 | `c397a1747b71` | Andrew Burnes <andrew.burnes@gsa.gov> | Refactor verifyGithub | 1 | 15 | 21 | No |
| 2021-05-28 | `40c854af99b3` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to two feature flags for uaa and github | 13 | 126 | 155 | No |
| 2021-05-28 | `8de510e2454b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge with staging | 2 | 5 | 5 | No |
| 2021-05-28 | `672195e1ee38` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-uaa-or-github-3316 | 6 | 102 | 4 | No |
| 2021-05-28 | `ce3958bfdccd` | Andrew Burnes <andrew.burnes@gsa.gov> | Change github auth to update not upsert user | 2 | 45 | 25 | No |
| 2021-05-27 | `113be277f7fa` | Andrew Burnes <andrew.burnes@gsa.gov> | Use correct user key for onGithubSuccess find by pk | 1 | 1 | 1 | No |
| 2021-05-27 | `581721cc6cd5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge with staging | 62 | 3249 | 3656 | No |
| 2021-05-26 | `727308031af6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge with staging | 63 | 2459 | 685 | Yes |
| 2021-05-12 | `2aa2c39eda05` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3355 from 18F/3353-site-serializer-update | 1 | 7 | 7 | No |
| 2021-05-12 | `6ed203f5aefd` | Andrew Burnes <andrew.burnes@gsa.gov> | Update serializeMany with serializeObject | 1 | 7 | 7 | No |
| 2021-05-11 | `9311a8c0ad6f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3351 from 18F/apb/fix-template-org-select-3350 | 1 | 3 | 3 | No |
| 2021-05-11 | `629a4fcb1f4c` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix template org select | 1 | 3 | 3 | No |
| 2021-05-11 | `bfe53edbdd72` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3346 from 18F/3344-uaa-scope-refactor | 5 | 20 | 21 | No |
| 2021-05-10 | `1dda1a3cb45a` | Andrew Burnes <andrew.burnes@gsa.gov> | Update views/home.njk | 1 | 1 | 1 | No |
| 2021-05-07 | `9997cb4d72c8` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix flash message typo | 1 | 1 | 1 | No |
| 2021-05-07 | `a06001e52569` | Andrew Burnes <andrew.burnes@gsa.gov> | Update api/controllers/main.js message | 1 | 1 | 1 | No |
| 2021-05-07 | `55165645e0c2` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix  .cloudgov/manifest.yml | 1 | 1 | 1 | No |
| 2021-05-06 | `96557e764ed4` | Andrew Burnes <andrew.burnes@gsa.gov> | Add prose for connecting you github account | 4 | 34 | 23 | No |
| 2021-05-04 | `29af31636afa` | Andrew Burnes <andrew.burnes@gsa.gov> | Add hasMultiAuth and alerts to views | 10 | 97 | 31 | No |
| 2021-04-29 | `1c576c9972d7` | Andrew Burnes <andrew.burnes@gsa.gov> | Add multi auth feature to backend | 7 | 467 | 300 | No |
| 2021-04-22 | `334e868d8ff6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3313 from 18F/apb-has-org-3310 | 7 | 335 | 196 | No |
| 2021-04-20 | `08357c8b3f24` | Andrew Burnes <andrew.burnes@gsa.gov> | Rerefactor create authorizor | 1 | 26 | 18 | No |
| 2021-04-20 | `062b7bc8af33` | Andrew Burnes <andrew.burnes@gsa.gov> | Refactor create authorizor | 1 | 15 | 14 | No |
| 2021-04-20 | `fc73016f7ef5` | Andrew Burnes <andrew.burnes@gsa.gov> | Update tests and add additional site create auth logic | 3 | 93 | 65 | No |
| 2021-04-19 | `54a39e8cf167` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-has-org-3310 | 4 | 11 | 8 | No |
| 2021-04-19 | `dd718cf007fe` | Andrew Burnes <andrew.burnes@gsa.gov> | Add authorizer for site creation | 6 | 293 | 191 | No |
| 2021-04-19 | `2cec97a6a17e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3297 from 18F/apb/fix-org-ui-ux | 18 | 349 | 128 | No |
| 2021-04-19 | `346101fa34a3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/fix-org-ui-ux | 2 | 18 | 11 | No |
| 2021-04-19 | `4be449a8559e` | Andrew Burnes <andrew.burnes@gsa.gov> | Breakout validation for AddSiteRepoForm | 3 | 58 | 13 | No |
| 2021-04-16 | `d58e4e79b247` | Andrew Burnes <andrew.burnes@gsa.gov> | Update org element views with hasOrgs and add org select validation | 13 | 211 | 126 | Yes |
| 2021-04-13 | `009f8b014b67` | Andrew Burnes <andrew.burnes@gsa.gov> | Add tests for siteList and siteListItem components | 2 | 46 | 3 | No |
| 2021-04-09 | `4382b0aae449` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up redux state to properly display org info when user has orgs | 8 | 97 | 49 | No |
| 2021-04-08 | `9f71f5027ceb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3284 from 18F/apb/user-org-site-ui | 35 | 897 | 84 | No |
| 2021-04-08 | `54183eb9122c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/user-org-site-ui | 2 | 47 | 21 | No |
| 2021-04-08 | `bca662a49dd7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/user-org-site-ui | 2 | 46 | 39 | No |
| 2021-04-07 | `3a1238e824cc` | Andrew Burnes <andrew.burnes@gsa.gov> | Refactor components for siteList and TemplateSiteList | 2 | 57 | 39 | No |
| 2021-04-06 | `14a312eb2b9d` | Andrew Burnes <andrew.burnes@gsa.gov> | Add additional frontend tests for organizations | 2 | 86 | 1 | No |
| 2021-04-06 | `d3e9c32893ba` | Andrew Burnes <andrew.burnes@gsa.gov> | Used scoped Site.forUser for fetchAllForUser and remove org link in site item | 3 | 9 | 14 | No |
| 2021-04-05 | `51a32413d7b3` | Andrew Burnes <andrew.burnes@gsa.gov> | organizationSerializer.serializeMany is not asynchronous | 1 | 1 | 1 | No |
| 2021-04-05 | `fd729314ac6b` | Andrew Burnes <andrew.burnes@gsa.gov> | Update org filter selection on site page | 13 | 224 | 115 | No |
| 2021-04-02 | `eb7376d3a2ec` | Andrew Burnes <andrew.burnes@gsa.gov> | Add org selection on site creation | 8 | 245 | 18 | No |
| 2021-04-01 | `24e7554274ad` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial sites grouped per organization update | 19 | 403 | 24 | No |
| 2021-03-11 | `1daa42819a56` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3252 from 18F/apb/uaa-verification | 29 | 1098 | 54 | No |
| 2021-03-11 | `706295d58843` | Andrew Burnes <andrew.burnes@gsa.gov> | Update uaa host env variables | 4 | 4 | 4 | No |
| 2021-03-11 | `a09439b78686` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/uaa-verification | 1 | 62 | 62 | No |
| 2021-03-11 | `f40a834dcc98` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/uaa-verification | 14 | 796 | 70 | No |
| 2021-03-11 | `ec5a9cd3c8ba` | Andrew Burnes <andrew.burnes@gsa.gov> | Streamline uaa model and uaaVerify function | 7 | 20 | 15 | No |
| 2021-03-09 | `955363c37c30` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix test nocks | 2 | 5 | 4 | No |
| 2021-03-09 | `44c9ef71c68b` | Andrew Burnes <andrew.burnes@gsa.gov> | Add local uaa for development and clean up uaa user verification | 18 | 338 | 78 | Yes |
| 2021-03-05 | `a692106326fd` | Andrew Burnes <andrew.burnes@gsa.gov> | Add uaa_identity table to support auth | 22 | 825 | 47 | Yes |
| 2021-03-03 | `24855095826b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3248 from 18F/apb/update-uaa-service | 3 | 21 | 13 | No |
| 2021-03-02 | `0f071026065a` | Andrew Burnes <andrew.burnes@gsa.gov> | Update uaa to use new admin and app client creds | 3 | 21 | 13 | No |
| 2021-02-26 | `ccbc2fa11b83` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3241 from 18F/apb/order-site-destroyer | 1 | 2 | 2 | No |
| 2021-02-26 | `2b6c410bae0a` | Andrew Burnes <andrew.burnes@gsa.gov> | Make sure remove S3 is run after bucket contents completely removed | 1 | 2 | 2 | No |
| 2021-02-26 | `b13bc31a0089` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3240 from 18F/apb/fix-queue-redis-url | 3 | 4 | 4 | No |
| 2021-02-26 | `b1490e92a1b1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb/fix-queue-redis-url | 3 | 5 | 2 | No |
| 2021-02-26 | `c629e785c70b` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix uri to url for redis usage | 3 | 4 | 4 | No |
| 2021-02-26 | `069f5e6e9f6d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3239 from 18F/apb/enable_bull_queue | 3 | 5 | 2 | No |
| 2021-02-26 | `9ea6979f6027` | Andrew Burnes <andrew.burnes@gsa.gov> | Turn bull queue feature on for staging | 3 | 5 | 2 | No |
| 2021-02-25 | `c6ccf4fc9156` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3235 from 18F/apb/add-bull-queue | 20 | 446 | 95 | No |
| 2021-02-25 | `55160b559c40` | Andrew Burnes <andrew.burnes@gsa.gov> | Add test for SiteBuildQueue bull client | 2 | 42 | 1 | No |
| 2021-02-25 | `40e586b65aeb` | Andrew Burnes <andrew.burnes@gsa.gov> | Add bull queue client tests | 2 | 69 | 4 | No |
| 2021-02-25 | `d3e0f733418e` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial transition to add bull queue as feature flag for site builds | 18 | 336 | 91 | No |
| 2020-09-17 | `7fc54770ad0a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2916 from 18F/apb-admin-delete-site | 15 | 358 | 83 | No |
| 2020-09-17 | `6a156771746b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-admin-delete-site | 2 | 2 | 2 | No |
| 2020-09-17 | `be6611107512` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-admin-delete-site | 7 | 265 | 202 | No |
| 2020-09-17 | `1eeebf96cffa` | Andrew Burnes <andrew.burnes@gsa.gov> | Refactor site delete into SiteDestroyer service | 11 | 97 | 123 | Yes |
| 2020-09-16 | `3c224eb7dcdb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge with staging | 9 | 77 | 70 | No |
| 2020-09-15 | `1b9876f1359f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-admin-delete-site | 3 | 168 | 137 | No |
| 2020-09-15 | `48bec218f4b8` | Andrew Burnes <andrew.burnes@gsa.gov> | Add admin delete site route | 4 | 158 | 19 | No |
| 2020-09-15 | `e9c1271eea93` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apb-admin-delete-site | 10 | 90 | 54 | No |
| 2020-09-10 | `ed37851ecba1` | Andrew Burnes <andrew.burnes@gsa.gov> | UI added to admin site page to delete site | 5 | 164 | 3 | No |
| 2020-08-18 | `c3593b0062aa` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2842 from 18F/admin-site-page | 22 | 354 | 66 | No |
| 2020-08-18 | `b81b90ebad52` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into admin-site-page | 1 | 1 | 0 | No |
| 2020-08-17 | `824dfe57113c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into admin-site-page | 60 | 2005 | 227 | No |
| 2020-08-17 | `9f44952849fc` | Andrew Burnes <andrew.burnes@gsa.gov> | Add `signedInAt` to site's users info | 1 | 1 | 0 | No |
| 2020-08-15 | `146eb2d06fcf` | Andrew Burnes <andrew.burnes@gsa.gov> | Add builds to site view and update builds view | 10 | 160 | 39 | No |
| 2020-08-14 | `2797339b2e24` | Andrew Burnes <andrew.burnes@gsa.gov> | Add site page to admin client | 17 | 214 | 48 | No |
| 2020-06-08 | `4612a1caca2b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2685 from 18F/dc/handle-failed-deployment | 1 | 14 | 1 | No |
| 2020-02-26 | `bb8fc3b3ce8d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2500 from 18F/apb-fix-site-links | 4 | 87 | 0 | No |
| 2020-02-25 | `ba24cafc4a48` | Andrew Burnes <andrew.burnes@gsa.gov> | Add site, demo, preview link attributes to site serializer | 4 | 87 | 0 | No |
| 2019-09-13 | `b35308d5ae9d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2334 from 18F/apburnes/fix-route-delete | 3 | 6 | 7 | No |
| 2019-09-12 | `3ca8526466c0` | Andrew Burnes <andrew.burnes@gsa.gov> | Query routes using host filter so no pagination is needed | 3 | 6 | 7 | No |
| 2019-09-10 | `859f7b48efa6` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix lint and test errors | 3 | 13 | 14 | No |
| 2019-09-09 | `16bb1dc9a3dc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2328 from 18F/apburnes/truncate-service-name | 3 | 32 | 4 | No |
| 2019-09-09 | `4bb4020c7893` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/truncate-service-name | 3 | 56 | 5 | No |
| 2019-09-09 | `46bd2ac9c754` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to random string from date appending string | 2 | 15 | 11 | No |
| 2019-09-09 | `1e5e11a49da7` | Andrew Burnes <andrew.burnes@gsa.gov> | Truncate service name generatation for s3 to account for 50 char limit | 3 | 28 | 4 | No |
| 2019-06-06 | `335901b40314` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2278 from 18F/staging | 1 | 1 | 1 | No |
| 2019-06-05 | `cc08f92aa423` | Andrew Burnes <andrew.burnes@gsa.gov> | Increase putBucketWebsite up to 30 times on site creation | 1 | 1 | 1 | No |
| 2019-05-14 | `df9bc0b28ebf` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2259 from 18F/apburnes/add-loading-ui | 3 | 36 | 2 | No |
| 2019-05-14 | `fd62a311a307` | Andrew Burnes <andrew.burnes@gsa.gov> | Render loading component while site is being added or deleted | 3 | 36 | 2 | No |
| 2019-05-13 | `3d9ffe57999a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2254 from 18F/apburnes/update-bucket-website-config | 4 | 14 | 10 | No |
| 2019-05-10 | `54231a06d7e0` | Andrew Burnes <andrew.burnes@gsa.gov> | Change to /404.html | 3 | 3 | 3 | No |
| 2019-05-10 | `4c04fce7076e` | Andrew Burnes <andrew.burnes@gsa.gov> | Update default 404 error config to match garden build | 4 | 14 | 10 | No |
| 2019-05-09 | `4aef57eee689` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove mock for 404 page creation from sendBuildMessage test | 1 | 0 | 9 | No |
| 2019-05-09 | `50897c2faf66` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove not found 404 template | 2 | 0 | 63 | No |
| 2019-05-08 | `ad13260a7dbb` | Andrew Burnes <andrew.burnes@gsa.gov> | Move S3 website config to time of first build | 12 | 310 | 71 | No |
| 2019-05-06 | `2db6c3e82bb2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2248 from 18F/apburnes/add-delay | 3 | 34 | 8 | No |
| 2019-05-06 | `2a975eaacc22` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix code climate | 1 | 5 | 5 | No |
| 2019-05-06 | `8f8a109262bf` | Andrew Burnes <andrew.burnes@gsa.gov> | Add logger for putBucketWebsite requests | 1 | 22 | 3 | No |
| 2019-05-03 | `ef68bef2189c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2247 from 18F/apburnes/bug-retry-website-config | 2 | 33 | 14 | No |
| 2019-05-03 | `249aaec2a77f` | Andrew Burnes <andrew.burnes@gsa.gov> | Code climate fix | 1 | 0 | 1 | No |
| 2019-05-03 | `a2ef21af2a49` | Andrew Burnes <andrew.burnes@gsa.gov> | Code climate fix move timeout to reject test | 1 | 4 | 3 | No |
| 2019-05-03 | `8733f24529b9` | Andrew Burnes <andrew.burnes@gsa.gov> | Code climate fix | 1 | 1 | 1 | No |
| 2019-05-03 | `092b0b66b5a2` | Andrew Burnes <andrew.burnes@gsa.gov> | Extend test timeout for delay in putBucketWebsite | 1 | 3 | 1 | No |
| 2019-05-03 | `81c242d39150` | Andrew Burnes <andrew.burnes@gsa.gov> | Add delay to putBucketWebsite creation | 2 | 10 | 5 | No |
| 2019-05-03 | `47953f08bd9d` | Andrew Burnes <andrew.burnes@gsa.gov> | Update AWS putBucketWebsite config request to retry multiple attempts | 2 | 33 | 14 | No |
| 2019-05-02 | `1c2f85c78b75` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2246 from 18F/apburnes/put-bucket-website | 4 | 99 | 13 | No |
| 2019-05-02 | `193b97d6e891` | Andrew Burnes <andrew.burnes@gsa.gov> | Add putBucketWebsite to creation of new site buckets | 4 | 99 | 13 | No |
| 2019-05-01 | `b02e73fccbf9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'apburnes/enable-private-buckets' into staging | 5 | 129 | 2 | No |
| 2019-04-30 | `cbe93aaf078a` | Andrew Burnes <andrew.burnes@gsa.gov> | fix code climate errors | 1 | 75 | 94 | No |
| 2019-04-30 | `a49a825d735f` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up code climate errors | 3 | 82 | 54 | No |
| 2019-04-30 | `6282b77af5d4` | Andrew Burnes <andrew.burnes@gsa.gov> | Set all new sites to automatically create a private bucket | 5 | 120 | 2 | No |
| 2019-04-30 | `9ef79fa87845` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'apburnes/site-links' into staging | 6 | 34 | 28 | No |
| 2019-04-30 | `bf8d92168785` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/site-links | 16 | 563 | 150 | No |
| 2019-04-30 | `b634390f5e62` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'apburnes/map-routes' into staging | 16 | 563 | 150 | No |
| 2019-04-29 | `3cf7f1f3ea63` | Andrew Burnes <andrew.burnes@gsa.gov> | Update site's proxy links to point to new bucket name based proxy route | 6 | 34 | 28 | No |
| 2019-04-26 | `75f6baed0bfa` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up CF API request method | 1 | 10 | 8 | No |
| 2019-04-26 | `fd1739142c37` | Andrew Burnes <andrew.burnes@gsa.gov> | Add delete private bucket and proxy route to S3SiteRemover | 5 | 156 | 79 | No |
| 2019-04-26 | `07abc0b5e8f2` | Andrew Burnes <andrew.burnes@gsa.gov> | Add delete service method to CF API client | 3 | 70 | 26 | No |
| 2019-04-26 | `174c3c1f7690` | Andrew Burnes <andrew.burnes@gsa.gov> | Add delete route method to CF API client | 3 | 77 | 0 | No |
| 2019-04-25 | `7e96e7fa0806` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up cfApiClient class | 3 | 117 | 58 | No |
| 2019-04-25 | `cc25eadb112a` | Andrew Burnes <andrew.burnes@gsa.gov> | Add to route creating and mapping on site bucket creation | 3 | 23 | 5 | No |
| 2019-04-24 | `b019b2169c44` | Andrew Burnes <andrew.burnes@gsa.gov> | Add route methods to api client | 8 | 137 | 1 | No |
| 2019-04-19 | `379771cd3636` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2218 from 18F/apburnes/template-engines | 2 | 5 | 1 | No |
| 2019-04-19 | `861123c98463` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge stagging | 38 | 2124 | 682 | No |
| 2019-04-19 | `78f4931cb119` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'apburnes/query-cf-bucket' into staging | 36 | 2117 | 669 | No |
| 2019-04-19 | `80d32895be57` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge from staging | 4 | 7 | 13 | No |
| 2019-04-18 | `8ab49f45f006` | Andrew Burnes <andrew.burnes@gsa.gov> | Update how we generateS3ServiceName | 3 | 4 | 4 | No |
| 2019-04-18 | `c174cc510d23` | Andrew Burnes <andrew.burnes@gsa.gov> | Add template engine through SiteCreator | 2 | 4 | 5 | No |
| 2019-04-17 | `9ad5d761f610` | Andrew Burnes <andrew.burnes@gsa.gov> | Add engine params to federalist templates | 2 | 7 | 2 | No |
| 2019-04-16 | `9f81fe9f64e6` | Andrew Burnes <andrew.burnes@gsa.gov> | Add federalist space and deploy user cf services | 3 | 12 | 4 | No |
| 2019-04-15 | `4801f9eb9e00` | Andrew Burnes <andrew.burnes@gsa.gov> | Update BUILD_SPACE_GUID to CF_SPACE_GUID env variable | 4 | 6 | 6 | No |
| 2019-04-15 | `f4c63e608201` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/query-cf-bucket | 29 | 391 | 130 | Yes |
| 2019-04-02 | `69b34720bde4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/query-cf-bucket | 1 | 12 | 1 | No |
| 2019-04-01 | `ffcff8fb53ba` | Andrew Burnes <andrew.burnes@gsa.gov> | SQS uses the bound S3 credentials when using shared bucket | 3 | 92 | 98 | No |
| 2019-04-01 | `06aabdcac95c` | Andrew Burnes <andrew.burnes@gsa.gov> | Gernerate S3 Service Name from owner and repository | 5 | 116 | 63 | No |
| 2019-03-29 | `ac409f73eb1c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/query-cf-bucket | 3 | 48 | 26 | No |
| 2019-03-29 | `20d693b6fc6a` | Andrew Burnes <andrew.burnes@gsa.gov> | Update cfInstanceName to s3ServiceName | 15 | 32 | 22 | No |
| 2019-03-27 | `2c8f0f444f9e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into apburnes/query-cf-bucket | 2 | 14 | 12 | No |
| 2019-03-27 | `26137c7edce6` | Andrew Burnes <andrew.burnes@gsa.gov> | Update SQS client to query CF API for site bucket credentials | 11 | 334 | 192 | Yes |
| 2019-03-26 | `4835ac40ff03` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix lint errors | 2 | 37 | 28 | No |
| 2019-03-26 | `2700963d518c` | Andrew Burnes <andrew.burnes@gsa.gov> | S3 services query CF API for credentials | 11 | 469 | 293 | No |
| 2019-03-25 | `92bc45a3ff0d` | Andrew Burnes <andrew.burnes@gsa.gov> | Add private bucket creation to the SiteCreator service | 8 | 524 | 375 | No |
| 2019-03-22 | `87fdbd0fd1d8` | Andrew Burnes <andrew.burnes@gsa.gov> | Add authentication and api client for Cloud Foundry | 13 | 855 | 41 | Yes |
| 2019-03-20 | `043f0a2d3a73` | Andrew Burnes <andrew.burnes@gsa.gov> | Add bucket fields to Site model | 6 | 93 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-core show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-bot`

* Path: `/Users/brianjhurst/Code/pages-bot`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/chore-set-security-considerations-read-only, origin/dependabot/npm_and_yarn/npm_and_yarn-f3562b46b9, origin/feat-add-cz-config, origin/feat-add-dev-and-staging-tests, origin/fix-airtable-sync-task-call, origin/fix-ci-git-pull-entire-origin-for-release, origin/fix-ci-slack-verify-database-queries-message, origin/fix-production-deploy-git-src-config, origin/main (+2 more)
* Remotes: `origin	https://github.com/cloud-gov/pages-bot.git (fetch)`; `origin	https://github.com/cloud-gov/pages-bot.git (push)`
* Matching commit count: 29
* Suspicious commit count: 1
* Timeline: 2024-06-26 to 2026-03-17
* Total files changed across matching commits: 100
* Total insertions/deletions: 2607 / 607
* Top changed file paths: `package.json` (12), `package-lock.json` (8), `ci/pipeline.yml` (8), `CHANGELOG.md` (7), `src/db/index.js` (5), `src/tasks/index.js` (5), `.github/workflows/security-considerations.yml` (4), `.github/workflows/security-considerations.properties.json` (3)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `2c12466dc52d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #25 from cloud-gov/release | 3 | 9 | 3 | No |
| 2026-03-17 | `ddc6188cef97` | William Zujkowski <william.zujkowski@gsa.gov> | chore(ci): Remove deprecated security-considerations automation | 1 | 0 | 8 | No |
| 2026-03-17 | `adf1ffef1e04` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #24 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-bot | 1 | 0 | 8 | No |
| 2026-03-11 | `afe1d86f24db` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #22 from cloud-gov/release | 3 | 9 | 3 | No |
| 2026-03-09 | `117c7e6ae2a9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #21 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-bot | 1 | 0 | 14 | No |
| 2025-10-07 | `0b5d714faf6a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #16 from cloud-gov/release | 3 | 11 | 3 | No |
| 2025-10-02 | `0c09305393e2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #18 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `41c8000a2f5d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-07-07 | `5c3865f5d2c5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #17 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `7d922c519548` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-05-23 | `ecdb15eddae6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #15 from cloud-gov/update-contrib-20250522221653 | 1 | 19 | 0 | No |
| 2025-05-22 | `6b779def2a97` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Update CONTRIBUTING.md | 1 | 19 | 0 | No |
| 2024-07-05 | `b27a79685594` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #13 from cloud-gov/release | 3 | 9 | 3 | No |
| 2024-07-05 | `67cccb7de7c5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #12 from cloud-gov/fix-ci-slack-verify-database-queries-message | 1 | 2 | 2 | No |
| 2024-07-05 | `e7b1d83fb7db` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #11 from cloud-gov/release | 3 | 9 | 3 | No |
| 2024-07-05 | `6a2944715c70` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #10 from cloud-gov/fix-airtable-sync-task-call | 4 | 14 | 9 | No |
| 2024-07-05 | `4a753c7e7c97` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #9 from cloud-gov/release | 3 | 9 | 3 | No |
| 2024-07-05 | `e316cd9f8e06` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #8 from cloud-gov/fix-production-deploy-git-src-config | 1 | 1 | 0 | No |
| 2024-07-05 | `dc882c1feb33` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Slack message for verify-database-queries task hooks | 1 | 2 | 2 | No |
| 2024-07-05 | `1543210be05b` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Airtable sync task call and DB query | 4 | 14 | 9 | No |
| 2024-07-03 | `75bd9ab2e79e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #6 from cloud-gov/release | 3 | 15 | 3 | No |
| 2024-07-03 | `c3c7839c2650` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #7 from cloud-gov/fix-ci-git-pull-entire-origin-for-release | 1 | 9 | 11 | No |
| 2024-07-03 | `c3255dc04e2f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Production git src config key | 1 | 1 | 0 | No |
| 2024-07-03 | `b8f5896f67e8` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Remove depth from src and fix pr status hooks | 1 | 9 | 11 | No |
| 2024-07-02 | `d255677f2b30` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2 from cloud-gov/feat-add-cz-config | 1 | 47 | 0 | No |
| 2024-07-02 | `7f7ed215ea70` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #1 from cloud-gov/feat-add-dev-and-staging-tests | 12 | 527 | 256 | No |
| 2024-07-02 | `87dbb79998fd` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add commitizen config for automated releases | 1 | 47 | 0 | No |
| 2024-06-26 | `d8014a033738` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add CI tasks for env to test database and run sync tasks | 12 | 527 | 256 | No |
| 2024-06-26 | `6cf1293629a2` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial Commit | 30 | 1290 | 0 | Yes |

Notes:
* Inspect any commit with `git -C pages-bot show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-editor`

* Path: `/Users/brianjhurst/Code/pages-editor`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/bug-editor-forms-padding, origin/bug-fix-richtext-error, origin/chore-remove-inline-styles-content-input, origin/chore-update-dependencies, origin/dependabot/npm_and_yarn/npm_and_yarn-80e28f85d4, origin/feat-Create-the-route-for-policy-pages-161, origin/feat-add-hero-and-card-grid-to-page, origin/feat-multitenancy-render, origin/fix-move-ready-review-checkbox, origin/main (+10 more)
* Remotes: `origin	https://github.com/cloud-gov/pages-editor.git (fetch)`; `origin	https://github.com/cloud-gov/pages-editor.git (push)`
* Matching commit count: 164
* Suspicious commit count: 12
* Timeline: 2025-04-23 to 2026-06-16
* Total files changed across matching commits: 1537
* Total insertions/deletions: 1804094 / 101457
* Top changed file paths: `src/payload-types.ts` (64), `src/migrations/index.ts` (59), `package.json` (42), `src/payload.config.ts` (42), `package-lock.json` (28), `src/collections/Pages/index.ts` (27), `test/utils/test.ts` (25), `src/app/(payload)/admin/importMap.js` (24)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-16 | `b8cc189c575a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #313 from cloud-gov/feat-add-forms-to-site | 63 | 45396 | 142 | No |
| 2026-06-11 | `9e76ce4e1748` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add feature flag to gate forms in env | 19 | 320 | 64 | Yes |
| 2026-06-10 | `1bc52d9a1c93` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Refine the admin view for form submissions | 16 | 1150 | 68 | No |
| 2026-06-08 | `d5bdd7d92b7d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add forms collection to allow users to create forms for sites | 38 | 43992 | 76 | Yes |
| 2026-06-03 | `8ef787ef7a8d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #292 from cloud-gov/release | 3 | 65 | 3 | No |
| 2026-06-01 | `8e55be9080fb` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #308 from cloud-gov/feat-add-theme-to-site-config | 16 | 38934 | 25 | Yes |
| 2026-06-01 | `a04e86640799` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update to Nodejs v24 with NPM v11.10 | 7 | 27 | 23 | Yes |
| 2026-05-21 | `cee20b65d7f3` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add theme group to site identity config | 10 | 38907 | 2 | Yes |
| 2026-05-20 | `f905fae1f21d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #304 from cloud-gov/chore-update-atu-package-diagram | 3 | 61 | 1 | No |
| 2026-05-18 | `31751b1ac988` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update ATU package with flow diagram | 3 | 61 | 1 | No |
| 2026-05-04 | `9543071bf1a7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #300 from cloud-gov/chore-testing-csp-configs | 1 | 5 | 6 | No |
| 2026-05-04 | `62f4ecf6d0e7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove unused CSP source variable | 1 | 0 | 2 | No |
| 2026-05-04 | `e42fd7570a47` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add connect-src to self | 1 | 4 | 4 | No |
| 2026-05-04 | `b38c9473cf07` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Adjusting CSP configs for built in component styles | 1 | 2 | 1 | No |
| 2026-04-30 | `5655de252f6b` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Rebased with main | 6 | 128 | 90 | No |
| 2026-04-30 | `681a96d2e8dc` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: IFrame CSP headers to allow cloud.gov preview urls | 1 | 4 | 1 | No |
| 2026-04-29 | `6445200c71c1` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #296 from cloud-gov/feat-add-nonce-to-csp-headers | 2 | 34 | 25 | No |
| 2026-04-29 | `311c843a85d4` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add nince to CSP headers | 2 | 34 | 25 | Yes |
| 2026-04-28 | `0480179adfd5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #295 from cloud-gov/fix-payload-config | 2 | 29 | 3 | No |
| 2026-04-27 | `8dc5ad66e643` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Payload config CSP headers and gravatar reference | 2 | 29 | 3 | No |
| 2026-04-24 | `888227649684` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #293 from cloud-gov/feat-add-collection-external-link | 8 | 35316 | 4 | No |
| 2026-04-24 | `1575660496de` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add validator to external link group | 2 | 30 | 6 | No |
| 2026-04-14 | `4a8c0a4127fe` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #278 from cloud-gov/release | 3 | 31 | 3 | No |
| 2026-04-14 | `011b98b62596` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #290 from cloud-gov/feat-add-layout-type-to-collection-types | 10 | 39734 | 4002 | No |
| 2026-04-13 | `830d5bd3542c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add layout type to collection types for list or card grid view | 10 | 39734 | 4002 | No |
| 2026-04-02 | `10c66ffe5a25` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #288 from cloud-gov/feat-refine-the-atu-package-and-dashboard | 3 | 560 | 364 | No |
| 2026-04-01 | `8e6a26c03e1a` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Refine ATU package and dashboard | 3 | 560 | 364 | No |
| 2026-03-30 | `7cd9bf5925d1` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #284 from cloud-gov/feat-add-site-compliance-atu-docs | 32 | 73250 | 35 | No |
| 2026-03-27 | `b6598c9b0cbf` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(ci): Add access tests to SiteAuth collection and ATU package | 6 | 258 | 7 | No |
| 2026-03-26 | `5c858928c017` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Table heading width to allow the first heading to expand based on content | 1 | 0 | 9 | No |
| 2026-03-23 | `7179f6a2881c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site ATU package for managers to download | 17 | 35779 | 259 | No |
| 2026-03-19 | `f9e2fef1b034` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site auth global collection to manage ATU | 10 | 36017 | 100 | No |
| 2026-03-18 | `df45d0439013` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site compliance ATU Package and compliance section | 8 | 454 | 14 | No |
| 2026-03-16 | `7a9176e98032` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add site compliance ATU docs page | 11 | 1098 | 2 | No |
| 2026-03-16 | `6048caaf8cd9` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #280 from cloud-gov/feat-add-collection-type-edit-link | 23 | 33453 | 442 | No |
| 2026-03-16 | `0b3d3a606ae4` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Collection entry preview and dev site gantry version build | 4 | 11 | 6 | No |
| 2026-03-13 | `bf68e96c8360` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add side nav collection to collection entries and pages | 17 | 33407 | 419 | No |
| 2026-03-13 | `5d83052f5152` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #279 from cloud-gov/feat-add-build-site-hook-on-unpublish-delete | 9 | 86 | 69 | No |
| 2026-03-13 | `3017542eb9f3` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add collection type edit link in type card | 3 | 35 | 17 | No |
| 2026-03-12 | `23d848d98dfc` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add build site hook on record unpublish or delete | 9 | 86 | 69 | Yes |
| 2026-03-12 | `4fcaecc276e8` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #274 from cloud-gov/chore-remove-security-considerations-action | 3 | 0 | 26 | No |
| 2026-03-11 | `67d63f0efada` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #271 from cloud-gov/release | 3 | 14 | 3 | No |
| 2026-03-11 | `752292d05e76` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #275 from cloud-gov/chore-deprecate-unused-collections | 44 | 34726 | 10471 | No |
| 2026-03-11 | `0c5a40eb9794` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Deprecate unused collections for initial data model | 44 | 34726 | 10471 | No |
| 2026-03-09 | `6e7822ff0f95` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove security considerations action | 3 | 0 | 26 | No |
| 2026-03-09 | `178f0aca7ff4` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #270 from cloud-gov/feat-refactor-dashboard | 11 | 485 | 336 | No |
| 2026-03-05 | `bf3720525445` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #269 from cloud-gov/chore-hide-site-bot-user | 2 | 147 | 34 | No |
| 2026-03-04 | `84126753034e` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Refactor admin dashboard #266 | 11 | 485 | 336 | No |
| 2026-03-03 | `b2e1b594f213` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #264 from cloud-gov/release | 3 | 199 | 3 | No |
| 2026-03-03 | `1c96fb0608c3` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #262 from cloud-gov/feat-ci-create-release-pipeline | 2 | 111 | 3 | No |
| 2026-03-02 | `b1417af56e0f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Create CI pipeline to automate tags and releases | 2 | 111 | 3 | No |
| 2026-03-02 | `e61ff8373238` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #260 from cloud-gov/feat-simplify-data-model | 75 | 209551 | 21066 | No |
| 2026-02-26 | `a52362582c7d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Update local dev seed data to refactored schema | 10 | 2023 | 17288 | No |
| 2026-02-25 | `3f6cec30fc6d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Refactor reused fields and standardize Pages collection | 19 | 88047 | 937 | No |
| 2026-02-19 | `74944a79c594` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Standardize hyperlink fields used by collections | 30 | 42418 | 1698 | No |
| 2026-02-12 | `8326685a9f25` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Simplify data model with collection types and entries | 46 | 77521 | 1601 | No |
| 2026-02-09 | `5188c591a6e6` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #251 from cloud-gov/chore-update-to-payload-3_75_0 | 5 | 1792 | 1288 | No |
| 2026-02-05 | `e5cffa5a0742` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update to Payload v3.75.0 | 5 | 1792 | 1288 | No |
| 2026-01-06 | `da001340d247` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #235 from cloud-gov/fix-access-permissions-for-pages-and-policies | 4 | 65 | 77 | No |
| 2026-01-06 | `fdbc83dfa0ae` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Access permisions to allow site users to delete Pages and Policies | 4 | 65 | 77 | No |
| 2026-01-05 | `22d7b9cead69` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #233 from cloud-gov/fix-home-page-card-length | 1 | 1 | 1 | No |
| 2025-12-29 | `c74830abf67e` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Home Page card length from 6 to 24 | 1 | 1 | 1 | No |
| 2025-12-29 | `e9e9636c2ef5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #230 from cloud-gov/fix-slug-hook-effect-errors | 7 | 36487 | 32 | No |
| 2025-12-29 | `44408a025bff` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #222 from cloud-gov/feat-create-user-roles-permission-page | 11 | 907 | 2 | No |
| 2025-12-22 | `e0b8dabb48f1` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Slug hook useEffect error affecting title input | 7 | 36487 | 32 | No |
| 2025-12-19 | `8e3af1122366` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #215 from cloud-gov/chore-add-domain-config-settings-to-readme | 1 | 1 | 0 | No |
| 2025-12-18 | `e66d8968dd74` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add domain service config to README docs | 1 | 1 | 0 | No |
| 2025-12-18 | `213eb9e151b0` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #212 from cloud-gov/fix-all-collections-item-preview-links | 6 | 50 | 23 | No |
| 2025-12-17 | `d93e13a82da2` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: All collection preview links to point to the correct url | 6 | 50 | 23 | No |
| 2025-12-16 | `1c4cb0b16d71` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #209 from cloud-gov/chore-update-payload-version | 4 | 185 | 188 | No |
| 2025-12-16 | `78f6adc45cf1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Upload PayloadCMS to v3.68.5 | 4 | 185 | 188 | No |
| 2025-12-15 | `f2a4619eb7b1` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #200 from cloud-gov/feat-add-related-items-component-to-collections | 13 | 37208 | 1 | No |
| 2025-12-15 | `5ecb37fa53aa` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #207 from cloud-gov/fix-check-migrations-ci-job | 8 | 1056 | 89 | No |
| 2025-12-15 | `c8154e65b797` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Rename 404 collection to NotFoundPage to successfull create types and regenerate migrations | 7 | 1055 | 88 | No |
| 2025-12-15 | `dbb14d166dd1` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update check migrations task to error when incomplete migrations exist | 1 | 1 | 1 | No |
| 2025-12-12 | `34cd5da1e3df` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Add related items component | 13 | 37208 | 1 | No |
| 2025-12-05 | `4e3fc4d8c776` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #197 from cloud-gov/feat-add-site-delete-hook-to-pages-core | 4 | 97 | 2 | No |
| 2025-12-05 | `93cc0e67d99f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add afterDelete hook for site to call delete webhook to Pages core | 4 | 97 | 2 | Yes |
| 2025-12-04 | `afb6e8e652ab` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #195 from cloud-gov/chore-update-node-deps-20251204 | 9 | 34173 | 2486 | No |
| 2025-12-04 | `21448a636d7d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #194 from cloud-gov/fix-editor-forms-padding | 2 | 53 | 15 | No |
| 2025-12-04 | `f043d6e44bfa` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update node deps 2025-12-04 | 9 | 34173 | 2486 | No |
| 2025-12-04 | `20ca2214fb22` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Editor forms padding | 2 | 53 | 15 | No |
| 2025-12-02 | `0afd6654865b` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #188 from cloud-gov/chore-rename-page-menus | 14 | 33498 | 990 | No |
| 2025-12-01 | `1778b3e18f1c` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #176 from cloud-gov/pb/codeowners-fix | 1 | 1 | 1 | No |
| 2025-11-26 | `1e0d5ffde79d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #183 from cloud-gov/feat-user-generated-general-collections | 15 | 38812 | 65 | No |
| 2025-11-26 | `4e5b927d20d2` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Seed datatsets for local dev | 4 | 2124 | 58 | No |
| 2025-11-17 | `c12944593910` | Peter Burkholder <peter.burkholder@gsa.gov> | fix: Limit CODEOWNERS only to Pages team | 1 | 1 | 1 | No |
| 2025-10-30 | `801c7f339514` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Page Menus collection | 10 | 13445 | 4839 | No |
| 2025-10-30 | `4cca62069499` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #149 from cloud-gov/chore-unify-live-preview-based-on-site-slug | 23 | 145 | 222 | No |
| 2025-10-29 | `e9da62437a87` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Unify live preview for collections based on site slug | 23 | 145 | 222 | Yes |
| 2025-10-27 | `28a7fb65912b` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #144 from cloud-gov/chore-update-site-create-delete-hooks-for-preview-deploys | 4 | 579 | 9 | No |
| 2025-10-24 | `1cbc71c65727` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #143 from cloud-gov/fix-user-selected-site-after-site-delete | 1 | 83 | 34 | No |
| 2025-10-24 | `e5d58d197603` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update site create and delete hooks preview deploy config | 4 | 579 | 9 | No |
| 2025-10-24 | `593db8754d49` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: User selectedSiteId to update to other site if selected site is deleted | 1 | 83 | 34 | No |
| 2025-10-23 | `5bca45b251bc` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #142 from cloud-gov/fix-home-page-custom-rich-text | 1 | 2 | 0 | No |
| 2025-10-23 | `735a1dd990e6` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add our custom lexical editor to Home Page rich text | 1 | 2 | 0 | No |
| 2025-10-23 | `914351b1581f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #141 from cloud-gov/chore-add-slug-field-to-sites | 10 | 24219 | 201 | No |
| 2025-10-22 | `9c41b3500d9e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add slug field to sites for preview deployments | 10 | 24219 | 201 | No |
| 2025-10-21 | `0e301f15d8c8` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Add Side Navigation component to Single Pages | 7 | 22030 | 4 | No |
| 2025-10-20 | `ba2655f4b3d9` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #131 from cloud-gov/fix-slug-field-returning-null | 4 | 207 | 29 | No |
| 2025-10-16 | `0165667dc728` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #130 from cloud-gov/fix-pages-staging-postfix | 1 | 1 | 1 | No |
| 2025-10-16 | `daa584f520f9` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #129 from cloud-gov/fix-docker-gantry-service | 1 | 2 | 2 | No |
| 2025-10-16 | `638145ad3009` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #128 from cloud-gov/fix-staging-deploy | 2 | 12 | 11 | No |
| 2025-10-16 | `33a5bfaff138` | Kevin Masters <kevin.masters@gsa.gov> | fix: update docker npm scripts to match gantry service in Dockerfile | 1 | 2 | 2 | No |
| 2025-10-16 | `95b24192f752` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Slug field generates random string when title is null during draft | 4 | 207 | 29 | No |
| 2025-10-16 | `458f3eca2441` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Pages staging postfix deploy variable | 1 | 1 | 1 | No |
| 2025-10-16 | `74b68a026388` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Staging deploy pipeline | 2 | 12 | 11 | No |
| 2025-10-16 | `af4bd945995a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #127 from cloud-gov/chore-add-bootstrap-script | 4 | 97 | 2 | No |
| 2025-10-15 | `065a338cc3e9` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #123 from cloud-gov/chore-email-logo-resize | 3 | 0 | 0 | No |
| 2025-10-15 | `8505aa0c4114` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add bootstrap script for payload instance | 4 | 97 | 2 | No |
| 2025-10-10 | `f484f44f2226` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #122 from cloud-gov/chore-small-content-changes | 14 | 14707 | 78 | No |
| 2025-10-10 | `a984044d6b68` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #121 from cloud-gov/chore-add-routes-to-deploy-envs | 4 | 5 | 2 | No |
| 2025-10-10 | `33d4f16a31a8` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Create migration to remove subtitle and label from Page collection | 11 | 14704 | 43 | No |
| 2025-10-10 | `8fc09cef4c94` | Jonathan Bobel <jonathan.bobel@gsa.gov> | chore: small content changes | 6 | 3 | 35 | No |
| 2025-10-10 | `74c267d530b7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add routes to app deploy envs | 4 | 5 | 2 | No |
| 2025-10-09 | `3e0c0003ef24` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #120 from cloud-gov/chore-remove-auto-image-resizing | 6 | 14828 | 185 | No |
| 2025-10-09 | `c77390faa7d5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #119 from cloud-gov/bug-typo-in-dcgantry-command | 1 | 1 | 1 | No |
| 2025-10-09 | `867b031fce44` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove auto image resizing from Media collection | 6 | 14828 | 185 | No |
| 2025-09-30 | `647569fbdcc6` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #109 from cloud-gov/feat-add-resources-collection | 13 | 16610 | 63 | No |
| 2025-09-26 | `e01a1247b526` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #107 from cloud-gov/chore-duplicate-welcome-alerts | 3 | 14 | 17 | No |
| 2025-09-25 | `e79fedae1a5f` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Adding Resources collection | 13 | 16610 | 63 | No |
| 2025-09-24 | `b5eb0b0c6c7f` | Jonathan Bobel <jonathan.bobel@gsa.gov> | chore: Fixing duplicate alerts on dashboard | 3 | 14 | 17 | No |
| 2025-09-23 | `7e694149f934` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #101 from cloud-gov/feat-add-description-to-editor-cards | 28 | 2940 | 556 | No |
| 2025-09-22 | `6da9bff0df76` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add additional npm install sharp step for CI app build | 1 | 1 | 0 | No |
| 2025-09-16 | `c507b12d3649` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: add description to editor cards | 26 | 1295 | 727 | No |
| 2025-09-11 | `dfabd946e50f` | Jonathan Bobel <jonathan.bobel@gsa.gov> | chore: Reorganizeing admin dashboard | 6 | 2134 | 319 | No |
| 2025-09-11 | `69e1a6f201c2` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #97 from cloud-gov/feat-add-two-color-and-font-theming | 6 | 14442 | 10 | No |
| 2025-09-11 | `7e9ac1e0438b` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add two color and font theming from site config | 6 | 14442 | 10 | No |
| 2025-09-04 | `f86d797ac07a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #93 from cloud-gov/chore-adjust-menu-collection-to-site | 10 | 26403 | 126 | No |
| 2025-09-04 | `be27f9fc4dac` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add label text to menu subitems | 5 | 12949 | 1 | No |
| 2025-09-03 | `a87048291749` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Adjust global menu collection to be related to a site | 8 | 13460 | 131 | No |
| 2025-09-02 | `dcaf84e7cd2f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #92 from cloud-gov/feat-add-leadership-collection-page | 13 | 12259 | 20 | No |
| 2025-08-29 | `b34e887ea33f` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Add leadership collection to CMS | 13 | 12259 | 20 | No |
| 2025-08-28 | `7e338b7596aa` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #90 from cloud-gov/fix-pin-payload-3.50.0-for-lexical-files | 5 | 10960 | 119 | No |
| 2025-08-28 | `0f70864ad5ef` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Pin Payload to v3.50.0 to fix lexical editor bug | 5 | 10960 | 119 | No |
| 2025-08-28 | `feede6ee8e67` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #89 from cloud-gov/feat-dynamic-menu-items | 25 | 17109 | 2660 | No |
| 2025-08-27 | `1853da1036b3` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add dynamic menu items and refine existing collection fields | 25 | 17109 | 2660 | No |
| 2025-08-19 | `018469386b1c` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #85 from cloud-gov/chore-make-local-minio-storage-public | 1 | 3 | 3 | No |
| 2025-08-18 | `ea31911f148c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Make local minio storage publically accessible | 1 | 3 | 3 | No |
| 2025-08-14 | `cf66529d2582` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #84 from cloud-gov/feat-add-s3-media-sync-to-site-bucket | 13 | 537 | 23 | No |
| 2025-08-12 | `3cc63456d934` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add S3 site media sync to site Pages bucket | 13 | 537 | 23 | Yes |
| 2025-08-12 | `af3644401208` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #83 from cloud-gov/chore-add-local-seed-data | 11 | 20370 | 76 | No |
| 2025-08-07 | `389c88efc836` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add seed data for local dev | 11 | 20370 | 76 | No |
| 2025-07-18 | `ae6e4bea9cb7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #82 from cloud-gov/ci-bucket-manger-creds-sync | 5 | 112 | 0 | No |
| 2025-07-17 | `5877f8a83796` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Add user provided service sync for Pages bucket manager | 5 | 112 | 0 | No |
| 2025-07-07 | `0f8878b271b7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #80 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `ce1111796255` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-06-26 | `bc3fa9250650` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #78 from cloud-gov/fix-preview-site-config-bucket-prefix | 1 | 4 | 2 | No |
| 2025-06-17 | `600956330d9c` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Preview site config file S3 bucket prefix | 1 | 4 | 2 | No |
| 2025-06-11 | `cc0e777e78bf` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #76 from cloud-gov/feat-add-policies-collection | 24 | 19528 | 75 | No |
| 2025-06-11 | `6a4e296a5f94` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Simplify policies collection and record review completion | 14 | 9339 | 89 | No |
| 2025-06-04 | `ef1854f25ca0` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add policies collection | 15 | 10253 | 50 | No |
| 2025-06-03 | `281af735fde0` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #74 from cloud-gov/feat-add-contact-and-history-pages | 22 | 18973 | 357 | No |
| 2025-06-03 | `7a269e6c3466` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Rename collection singlepages to pages | 11 | 9010 | 95 | No |
| 2025-05-23 | `a3ae33bdc7c8` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add singlepages collection for contact, history, about, careers | 20 | 10058 | 357 | No |
| 2025-05-22 | `bde174a776f7` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Replace CONTRIBUTING.md | 1 | 13 | 11 | No |
| 2025-05-22 | `cc5b5676bd70` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #69 from cloud-gov/update-contrib-20250522195325 | 1 | 13 | 11 | No |
| 2025-05-22 | `327f89a4304d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #68 from cloud-gov/feat-add-report-category-collections | 23 | 17200 | 123 | No |
| 2025-05-22 | `e24ccb5d289b` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Adjust reports to have excerpt field | 9 | 7877 | 19 | No |
| 2025-05-21 | `2469e2a13168` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Reports and Categories collections | 21 | 9330 | 111 | No |
| 2025-05-20 | `913b189b192e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #66 from cloud-gov/feat-add-media-collection | 26 | 7933 | 654 | No |
| 2025-05-15 | `032619726583` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Media collection type | 26 | 7933 | 654 | Yes |
| 2025-04-24 | `fb02e270fd25` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #51 from cloud-gov/fix-create-site-webhook-endpoint | 2 | 16 | 14 | No |
| 2025-04-23 | `b04e24afca56` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Create site Pages webhook endpoint path | 2 | 16 | 14 | Yes |

Notes:
* Inspect any commit with `git -C pages-editor show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `eleventy-preset`

* Path: `/Users/brianjhurst/Code/eleventy-preset`
* Current branch: `release/v0.3.1`
* Readable: yes
* Available branches/remotes: feature/release-workflow, feature/remove-decap-code-block-editor, feature/uswds-accordion-component, feature/uswds-accordion-editor-component, fix/uswds-accordion-shortcode-registration, main, release/v0.3.0, release/v0.3.1, use-bundled-decap-cms-admin, origin, origin/dependabot/npm_and_yarn/npm_and_yarn-53cbaf2a5b, origin/feature/release-workflow (+8 more)
* Remotes: `origin	git@github.com:cloud-gov/eleventy-preset.git (fetch)`; `origin	git@github.com:cloud-gov/eleventy-preset.git (push)`
* Matching commit count: 1
* Suspicious commit count: 0
* Timeline: 2026-06-17 to 2026-06-17
* Total files changed across matching commits: 4
* Total insertions/deletions: 901 / 1136
* Top changed file paths: `src/shortcodes.js` (1), `package.json` (1), `package-lock.json` (1), `test/shortcodes.test.js` (1)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-17 | `f4d0f0c1c680` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Shortcode eleventy registration for images | 4 | 901 | 1136 | No |

Notes:
* Inspect any commit with `git -C eleventy-preset show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `docs`

* Path: `/Users/brianjhurst/Code/docs`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: bh-broken-links, bh-fix-kb-broken-links, bh-local-search, bh-remove-noindex, bh-update-deps, bh-update-deps-part-deux, feat-modal, main, origin/2025-07-23_security_review, origin/2025-08-27_wjz_updates, origin/ArsHaider-patch-1, origin (+42 more)
* Remotes: `origin	git@github.com:cloud-gov/docs.git (fetch)`; `origin	git@github.com:cloud-gov/docs.git (push)`
* Matching commit count: 4
* Suspicious commit count: 0
* Timeline: 2026-04-14 to 2026-05-21
* Total files changed across matching commits: 52
* Total insertions/deletions: 28 / 28
* Top changed file paths: `docs/pages/developers/large-file-handling.md` (2), `docs/pages/developers/how-builds-work.md` (2), `docs/assets/pages/pages-site-settings-branch-config.png` (2), `docs/assets/pages-site-settings-branch-config copy.png` (2), `docs/pages/developers/env-vars-on-pages-builds.md` (2), `docs/assets/{ => pages}/env_var.png` (2), `docs/assets/{ => pages}/schedule-nightly.png` (2), `docs/assets/custom-domain-create.png` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-05-21 | `0d23e9aa8456` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #179 from cloud-gov/chore-update-pages-build-container-disk-size | 1 | 2 | 2 | No |
| 2026-05-21 | `d19a87c1a7a9` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Pages update disk space docs to 10GB for large site builds | 1 | 2 | 2 | No |
| 2026-04-14 | `b37664efd3ab` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #161 from cloud-gov/feat-add-site-engine-select-site-creation | 25 | 12 | 12 | No |
| 2026-04-14 | `4b3400b3fdbb` | Andrew Burnes <andrew.burnes@gsa.gov> | pages: Add site engine select and update to latest app branding images | 25 | 12 | 12 | No |

Notes:
* Inspect any commit with `git -C docs show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-example-spa`

* Path: `/Users/brianjhurst/Code/pages-example-spa`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/dependabot/npm_and_yarn/npm_and_yarn-53cbaf2a5b, origin/main
* Remotes: `origin	https://github.com/cloud-gov/pages-example-spa.git (fetch)`; `origin	https://github.com/cloud-gov/pages-example-spa.git (push)`
* Matching commit count: 3
* Suspicious commit count: 0
* Timeline: 2025-10-02 to 2026-06-10
* Total files changed across matching commits: 4
* Total insertions/deletions: 18 / 14
* Top changed file paths: `CODEOWNERS` (2), `package.json` (1), `package-lock.json` (1)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-10 | `b75615346f9d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #34 from cloud-gov/dp-security | 2 | 16 | 14 | No |
| 2025-10-02 | `12c9d69c07ff` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #24 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `fa74fc905dfb` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-example-spa show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-example-website-api`

* Path: `/Users/brianjhurst/Code/pages-example-website-api`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/db-logic-ideas, origin/dependabot/pip/werkzeug-3.1.6, origin/dp-security, origin/main, origin/pages-example-website-api_add_security_md_20240408110349, origin/update-contrib-20250522195325, origin/update-contrib-20250522200030, origin/update-contrib-20250522200331
* Remotes: `origin	https://github.com/cloud-gov/pages-example-website-api.git (fetch)`; `origin	https://github.com/cloud-gov/pages-example-website-api.git (push)`
* Matching commit count: 2
* Suspicious commit count: 0
* Timeline: 2025-10-02 to 2025-10-02
* Total files changed across matching commits: 2
* Total insertions/deletions: 2 / 0
* Top changed file paths: `CODEOWNERS` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2025-10-02 | `e2977e0f3335` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #39 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `2b866984fc32` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-example-website-api show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-example-api-website`

* Path: `/Users/brianjhurst/Code/pages-example-api-website`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/dependabot/npm_and_yarn/follow-redirects-1.16.0, origin/dp-security, origin/main, origin/pages-example-api-website_add_security_md_20240408110403, origin/update-contrib-20250522193849, origin/update-contrib-20250522195325, origin/update-contrib-20250522200030
* Remotes: `origin	https://github.com/cloud-gov/pages-example-api-website.git (fetch)`; `origin	https://github.com/cloud-gov/pages-example-api-website.git (push)`
* Matching commit count: 2
* Suspicious commit count: 0
* Timeline: 2025-10-02 to 2025-10-02
* Total files changed across matching commits: 2
* Total insertions/deletions: 2 / 0
* Top changed file paths: `CODEOWNERS` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2025-10-02 | `50ab6653639a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #27 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `0008ffc26959` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-example-api-website show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-proxy`

* Path: `/Users/brianjhurst/Code/pages-proxy`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/dependabot/npm_and_yarn/npm_and_yarn-3c67cbb9cd, origin/main
* Remotes: `origin	https://github.com/cloud-gov/pages-proxy.git (fetch)`; `origin	https://github.com/cloud-gov/pages-proxy.git (push)`
* Matching commit count: 113
* Suspicious commit count: 0
* Timeline: 2019-04-23 to 2026-06-03
* Total files changed across matching commits: 346
* Total insertions/deletions: 15001 / 5117
* Top changed file paths: `ci/pipeline.yml` (42), `README.md` (32), `nginx.conf` (28), `ci/federalist-pipeline.yml` (26), `package-lock.json` (25), `test/main.js` (20), `package.json` (19), `docker-compose.yml` (18)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-03 | `a89f6f0d9b94` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #238 from cloud-gov/release | 3 | 10 | 3 | No |
| 2026-03-09 | `4319dd8dfb9b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #237 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-proxy | 1 | 0 | 14 | No |
| 2025-11-25 | `33d8831ac4c6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #235 from cloud-gov/release | 3 | 9 | 3 | No |
| 2025-11-25 | `78557a731d64` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #234 from cloud-gov/feat-enable-public-file-hosting-for-preview-domains | 2 | 47 | 14 | No |
| 2025-11-25 | `81554b65640a` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Enable public file hosting for site preview domains | 2 | 47 | 14 | No |
| 2025-10-16 | `f112702e4306` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #231 from cloud-gov/release | 3 | 9 | 3 | No |
| 2025-10-16 | `5e948420926e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #230 from cloud-gov/chore-update-deps-20251015 | 1 | 101 | 38 | No |
| 2025-10-15 | `bdf409f0c889` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update dependencies form-data and brace-expansion | 1 | 101 | 38 | No |
| 2025-10-06 | `db2938457c97` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #228 from cloud-gov/release | 3 | 13 | 3 | No |
| 2025-10-06 | `51f7018d6be7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #229 from cloud-gov/fix-encoded-forward-slash-redirects | 2 | 32 | 2 | No |
| 2025-10-06 | `1489940db830` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Return 404 when encoded forward slashes attempt redirect | 2 | 32 | 2 | No |
| 2025-10-02 | `5f397ed05f6f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #227 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `9603d31d26f7` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-09-30 | `20e5a18f0f7d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #222 from cloud-gov/release | 3 | 15 | 3 | No |
| 2025-09-30 | `6f40844ca1df` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #223 from cloud-gov/update-contrib-20250522220748 | 1 | 13 | 13 | No |
| 2025-09-30 | `90e3776b0c6c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #225 from cloud-gov/chore-set-x-amz-if-match-last-modified-time | 1 | 1 | 0 | No |
| 2025-09-30 | `5ad7de2f3980` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set x-amz-if-match-last-modified-time to empty | 1 | 1 | 0 | No |
| 2025-07-07 | `815ed509ddb6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #224 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `9c83c6f5856e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-05-22 | `f4b67b984b15` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Update CONTRIBUTING.md | 1 | 13 | 13 | No |
| 2025-03-18 | `947314a06369` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #221 from cloud-gov/feat-add-assets-routing | 8 | 1382 | 473 | No |
| 2025-03-13 | `bfab5e8d9825` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add ~assets routing for sites | 8 | 1382 | 473 | No |
| 2024-07-11 | `d7dab0386c6b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #217 from cloud-gov/release | 3 | 46 | 3 | No |
| 2024-07-10 | `2a8d71258e21` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #216 from cloud-gov/fix-ci-set-src-passing-correctly-for-release | 1 | 6 | 7 | No |
| 2024-07-10 | `bacd4c43eb0f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #215 from cloud-gov/chore-ci-task-topology-and-cz-config | 2 | 64 | 14 | No |
| 2024-07-10 | `798e5fb07a26` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #214 from cloud-gov/chore-update-node-deps | 1 | 14 | 14 | No |
| 2024-07-10 | `43f9dec1a872` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #213 from cloud-gov/chore-ci-cleaner | 1 | 1 | 6 | No |
| 2024-07-10 | `ca2aed7a04ce` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Set src passed a correct level for release tasks | 1 | 6 | 7 | No |
| 2024-07-10 | `f7510187431c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Rework staging and prod CI task topology and add .cz.json config | 2 | 64 | 14 | No |
| 2024-07-10 | `74bc0378fd7a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update node.js dependencies braces and fill-range | 1 | 14 | 14 | No |
| 2024-07-03 | `ab86b2e49a83` | Drew Bollinger <drew.bollinger@gsa.gov> | chore(ci): pull full repo for release | 1 | 1 | 6 | No |
| 2024-05-29 | `7ca4e5da82da` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #209 from cloud-gov/staging | 9 | 164 | 131 | No |
| 2024-03-12 | `6bd7bed17d2b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #205 from cloud-gov/chore-ci-update-general-task-registry-image | 2 | 22 | 4 | No |
| 2024-03-12 | `619c5a59f055` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Switch to general-task and registry-image for CI jobs | 2 | 22 | 4 | No |
| 2024-02-16 | `124f702398be` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #204 from cloud-gov/staging | 10 | 139 | 510 | No |
| 2024-02-15 | `cbc1176ba775` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #203 from cloud-gov/chore-cleanup-ci-tests-and-git-source | 4 | 68 | 135 | No |
| 2024-02-15 | `0e27d5b85b88` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #202 from cloud-gov/chore-update-ci-to-hardened-resources | 8 | 120 | 424 | No |
| 2024-02-15 | `b2cebd07d260` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Partialize CI tests and use hardened git resource | 4 | 68 | 135 | No |
| 2024-02-14 | `5d50879d3b37` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update README.md | 1 | 1 | 1 | No |
| 2024-02-14 | `1e563e55bfe0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update CI pipelines to hardened resources | 8 | 119 | 423 | No |
| 2023-05-03 | `34d5d3c32c87` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #198 from cloud-gov/staging | 8 | 542 | 61 | No |
| 2023-04-18 | `794a2f98af0c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #197 from cloud-gov/ci-verify-commit-gpg-key | 2 | 2 | 0 | No |
| 2023-04-17 | `0eb0847b5dbc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #196 from cloud-gov/feat-add-pr-dev-deployment | 8 | 540 | 61 | No |
| 2023-04-17 | `b5c95c2e27cb` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 2 | 2 | 0 | No |
| 2023-04-13 | `b27559233f9f` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove GH PR status updates since the staging pipeline does this already | 1 | 0 | 24 | No |
| 2023-04-11 | `ae5327783b52` | Andrew Burnes <andrew.burnes@gsa.gov> | Update node dependencies to v18 | 3 | 278 | 55 | No |
| 2023-04-11 | `093b46a44230` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add dev deployment env for PRs to staging | 5 | 286 | 6 | No |
| 2023-03-27 | `2380745798b2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #193 from cloud-gov/staging | 3 | 18 | 5 | No |
| 2023-03-22 | `23fd46c87285` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #192 from cloud-gov/feat-switch-to-hardened-container | 2 | 12 | 4 | No |
| 2023-03-22 | `1f52690e7f28` | Andrew Burnes <andrew.burnes@gsa.gov> | Switch to hyphens for ecr creds | 2 | 4 | 4 | No |
| 2023-03-21 | `3aee70e3461f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Switch to using harden container fof cf-image | 2 | 12 | 4 | No |
| 2023-03-14 | `9116699b0bb1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #191 from cloud-gov/chore-update-app-stack-cflinuxfs4 | 3 | 6 | 1 | No |
| 2023-03-14 | `3af64bc45de6` | Andrew Burnes <andrew.burnes@gsa.gov> | update: Parameterize stack with CF_STACK | 3 | 3 | 1 | No |
| 2023-03-13 | `c01517de2137` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update app stack to cflinuxfs4 | 1 | 4 | 1 | No |
| 2023-03-09 | `facd0644df03` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #188 from cloud-gov/feat-only-allow-get-head-requests | 2 | 57 | 0 | No |
| 2023-03-09 | `6883cb9aa112` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Only allow GET, HEAD requests | 2 | 57 | 0 | No |
| 2023-03-07 | `f90767b1e444` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #186 from cloud-gov/staging | 3 | 284 | 117 | No |
| 2023-03-07 | `c084e1291522` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #185 from cloud-gov/add-additional-other-encoded-checks | 1 | 2 | 1 | No |
| 2023-03-07 | `3c33720bffd6` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Added encoded values check regex | 1 | 2 | 1 | No |
| 2023-03-07 | `e8ef2ad88127` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #184 from cloud-gov/add-additional-encoded-checks | 3 | 283 | 117 | No |
| 2023-03-07 | `319f174e019e` | Andrew Burnes <andrew.burnes@gsa.gov> | add: Additional checks on encoded strings in path | 3 | 283 | 117 | No |
| 2022-10-05 | `a35964d87af2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #179 from cloud-gov/staging | 14 | 2 | 64 | No |
| 2022-09-27 | `886157718009` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #177 from cloud-gov/staging | 16 | 1928 | 97 | No |
| 2022-09-22 | `006a73a37271` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #176 from cloud-gov/feat-specify-redirect-site-path | 5 | 57 | 21 | No |
| 2022-09-22 | `dd97e6f5df30` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add usePreviewPath option on redirects to keep site preview path on redirect | 5 | 57 | 21 | No |
| 2022-09-20 | `9c20d30b7c9b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #175 from cloud-gov/fix-build-redirects-task | 2 | 24 | 34 | No |
| 2022-09-20 | `a352a3dadd46` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI pipeline has working build-redirects task | 2 | 24 | 34 | No |
| 2022-09-20 | `c87df20cb577` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #174 from cloud-gov/feat-add-redirects-for-sites-173 | 16 | 1898 | 93 | No |
| 2022-09-20 | `4cdff8d1f4d6` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add build redirects to federalist proxy deploy | 1 | 15 | 0 | No |
| 2022-09-19 | `4ab3be46adda` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: add support for empty array of redirects | 3 | 41 | 2 | No |
| 2022-09-19 | `62faa8aadefa` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: test:integration to include redirects | 1 | 2 | 3 | No |
| 2022-09-19 | `3dab37cb1578` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Test and build redirects | 10 | 135 | 50 | No |
| 2022-09-16 | `b4e1b7766f92` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add redirects utils | 10 | 292 | 37 | No |
| 2022-09-15 | `ce97df637a7c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: update test env to Node 16 | 4 | 1464 | 52 | No |
| 2022-08-03 | `696151e8a7ef` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #167 from 18F/staging | 1 | 1 | 4 | No |
| 2022-08-03 | `824dd6e4aea9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'main' into staging | 0 | 0 | 0 | No |
| 2022-08-03 | `efee6b2225af` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #166 from 18F/apb/fix-federalist-proxy-set-pipeline | 1 | 1 | 4 | No |
| 2022-08-03 | `1e82a6968513` | Andrew Burnes <andrew.burnes@gsa.gov> | Fixed the set-pipeline job to federalist-proxy pipeline | 1 | 1 | 4 | No |
| 2022-08-03 | `91a604876598` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #165 from 18F/staging | 6 | 311 | 147 | No |
| 2022-08-03 | `e49bcff93e12` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'main' into staging | 0 | 0 | 0 | No |
| 2022-08-02 | `c28948e1cfae` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #164 from 18F/apb/move-federalist-prod-concourse-2086 | 6 | 311 | 147 | No |
| 2022-08-02 | `24ac79365b1b` | Andrew Burnes <andrew.burnes@gsa.gov> | Move federalist-proxy prod to concourse | 6 | 311 | 147 | No |
| 2022-08-02 | `b0a65d456766` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #162 from 18F/staging | 3 | 98 | 149 | No |
| 2022-07-28 | `dc6fb44f77dd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #160 from 18F/apb/refactor-ci-pipeline-2086 | 2 | 96 | 147 | No |
| 2022-07-28 | `46320e8635d9` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix the bear | 1 | 1 | 1 | No |
| 2022-07-28 | `ece4c6027b4c` | Andrew Burnes <andrew.burnes@gsa.gov> | Update README.md | 1 | 1 | 1 | No |
| 2022-07-28 | `b4e0153f3a75` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix `Concourse` spelling | 1 | 1 | 1 | No |
| 2022-07-28 | `128c6ac3660f` | Andrew Burnes <andrew.burnes@gsa.gov> | Add docs about pipeline param vars | 1 | 28 | 7 | No |
| 2022-07-27 | `912014bfdefa` | Andrew Burnes <andrew.burnes@gsa.gov> | Update proxy pipeline to staging and production instanced pipelines | 2 | 75 | 147 | No |
| 2022-07-26 | `f4687b10bf1a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #159 from 18F/staging | 5 | 221 | 25 | No |
| 2022-07-22 | `68b5275bef80` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #158 from 18F/apb/add-pages-production-concourse-2086 | 2 | 179 | 4 | No |
| 2022-07-22 | `bfe3b4c83a16` | Andrew Burnes <andrew.burnes@gsa.gov> | Upate CI repo info to credhub variables | 1 | 3 | 3 | No |
| 2022-07-21 | `405903fbe1fb` | Andrew Burnes <andrew.burnes@gsa.gov> | Update ci/pipeline.yml | 1 | 1 | 1 | No |
| 2022-07-21 | `fea65761b86d` | Andrew Burnes <andrew.burnes@gsa.gov> | Hardcode GH repo path | 1 | 1 | 1 | No |
| 2022-07-21 | `91e6e1c78295` | Andrew Burnes <andrew.burnes@gsa.gov> | Add job to test PRs | 1 | 54 | 0 | No |
| 2022-07-20 | `a34e7700359a` | Andrew Burnes <andrew.burnes@gsa.gov> | Add pages production concourse jobs and cg vars file | 2 | 125 | 4 | No |
| 2022-07-19 | `0f8c86e3b489` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #157 from 18F/apb/remove-staging-circleci | 1 | 0 | 18 | No |
| 2022-07-18 | `ec55037173d0` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove staging deploy from circleci | 1 | 0 | 18 | No |
| 2022-06-13 | `4a5075a08e17` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #156 from 18F/apb/add-code-ql | 1 | 39 | 0 | No |
| 2022-06-13 | `6f57c6b7013c` | Andrew Burnes <andrew.burnes@gsa.gov> | Add codeql scanning | 1 | 39 | 0 | No |
| 2022-04-27 | `79596db3d30c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #152 from 18F/apb/adjust-memory-3833 | 1 | 2 | 2 | No |
| 2022-04-27 | `7a0d316f8cd9` | Andrew Burnes <andrew.burnes@gsa.gov> | Adjust memory for apps | 1 | 2 | 2 | No |
| 2021-11-23 | `481385af01a6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #106 from 18F/apb/add-security-considerations-action | 1 | 11 | 0 | No |
| 2021-11-22 | `91ffdd386799` | Andrew Burnes <andrew.burnes@gsa.gov> | Add security-considerations-action | 1 | 11 | 0 | No |
| 2020-05-06 | `4659ac630bdb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #58 from 18F/staging | 7 | 86 | 18 | No |
| 2020-05-04 | `6a9dc3ce0433` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #57 from 18F/apb-hsts-update | 7 | 86 | 18 | No |
| 2020-05-01 | `ddb490db034b` | Andrew Burnes <andrew.burnes@gsa.gov> | Add cloud.gov info into README and cleanup tests | 2 | 55 | 9 | No |
| 2020-04-30 | `1948c69c0f9f` | Andrew Burnes <andrew.burnes@gsa.gov> | Add HSTS includeSubDomains on specific cloud.gov host site | 7 | 39 | 17 | No |
| 2020-04-30 | `05b5262f41a5` | Andrew Burnes <andrew.burnes@gsa.gov> | Update HSTS headers | 3 | 5 | 5 | No |
| 2019-04-30 | `a78045123428` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #40 from 18F/apburnes/build-proxy-routes | 3 | 16 | 7 | No |
| 2019-04-23 | `1afd27683722` | Andrew Burnes <andrew.burnes@gsa.gov> | Update production manifest | 1 | 1 | 1 | No |
| 2019-04-23 | `ef88ea4d1a78` | Andrew Burnes <andrew.burnes@gsa.gov> | remove debug headers | 1 | 0 | 3 | No |
| 2019-04-23 | `e440bc6ec599` | Andrew Burnes <andrew.burnes@gsa.gov> | Add routing based on subdomain when subdomain is bucket name | 2 | 18 | 6 | No |

Notes:
* Inspect any commit with `git -C pages-proxy show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-cf-build-tasks`

* Path: `/Users/brianjhurst/Code/pages-cf-build-tasks`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-compact-json, origin/chore-task-tests, origin/dependabot/npm_and_yarn/tasks/a11y/reporter/npm_and_yarn-e7ad013787, origin/dp-fix, origin/fake-debug-branch, origin/fix-zap, origin/main, origin/release, origin/update-chromium, origin/update-zap-reporter
* Remotes: `origin	https://github.com/cloud-gov/pages-cf-build-tasks.git (fetch)`; `origin	https://github.com/cloud-gov/pages-cf-build-tasks.git (push)`
* Matching commit count: 35
* Suspicious commit count: 4
* Timeline: 2024-05-22 to 2026-06-03
* Total files changed across matching commits: 121
* Total insertions/deletions: 1612 / 5157
* Top changed file paths: `tasks/a11y/reporter/package-lock.json` (8), `tasks/owasp-zap/reporter/package-lock.json` (8), `tasks/owasp-zap/reporter/package.json` (8), `tasks/a11y/reporter/package.json` (8), `tasks/a11y/build.sh` (6), `tasks/a11y/definition.py` (6), `CHANGELOG.md` (6), `common/lib/task.py` (6)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-03 | `3889322ff033` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #101 from cloud-gov/chore-a11y-direct-install-chrome-driver | 1 | 48 | 7 | No |
| 2026-06-01 | `e2eee66cfe39` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Explicitly install chrome driver version for a11y tasks | 1 | 48 | 7 | Yes |
| 2026-04-16 | `c94c42f12e6a` | Andrew Burnes <andrew.burnes@gsa.gov> | test: Different chromium install type | 1 | 5 | 0 | Yes |
| 2026-04-09 | `70d121889002` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #97 from cloud-gov/release | 1 | 6 | 0 | No |
| 2026-04-09 | `21ab41015470` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #96 from cloud-gov/fix-axe-core-scan | 8 | 24 | 26 | No |
| 2026-04-07 | `f50c42c0fd0f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Pages CF task axe core scan | 8 | 24 | 26 | No |
| 2026-04-01 | `8d016fa3db1b` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #91 from cloud-gov/release | 1 | 11 | 0 | No |
| 2026-03-17 | `58d2ed878a9c` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #94 from cloud-gov/chore-update-reporter-deps-20260317 | 4 | 306 | 304 | No |
| 2026-03-17 | `2dc590a811b0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update reporter node dependencies | 4 | 306 | 304 | No |
| 2026-03-16 | `504fe3d3f0e4` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #93 from cloud-gov/feat-ci-add-weekly-build-deploy-tasks | 1 | 13 | 0 | No |
| 2026-03-13 | `90ea7702212b` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(ci): Add weekly build and deploy trigger for tasks | 1 | 13 | 0 | No |
| 2026-03-09 | `d81f40c0ea75` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #90 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-cf-build-tasks | 1 | 0 | 14 | No |
| 2025-10-07 | `13eb5d259ff4` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #87 from cloud-gov/release | 1 | 6 | 0 | No |
| 2025-10-02 | `fe421699495e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #86 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `af210bc192c3` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-09-18 | `227e2672d2e5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #82 from cloud-gov/release | 1 | 9 | 0 | No |
| 2025-09-18 | `8d39c846dd95` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #83 from cloud-gov/update-contrib-20250522221653 | 1 | 19 | 0 | No |
| 2025-09-18 | `e0dc5861167f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #85 from cloud-gov/chore-update-report-deps-q4fy25 | 6 | 73 | 149 | Yes |
| 2025-09-17 | `96805ff8a53d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update reporter npm dependencies for Q4 FY25 | 6 | 73 | 149 | Yes |
| 2025-07-07 | `9f1dc71b0bcd` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #84 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `8d5ca6b2aba1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-05-22 | `a159d98a95b3` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Update the CONTRIBUTING.md | 1 | 19 | 0 | No |
| 2024-10-09 | `bff52b463f4f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #67 from cloud-gov/chore-lower-page-limit | 1 | 1 | 1 | No |
| 2024-09-23 | `1912c93328bc` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #53 from cloud-gov/release | 1 | 11 | 0 | No |
| 2024-09-13 | `ebb8ca110f3a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #54 from cloud-gov/chore-update-task-reporter-node-deps-09-12-24 | 12 | 11 | 2000 | No |
| 2024-09-12 | `fbea7ed835c0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update task reporter node dependencies | 12 | 11 | 2000 | No |
| 2024-09-04 | `9679a5e0bba8` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #40 from cloud-gov/release | 1 | 23 | 0 | No |
| 2024-09-04 | `2def433f5c91` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #49 from cloud-gov/feat-update-release | 1 | 4 | 0 | No |
| 2024-09-04 | `b4d1aa77a5b9` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Update release | 1 | 4 | 0 | No |
| 2024-08-22 | `85ab8fc3704a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #43 from cloud-gov/chore-refactor-zap-a11y-task-output | 11 | 139 | 65 | No |
| 2024-07-02 | `a587b867dc5c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor zap and a11y tasks to upload just JSON results | 11 | 139 | 65 | No |
| 2024-05-28 | `c189523a390a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #35 from cloud-gov/fix-set-task-encryption-key | 1 | 1 | 1 | No |
| 2024-05-28 | `b69959dd02c3` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #34 from cloud-gov/feat-decrypt-task-params-and-args | 8 | 128 | 19 | No |
| 2024-05-28 | `a2fc09099cdc` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add self to BaseBuildTask set_encryption_key method | 1 | 1 | 1 | No |
| 2024-05-22 | `cec59582a587` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Decrypt params and args values passed to build task #4509 | 8 | 128 | 19 | No |

Notes:
* Inspect any commit with `git -C pages-cf-build-tasks show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-build-container`

* Path: `/Users/brianjhurst/Code/pages-build-container`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/dependabot/pip/pip-aa7cb66ac2, origin/feat-add-ruby-bigdecimal-to-build-container, origin/main
* Remotes: `origin	https://github.com/cloud-gov/pages-build-container.git (fetch)`; `origin	https://github.com/cloud-gov/pages-build-container.git (push)`
* Matching commit count: 99
* Suspicious commit count: 2
* Timeline: 2019-05-10 to 2026-06-03
* Total files changed across matching commits: 211
* Total insertions/deletions: 3185 / 3026
* Top changed file paths: `ci/pipeline.yml` (32), `requirements.txt` (16), `src/steps/build.py` (14), `Dockerfile` (12), `ci/pipeline-dev.yml` (11), `test/test_build.py` (9), `README.md` (9), `src/build.py` (8)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-03 | `e8f95de2fa04` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #517 from cloud-gov/release | 1 | 6 | 0 | No |
| 2026-05-05 | `745ed9604bf6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #505 from cloud-gov/release | 1 | 17 | 0 | No |
| 2026-05-05 | `bb86dfed80b4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #515 from cloud-gov/update-deps-20260505 | 1 | 5 | 5 | No |
| 2026-05-05 | `e51953adcb74` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update deps requests and cryptography | 1 | 5 | 5 | No |
| 2026-03-17 | `813884b0e9c5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #508 from cloud-gov/chore-add-pagefind-to-build-container | 2 | 34 | 1 | No |
| 2026-01-05 | `36b8c96ac339` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #504 from cloud-gov/fix-prod-pipeline-config-to-use-single-file-config | 4 | 1 | 443 | No |
| 2026-01-05 | `4c71aafca348` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Production CI pipeline to use single file config | 4 | 1 | 443 | No |
| 2026-01-05 | `427b7a041510` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #503 from cloud-gov/release | 1 | 6 | 0 | No |
| 2026-01-05 | `9abe08bed2b2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #502 from cloud-gov/feat-add-node-v24 | 4 | 12 | 12 | No |
| 2026-01-05 | `c761a8e5eaa6` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Node.js v24 as the default node version | 4 | 12 | 12 | Yes |
| 2025-10-07 | `98229aaac1d6` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #500 from cloud-gov/release | 1 | 7 | 0 | No |
| 2025-10-02 | `79de5755a155` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #501 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `5e9fbad7db53` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-09-16 | `be1bfc3c165b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #499 from cloud-gov/chore-bump-boto3-to-50-max-pool-connections | 1 | 7 | 1 | No |
| 2025-09-15 | `34f088b0eb0a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Bump boto3 to 50 max pool connections | 1 | 7 | 1 | No |
| 2025-06-10 | `00b490e9f858` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #496 from cloud-gov/release | 1 | 12 | 0 | No |
| 2025-06-10 | `52a93c9ee8b1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #497 from cloud-gov/update-contrib-20250522220411 | 1 | 13 | 14 | No |
| 2025-06-10 | `dfdfddc2c4e4` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Sets proper headings on CONTRIBUTING.md | 1 | 3 | 3 | No |
| 2025-06-10 | `abae6d9d3aea` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #498 from cloud-gov/chore-update-requests-v2.32.4 | 1 | 1 | 1 | No |
| 2025-06-09 | `20257576aff1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update dependency requests to v2.32.4 | 1 | 1 | 1 | No |
| 2025-05-22 | `f142dd344ad5` | William Zujkowski <153217227+wz-gsa@users.noreply.github.com> | chore: Update CONTRIBUTING.md | 1 | 13 | 14 | No |
| 2025-01-08 | `07eb8b814d1d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #493 from cloud-gov/release | 1 | 6 | 0 | No |
| 2024-12-05 | `00a8917ccbe0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #492 from cloud-gov/chore-set-default-node-v20 | 2 | 5 | 5 | No |
| 2024-12-05 | `4e3caf092bb8` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Install and set default node to v20 | 2 | 5 | 5 | No |
| 2024-09-12 | `5d49db97a613` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #487 from cloud-gov/dependabot-pip-18e15a66a3 | 1 | 1 | 1 | No |
| 2024-09-11 | `cfd669ddfbb7` | Andrew Burnes <andrew.burnes@gsa.gov> | test without hardening | 1 | 15 | 16 | Yes |
| 2024-09-11 | `b522bd9e6572` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add ruby bigdecimal to build container | 1 | 3 | 2 | No |
| 2024-09-04 | `0877a0f6d7b5` | dependabot[bot] <49699333+dependabot[bot]@users.noreply.github.com> | chore: Bump cryptography from 42.0.7 to 43.0.1 in the pip | 1 | 1 | 1 | No |
| 2024-07-03 | `9aa200af4a4f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #481 from cloud-gov/release | 1 | 56 | 0 | No |
| 2024-06-24 | `75831c8891aa` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #480 from cloud-gov/chore-fix-release | 1 | 8 | 0 | No |
| 2024-06-18 | `d9dadd963932` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #471 from cloud-gov/staging | 6 | 60 | 16 | No |
| 2024-06-17 | `b5ea69c8390e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #470 from cloud-gov/fix-build-params-keys-to-decrypt | 1 | 21 | 4 | No |
| 2024-06-13 | `ab92c11f86de` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Decrypt predefined keys in build params | 1 | 21 | 4 | No |
| 2024-06-07 | `d61fc698965b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #469 from cloud-gov/fix-called-process-error-exception | 5 | 39 | 12 | No |
| 2024-06-07 | `fce42fb413ef` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Bump requests to v2.32.3 | 2 | 13 | 2 | No |
| 2024-06-06 | `ab19cfd6c257` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Run build CalledProcessError exception | 4 | 27 | 11 | No |
| 2024-05-21 | `85e753c8aa98` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #467 from cloud-gov/staging | 23 | 648 | 455 | No |
| 2024-05-15 | `206740e6fd1b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #465 from cloud-gov/chore-decrypt-params | 3 | 35 | 4 | No |
| 2024-05-14 | `7d7b17e7cae6` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add decrypt to build site params | 3 | 35 | 4 | No |
| 2024-03-12 | `e7d3cc5adc50` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #457 from cloud-gov/chore-ci-update-general-task-registry-image | 2 | 22 | 4 | No |
| 2024-03-12 | `1b5c8ca9b2bf` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Switch to general-task and registry-image for CI jobs | 2 | 22 | 4 | No |
| 2024-02-16 | `3954574f30af` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #455 from cloud-gov/staging | 10 | 148 | 139 | No |
| 2024-02-16 | `74aa84909389` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #454 from cloud-gov/chore-simplify-ci-notifications | 2 | 43 | 89 | No |
| 2024-02-16 | `fe78d8caafeb` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add hardened git resource | 1 | 9 | 0 | No |
| 2024-02-16 | `0590903195a0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Simplify CI notifications from task hooks | 2 | 34 | 89 | No |
| 2024-01-18 | `54a5bafa89cb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #451 from cloud-gov/staging | 1 | 1 | 0 | No |
| 2024-01-18 | `7de3e02929bd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #450 from cloud-gov/adjust-for-gh-gpg-token-expiration | 1 | 1 | 0 | No |
| 2024-01-18 | `4f23dbb2fedf` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Adjust for Github GPG token expiration | 1 | 1 | 0 | No |
| 2023-12-19 | `f7d4cb176991` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #449 from cloud-gov/staging | 1 | 3 | 1 | No |
| 2023-04-17 | `3390be16566f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #427 from cloud-gov/ci-verify-commit-gpg-key | 1 | 1 | 0 | No |
| 2023-04-17 | `4c383f0a783c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #425 from cloud-gov/feat-add-pr-dev-deployment | 3 | 268 | 2 | No |
| 2023-04-17 | `24f69b8abc49` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 1 | 1 | 0 | No |
| 2023-04-17 | `94df442ef257` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix CI README intro | 1 | 1 | 1 | No |
| 2023-04-13 | `7b67573d453b` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove GH PR status updates since the staging pipeline does this already | 1 | 0 | 32 | No |
| 2023-04-11 | `8c7252be4435` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add dev deployment env for PRs to staging | 3 | 300 | 2 | No |
| 2023-03-30 | `1905c7769d9d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #423 from cloud-gov/staging | 1 | 2 | 1 | No |
| 2023-03-30 | `3c9685a26cac` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #422 from cloud-gov/fix-additional-libs-for-site-builds | 1 | 2 | 1 | No |
| 2023-03-30 | `4ade7ef38edc` | Andrew Burnes <andrew.burnes@gsa.gov> | Add additional image libs | 1 | 2 | 1 | No |
| 2023-03-30 | `386a934f849b` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add additional lib deps for site builds | 1 | 1 | 1 | No |
| 2023-03-22 | `6a94f06e1a43` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #420 from cloud-gov/feat-switch-to-hardened-container | 1 | 6 | 1 | No |
| 2023-03-22 | `340ca8c7ea67` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Switch to using harden container for cf-image | 1 | 6 | 1 | No |
| 2023-03-14 | `c8aff5b38711` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #414 from cloud-gov/fix-app-deploy-params | 2 | 1 | 3 | No |
| 2023-03-14 | `66c827a35ee2` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Remove stack param since it is docker image | 2 | 1 | 3 | No |
| 2023-03-14 | `753fd297454f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #413 from cloud-gov/chore-update-app-stack-cflinuxfs4 | 10 | 17 | 262 | No |
| 2023-03-14 | `f96e7f98ee11` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update tests to account for request timeout kwarg addition | 2 | 11 | 5 | No |
| 2023-03-14 | `43839576fc1b` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add timeout to requests based on bandit findings | 3 | 4 | 3 | No |
| 2023-03-14 | `48985582c33f` | Andrew Burnes <andrew.burnes@gsa.gov> | update: Parameterize stack with CF_STACK and remove unused federalist deployments | 6 | 2 | 255 | No |
| 2023-03-13 | `787b074bc233` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update app stack to cflinuxfs4 | 1 | 2 | 1 | No |
| 2023-02-03 | `64b3e2dc6b50` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #401 from cloud-gov/staging | 1 | 28 | 48 | No |
| 2023-02-03 | `c360190b2f20` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #402 from cloud-gov/fix-ci-slack-success-emoji | 1 | 1 | 1 | No |
| 2023-02-03 | `c76d393a6c92` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI slack emoji for successful nightly restage | 1 | 1 | 1 | No |
| 2023-02-02 | `61e69e95b247` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #400 from cloud-gov/fix-ci-restage-nightly-job | 1 | 5 | 0 | No |
| 2023-02-02 | `8aa107373112` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI pipeline to properly use src input for nightly rebuild | 1 | 5 | 0 | No |
| 2023-01-30 | `6d113a7520e3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #399 from cloud-gov/ci-update-nightly-rebuild-step | 1 | 24 | 49 | No |
| 2023-01-30 | `1c4a654f7e53` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Remove test-nightly job and update nightly job to use cf restage | 1 | 12 | 42 | No |
| 2023-01-30 | `841a8dd9a221` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Update nightly deploy to just redeploy app | 1 | 22 | 17 | No |
| 2023-01-06 | `3401f18c7d48` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #388 from cloud-gov/staging | 7 | 54 | 4 | No |
| 2023-01-05 | `09f7c3d3d74b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #387 from cloud-gov/chore-add-gem-update-for-jeykll | 2 | 5 | 1 | No |
| 2023-01-05 | `bb4f163a0571` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into chore-add-gem-update-for-jeykll | 3 | 8 | 4 | No |
| 2023-01-05 | `6d416ab3a334` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update tests with additional mock calls | 1 | 3 | 1 | No |
| 2023-01-05 | `980c7efc953a` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Remove f-string for gem update command | 1 | 1 | 1 | No |
| 2023-01-05 | `a861e1bd00c6` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add gem update --system for Jekyll builds | 1 | 2 | 0 | No |
| 2022-08-18 | `72c09a24aa11` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #373 from 18F/apb/fix-gh-status-for-real | 1 | 2 | 6 | No |
| 2022-08-18 | `d5600c40853a` | Andrew Burnes <andrew.burnes@gsa.gov> | Use correct put resource and switch to just state params | 1 | 2 | 6 | No |
| 2022-08-18 | `546e070cf645` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #372 from 18F/apb/report-staging-gh-status-on-success | 1 | 11 | 1 | No |
| 2022-08-17 | `e39d7f2bff62` | Andrew Burnes <andrew.burnes@gsa.gov> | Report back to GH status of sucessfull test for a branch | 1 | 11 | 1 | No |
| 2022-08-17 | `cb87b37f9a00` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #370 from 18F/apb/match-pages-prod-env_postfix | 1 | 1 | 1 | No |
| 2022-08-17 | `c3dff2d87984` | Andrew Burnes <andrew.burnes@gsa.gov> | Add env_postfix -production to match pipeline deploy CF_APP name | 1 | 1 | 1 | No |
| 2022-08-17 | `35d77f4e1f62` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #369 from 18F/staging | 7 | 454 | 361 | No |
| 2022-08-15 | `55410d557c64` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #365 from 18F/bh-federalist-pipeline | 2 | 256 | 13 | No |
| 2022-05-04 | `2f6365867b5b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #358 from 18F/apb/add-codeql | 1 | 38 | 0 | No |
| 2022-05-04 | `aa4ab61e86ff` | Andrew Burnes <andrew.burnes@gsa.gov> | Add codeql GH action | 1 | 38 | 0 | No |
| 2022-01-11 | `7b3ed5fcba99` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #340 from 18F/ar/pr-template | 1 | 7 | 0 | No |
| 2021-12-16 | `e9d20ecf5f3d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'staging' into ar/pr-template | 2 | 12 | 6 | No |
| 2021-04-09 | `338809f7f9b1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #322 from 18F/dc/configure-home-dir | 2 | 5 | 1 | No |
| 2019-05-13 | `4daf1eb9fb35` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up bandit scan | 2 | 4 | 5 | No |
| 2019-05-13 | `f8a370b609ee` | Andrew Burnes <andrew.burnes@gsa.gov> | fix line length in test | 1 | 1 | 1 | No |
| 2019-05-10 | `9587c4103749` | Andrew Burnes <andrew.burnes@gsa.gov> | Change to /404.html from /404/index.html | 2 | 6 | 7 | No |
| 2019-05-10 | `f2462bec5c67` | Andrew Burnes <andrew.burnes@gsa.gov> | Add 404 when not present in build | 3 | 89 | 48 | No |

Notes:
* Inspect any commit with `git -C pages-build-container show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-site-gantry`

* Path: `/Users/brianjhurst/Code/pages-site-gantry`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-Update-Pages-ci-pipelines-to-use-the-same-creds-value-for-Github-2839, origin/chore-refactor-payload-preview, origin/dependabot/npm_and_yarn/npm_and_yarn-db35b1c8a5, origin/dp-update, origin/feat-add-breadcrumbs, origin/feat-add-posts-section, origin/feat-add-side-nav-to-single-pages, origin/feat-add-theming, origin/fix-refactor-payload-fetch, origin/main (+5 more)
* Remotes: `origin	https://github.com/cloud-gov/pages-site-gantry.git (fetch)`; `origin	https://github.com/cloud-gov/pages-site-gantry.git (push)`
* Matching commit count: 66
* Suspicious commit count: 3
* Timeline: 2025-05-23 to 2026-06-03
* Total files changed across matching commits: 762
* Total insertions/deletions: 39149 / 24265
* Top changed file paths: `src/layouts/Layout.astro` (24), `package-lock.json` (20), `astro.config.ts` (19), `src/content.config.ts` (18), `package.json` (17), `ci/pipeline.yml` (13), `README.md` (12), `src/pages/events/[slug].astro` (11)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-06-03 | `50a66b4558c7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #207 from cloud-gov/release | 3 | 101 | 7 | No |
| 2026-06-01 | `4738bcbb39d9` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #230 from cloud-gov/chore-refactor-site-theming-styles | 34 | 645 | 321 | Yes |
| 2026-05-26 | `9060d63a6219` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor site theming styles config | 34 | 645 | 321 | Yes |
| 2026-05-18 | `2e8989305980` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #226 from cloud-gov/chore-upgrade-astro-v6 | 72 | 4814 | 6293 | No |
| 2026-05-18 | `27abe31e82d3` | Kevin Masters <kevin.masters@gsa.gov> | fix: component scss causing transport timeout | 2 | 39 | 40 | No |
| 2026-05-14 | `0ef1afde984a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update tests to account for astro v6 test config to node | 14 | 873 | 321 | No |
| 2026-05-13 | `53c460f0b115` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update README | 1 | 1 | 0 | No |
| 2026-05-11 | `583ed0822b21` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Upgrade astro to v6 | 62 | 4771 | 6802 | No |
| 2026-03-17 | `5d1a7c201b6c` | William Zujkowski <william.zujkowski@gsa.gov> | chore(ci): Remove deprecated security-considerations automation | 1 | 0 | 8 | No |
| 2026-03-17 | `1986fb8d28df` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #203 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-site-gantry | 1 | 0 | 8 | No |
| 2026-03-13 | `f73ec3434c3f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #200 from cloud-gov/release | 3 | 202 | 6 | No |
| 2026-03-13 | `eb4b90bfe41a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #198 from cloud-gov/feat-ci-add-release-tasks | 2 | 117 | 0 | No |
| 2026-03-12 | `2d69224a18f6` | Andrew Burnes <andrew.burnes@gsa.gov> | feat(ci): Add release deployment pipeline | 2 | 117 | 0 | No |
| 2026-03-10 | `e964e95eb1c0` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #195 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-site-gantry | 1 | 0 | 14 | No |
| 2026-03-05 | `fd4190bbb573` | William Zujkowski <william.zujkowski@gsa.gov> | chore: Remove deprecated security-considerations automation files | 1 | 0 | 14 | No |
| 2026-02-12 | `6961dab294a6` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #186 from cloud-gov/dependabot/npm_and_yarn/npm_and_yarn-df2a24b344 | 1 | 14 | 14 | No |
| 2026-02-05 | `076e640e4f5e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #181 from cloud-gov/dependabot/npm_and_yarn/npm_and_yarn-1b92d517bd | 1 | 3 | 3 | No |
| 2026-02-04 | `9f6eea177482` | Andrew Burnes <apburnes@gmail.com> | chore: Optionally render the hero button if text and url not set (#175) | 6 | 1134 | 9 | No |
| 2026-01-08 | `e1503c685c44` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #171 from cloud-gov/fix-preview-image-links | 4 | 56 | 46 | No |
| 2026-01-08 | `e6d3201085d5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #159 from cloud-gov/feat-Create-filtering-component-126 | 63 | 5815 | 1396 | No |
| 2026-01-08 | `df7e554fa333` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Preview deployment image paths and static file serving | 4 | 56 | 46 | No |
| 2026-01-08 | `91b367d134e7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #170 from cloud-gov/feat-use-slug-title-in-breadcrumb | 12 | 68 | 53 | No |
| 2026-01-07 | `2bcf6d95a248` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: User page title in breadcrumb on slug pages | 12 | 68 | 53 | No |
| 2026-01-07 | `c264d41ccca3` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #165 from cloud-gov/fix-card-description-string-check | 1 | 2 | 1 | No |
| 2026-01-05 | `c80d169c9831` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #158 from cloud-gov/feat-add-404-page | 4 | 53 | 0 | No |
| 2025-12-29 | `6baaaefaf26f` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Homepage card description to check string type | 1 | 2 | 1 | No |
| 2025-12-03 | `f2677811c3dd` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #137 from cloud-gov/chore-refactor-payload-preview-reload-on-preview-mode | 20 | 353 | 198 | No |
| 2025-12-03 | `92d0cd2e5b6e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor PayloadPreview to render when PREVIEW_MODE is true | 20 | 353 | 198 | No |
| 2025-10-29 | `8928a80336ee` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Refactor payload preview to only initiate in layout when in preview mode | 9 | 27 | 26 | No |
| 2025-10-28 | `274acfd4faf4` | Andrew Burnes <andrew.burnes@gsa.gov> | test commit | 44 | 382 | 335 | No |
| 2025-10-28 | `2f617ee0448e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #123 from cloud-gov/chore-ci-rework-preview-app-deploy-and-delete | 6 | 103 | 8 | No |
| 2025-10-27 | `27121c3557df` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Rework the preview app deploy and delete pipelines | 6 | 103 | 8 | No |
| 2025-10-24 | `b452d069f49c` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #121 from cloud-gov/fix-astro-config | 1 | 5 | 17 | No |
| 2025-10-24 | `9928b1665d4b` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Astro config to build CSS properly | 1 | 5 | 17 | No |
| 2025-10-23 | `9e6650537dd5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #110 from cloud-gov/feat-add-hero-and-card-grid-to-page | 14 | 859 | 450 | No |
| 2025-10-21 | `c16c263d5361` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #116 from cloud-gov/fix-ci-add-clear-buildpack-cache-check | 1 | 7 | 4 | No |
| 2025-10-21 | `9768109c6aa6` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #115 from cloud-gov/fix-search-baseurl | 1 | 1 | 1 | No |
| 2025-10-21 | `954825cf6cfd` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Add clear buildpack cache check to ci | 1 | 7 | 4 | No |
| 2025-10-21 | `0be24702ad6d` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Search baseUrl when BASEURL env var is undefined | 1 | 1 | 1 | No |
| 2025-10-15 | `1fc32b685136` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Enable custom home page layout | 14 | 859 | 450 | No |
| 2025-10-10 | `c26d0cf1746e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #105 from cloud-gov/feat-update-events-area | 12 | 2296 | 23 | No |
| 2025-10-09 | `60a4143aed3a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #106 from cloud-gov/chore-add-staging-ci | 65 | 1471 | 1347 | No |
| 2025-10-09 | `8a38588ed2f2` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Run prettier formatting | 57 | 908 | 628 | No |
| 2025-10-08 | `51f11c81a6d0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add staging ci deployment | 9 | 565 | 721 | No |
| 2025-09-12 | `71dc74ca603a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #74 from cloud-gov/feat-add-two-color-and-font-theming | 7 | 210 | 146 | No |
| 2025-09-11 | `37c9c97c564d` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add two color and font theming from site config | 7 | 210 | 146 | No |
| 2025-09-08 | `f5a5c080206f` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #68 from cloud-gov/feat-add-breadcrumbs-original | 2 | 96 | 1 | No |
| 2025-09-08 | `b21cd14506dc` | Jonathan Bobel <jonathan.bobel@gsa.gov> | fix: Slight change to BASEURL var | 1 | 1 | 1 | No |
| 2025-09-05 | `ddf4909d8aaf` | Jonathan Bobel <jonathan.bobel@gsa.gov> | chore: Removing home breadcrumb in preview environment | 2 | 25 | 23 | No |
| 2025-09-05 | `5f34b41a22b1` | Jonathan Bobel <jonathan.bobel@gsa.gov> | chore: Changing API call to build from URL path | 1 | 29 | 28 | No |
| 2025-09-04 | `c27bbc34d341` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #66 from cloud-gov/fix-media-url-rich-text | 2 | 17 | 5 | No |
| 2025-09-04 | `c8a9aceca126` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Add breadcrumbs to site | 2 | 92 | 0 | No |
| 2025-09-04 | `d20a81190494` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Media URL utility in RichText component | 2 | 17 | 5 | No |
| 2025-09-04 | `cfd1e94803a6` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add menu to astro content validation | 4 | 153 | 88 | No |
| 2025-09-03 | `14a3eedd77e9` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Adding dropdown capability to main nav | 1 | 35 | 0 | No |
| 2025-09-02 | `a61d6a26a6e2` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #64 from cloud-gov/feat-add-leadership-collection-page | 10 | 349 | 19 | No |
| 2025-08-29 | `97ffbcacc3e3` | Jonathan Bobel <jonathan.bobel@gsa.gov> | feat: Add leadership collection to content | 10 | 349 | 19 | No |
| 2025-08-19 | `7054fd19186c` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #49 from cloud-gov/feat-render-cms-media-uploadst | 7 | 274 | 8 | No |
| 2025-08-15 | `602f3f64e3b4` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Render CMS Media uploads in site | 7 | 274 | 8 | No |
| 2025-07-29 | `41fe82fa9d68` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #30 from cloud-gov/feat-add-reports-pages | 34 | 4547 | 1772 | No |
| 2025-07-23 | `82d44a09013f` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add reports pages | 34 | 4547 | 1772 | Yes |
| 2025-07-07 | `38876dd44dc0` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #29 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `7d1084afddba` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-06-26 | `95cf26ec6b9a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #23 from cloud-gov/fix-ci-preview-launch-bucket-prefix | 1 | 2 | 0 | No |
| 2025-06-17 | `ad607b74e972` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI preview launch bucket prefix | 1 | 2 | 0 | No |
| 2025-05-23 | `d8fb53f8828d` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #19 from cloud-gov/update-contrib-20250522221653 | 1 | 13 | 11 | No |

Notes:
* Inspect any commit with `git -C pages-site-gantry show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-pipeline-tasks`

* Path: `/Users/brianjhurst/Code/pages-pipeline-tasks`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/add-readme, origin/chore-add-local-set-pipeline-example, origin/chore-multi-env-pipeline, origin/feat-add-get-app-env-task, origin/initial-tasks, origin/main
* Remotes: `origin	https://github.com/cloud-gov/pages-pipeline-tasks.git (fetch)`; `origin	https://github.com/cloud-gov/pages-pipeline-tasks.git (push)`
* Matching commit count: 29
* Suspicious commit count: 0
* Timeline: 2024-06-24 to 2026-03-17
* Total files changed across matching commits: 53
* Total insertions/deletions: 538 / 71
* Top changed file paths: `README.md` (13), `tasks/get-app-env.yml` (8), `scripts/get-app-env.sh` (8), `overlays/resource-templates-registry.yml` (4), `tasks/run-command.yml` (4), `.github/workflows/security-considerations.yml` (3), `CODEOWNERS` (2), `tasks/npm-audit.yml` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `c217b3014530` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #34 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-pipeline-tasks | 1 | 0 | 8 | No |
| 2026-03-09 | `182d7dbc5261` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #32 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-pipeline-tasks | 1 | 0 | 14 | No |
| 2026-01-12 | `d6117309208a` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #29 from cloud-gov/feat-add-node-v24-and-docs-update | 2 | 26 | 1 | No |
| 2026-01-12 | `4ae407c1108f` | Andrew Burnes <apburnes@gmail.com> | fix: README language | 1 | 1 | 1 | No |
| 2026-01-12 | `f6b2c264a99c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add node v24, set node default to v20, and add docs on pipeline setup | 2 | 26 | 1 | No |
| 2025-10-09 | `ab1a5d1b5ce0` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #28 from cloud-gov/feat-add-node-v22-resource | 1 | 1 | 0 | No |
| 2025-10-08 | `bcbf911ce279` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #27 from cloud-gov/chore-add-docs-on-ytt-pipeline-creation | 1 | 17 | 0 | No |
| 2025-10-08 | `c6d8dbb79849` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Nodejs v22 container resource | 1 | 1 | 0 | No |
| 2025-10-08 | `44b34efba5b0` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add docs on how to create a new pipeline with YTT | 1 | 17 | 0 | No |
| 2025-10-02 | `2c4fdb87af82` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #26 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `205fee6c5bcf` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-07-07 | `fd124ab9769e` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #25 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `d4a3efe6b6c1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-06-17 | `11e699848c9e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add local set pipeline example to docs | 1 | 25 | 0 | No |
| 2025-05-23 | `6b2b082a6fe7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #21 from cloud-gov/update-contrib-20250522221653 | 1 | 13 | 11 | No |
| 2024-07-09 | `1064b9a3d126` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #12 from cloud-gov/chore-add-ouput-to-command-task | 1 | 2 | 0 | No |
| 2024-07-08 | `3ce1f5130e9d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add output to src resource to pass any files created by command | 1 | 2 | 0 | No |
| 2024-07-01 | `b9236f1bb634` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #9 from cloud-gov/fix-get-app-env-script-exec-path | 1 | 3 | 1 | No |
| 2024-07-01 | `0022d03d3f49` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #8 from cloud-gov/feat-add-npm-audit-bash-command-tasks | 5 | 61 | 1 | No |
| 2024-07-01 | `d92a842a29fe` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Set get-app-env to proper path and output src | 1 | 3 | 1 | No |
| 2024-06-27 | `f0a39f0b2401` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add npm audit and run bash command tasks | 5 | 61 | 1 | No |
| 2024-06-27 | `810be9be3652` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #7 from cloud-gov/fix-set-app-env-output-to-src | 3 | 3 | 2 | No |
| 2024-06-27 | `d43d4c9194d7` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #6 from cloud-gov/fix-get-app-env-permissions | 1 | 0 | 0 | No |
| 2024-06-27 | `e3e509746ddd` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #5 from cloud-gov/chore-multi-env-pipeline | 5 | 71 | 10 | No |
| 2024-06-27 | `1d48b493a3d7` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Write .env output to src directory root for subsequent tasks | 3 | 3 | 2 | No |
| 2024-06-26 | `a1ce811051d1` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #4 from cloud-gov/feat-add-get-app-env-task | 3 | 80 | 0 | No |
| 2024-06-26 | `2fb65c14b651` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Set correct permission on get-app-env script | 1 | 0 | 0 | No |
| 2024-06-26 | `fea7415dff7c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add get-app-env task | 3 | 80 | 0 | No |
| 2024-06-24 | `4907c5a01bfb` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #3 from cloud-gov/chore-small-updates-for-cf-task | 3 | 34 | 17 | No |

Notes:
* Inspect any commit with `git -C pages-pipeline-tasks show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-gpg-keys`

* Path: `/Users/brianjhurst/Code/pages-gpg-keys`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/chore-ci-update-general-task-registry-image, origin/chore-set-security-considerations-read-only, origin/chore-update-ci-resources-to-hardened-images, origin/ci-verify-commit-gpg-key, origin/cleanup/security-considerations/cloud-gov-pages-gpg-keys, origin/main
* Remotes: `origin	https://github.com/cloud-gov/pages-gpg-keys.git (fetch)`; `origin	https://github.com/cloud-gov/pages-gpg-keys.git (push)`
* Matching commit count: 12
* Suspicious commit count: 0
* Timeline: 2023-04-18 to 2026-03-17
* Total files changed across matching commits: 12
* Total insertions/deletions: 84 / 32
* Top changed file paths: `ci/pipeline.yml` (6), `.github/workflows/security-considerations.yml` (3), `CODEOWNERS` (2), `.github/workflows/security-considerations.properties.json` (1)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `8c25b3be042b` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #10 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-gpg-keys | 1 | 0 | 8 | No |
| 2026-03-09 | `c1c0597ec2db` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #8 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-gpg-keys | 1 | 0 | 14 | No |
| 2025-10-02 | `e433bf3959a5` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #6 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `64ce00ece432` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-07-07 | `72a1379837db` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #5 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `d062e24c0e6c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2024-03-13 | `1492b5633bc6` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #4 from cloud-gov/chore-ci-update-general-task-registry-image | 1 | 11 | 2 | No |
| 2024-03-13 | `d5013dc9d8d1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Switch to general-task and registry-image for CI jobs | 1 | 11 | 2 | No |
| 2024-02-15 | `4ba43b6363b2` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #3 from cloud-gov/chore-update-ci-resources-to-hardened-images | 1 | 23 | 0 | No |
| 2024-02-15 | `80fff4274f3e` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update CI resource types to hardened images | 1 | 23 | 0 | No |
| 2023-04-18 | `bb278a966c22` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #1 from cloud-gov/ci-verify-commit-gpg-key | 1 | 4 | 3 | No |
| 2023-04-18 | `b11a3cb11d9f` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 1 | 4 | 3 | No |

Notes:
* Inspect any commit with `git -C pages-gpg-keys show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-studio-crawler`

* Path: `/Users/brianjhurst/Code/pages-studio-crawler`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-update-node-and-npm-npm-to-harden-the-npmrc-file-2953, origin/dependabot/npm_and_yarn/npm_and_yarn-fdf8171dcb, origin/main
* Remotes: `origin	git@github.com:cloud-gov/pages-studio-crawler.git (fetch)`; `origin	git@github.com:cloud-gov/pages-studio-crawler.git (push)`
* Matching commit count: 0
* Suspicious commit count: 0
* Timeline: none to none
* Total files changed across matching commits: 0
* Total insertions/deletions: 0 / 0
* Top changed file paths: None

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| - | - | - | No matching commits | 0 | 0 | 0 | No |

Notes:
* No matching author or committer entries were found on local reachable refs.

### `pages-redirects`

* Path: `/Users/brianjhurst/Code/pages-redirects`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin/88-rm-old-federalist-bucket, origin, origin/ads-bpa-paid-proto, origin/agile-bpa, origin/amir-pages, origin/amir-test, origin/amirbey-patch-1, origin/apb/redirect-govconnect, origin/apply-pif, origin/ar/remove-connect.gov, origin/ar/remove-federalist-templates (+38 more)
* Remotes: `origin	https://github.com/cloud-gov/pages-redirects.git (fetch)`; `origin	https://github.com/cloud-gov/pages-redirects.git (push)`
* Matching commit count: 105
* Suspicious commit count: 1
* Timeline: 2021-01-27 to 2026-03-17
* Total files changed across matching commits: 290
* Total insertions/deletions: 9796 / 8676
* Top changed file paths: `templates/_federalist-redirects.njk` (56), `docker-compose.yml` (49), `templates/manifest-prod.yml.njk` (33), `ci/pipeline.yml` (27), `test/integration/test_federalist_redirects.js` (19), `package.json` (12), `docker/Dockerfile-test_client` (9), `README.md` (8)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `138d09fc5e93` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #281 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-redirects | 4 | 28 | 30 | No |
| 2026-03-17 | `49713a3c3745` | William Zujkowski <william.zujkowski@gsa.gov> | chore(ci): remove deprecated security-considerations automation | 4 | 28 | 30 | No |
| 2026-03-09 | `68dd921a4b56` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #279 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-redirects | 1 | 0 | 15 | No |
| 2025-10-02 | `9d12ff17ebb3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #276 from cloud-gov/chore-add-codeowners | 1 | 2 | 0 | No |
| 2025-10-02 | `1ce5407901da` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 2 | 0 | No |
| 2025-08-14 | `096747f6f22f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #275 from cloud-gov/feat-remove-www.search.gov | 4 | 0 | 12 | No |
| 2025-08-14 | `4d65e6479251` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Remove www.search.gov redirect | 4 | 0 | 12 | No |
| 2025-07-07 | `335dff74f9ee` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #274 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `ff6a2ef1b79a` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-06-26 | `8455be3962d1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #273 from cloud-gov/feat-remove-modularcontracting.18f.gov | 2 | 0 | 3 | No |
| 2025-06-24 | `2f185051d836` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Remove modularcontracting.18f.gov redirect | 2 | 0 | 3 | No |
| 2025-06-10 | `d8ca089311ff` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #272 from cloud-gov/chore-remove-federalistapp.18f.gov | 1 | 0 | 1 | No |
| 2025-06-10 | `52c03018dc4f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove federalistapp.18f.gov redirect | 1 | 0 | 1 | No |
| 2025-05-07 | `97d09fbbc802` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #269 from cloud-gov/chore-remove-additional-deprecated-digital-gov-redirects | 4 | 0 | 56 | No |
| 2025-05-06 | `1bc9c536652f` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove additional deprecated digital.gov redirects | 4 | 0 | 56 | No |
| 2025-04-29 | `90947e0c7825` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #268 from cloud-gov/feat-deprecate-old-digitalgov-redirects | 4 | 2 | 49 | No |
| 2025-04-28 | `49d787fcfcc7` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Deprecate old digital.gov redirects | 4 | 2 | 49 | No |
| 2025-04-16 | `23c852aaa1ec` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #267 from cloud-gov/chore-remove-unresolvable-18f-redirects | 4 | 1 | 453 | No |
| 2025-04-11 | `c35bcd1f6077` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove unresolvable 18F redirects | 4 | 1 | 453 | No |
| 2025-04-07 | `49c64a8fdc76` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #266 from cloud-gov/feat-add-fehrm-apex-to-www | 3 | 10 | 0 | No |
| 2025-04-07 | `38f1fac838b7` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add fehrm apex to www redirect | 3 | 10 | 0 | No |
| 2025-03-11 | `c4f677e679c1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #265 from cloud-gov/chore-switch-code-gov-redirect-destination | 1 | 4 | 4 | No |
| 2025-03-11 | `d881bf859d80` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Switch code.gov redirects destination | 1 | 4 | 4 | No |
| 2025-03-10 | `88e02a379416` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #264 from cloud-gov/feat-add-code-gov-redirects | 3 | 40 | 0 | No |
| 2025-03-10 | `a50b95db00da` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add code.gov redirect to digital.gov | 3 | 40 | 0 | No |
| 2025-01-15 | `9ce89d3b9ab1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #263 from cloud-gov/fix-update-to-use-request-uri | 2 | 14 | 43 | No |
| 2025-01-15 | `a76b10434de6` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Update applicable redirects to use $request_uri | 2 | 14 | 43 | No |
| 2024-11-20 | `2d581a5ed93a` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #262 from cloud-gov/chore-remove-c2.18f.gov | 3 | 0 | 9 | No |
| 2024-11-20 | `3e6bc184b3b8` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove defunct c2.18f.gov | 3 | 0 | 9 | No |
| 2024-11-04 | `d65f817e8749` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #261 from cloud-gov/feat-add-demo.pra.digital.gov-redirect | 3 | 10 | 0 | No |
| 2024-11-04 | `bd45ebf3c358` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add demo.pra.digital.gov redirect to pra.digital.gov | 3 | 10 | 0 | No |
| 2024-09-16 | `2ad67c2555ae` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #258 from cloud-gov/feat-join.tts.gsa.gov-additional-redirects | 1 | 8 | 0 | No |
| 2024-09-13 | `fc5dfc3d900a` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add additional join.tts.gsa.gov redirects | 1 | 8 | 0 | No |
| 2024-09-13 | `0e974ae577fb` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #256 from cloud-gov/feat-tts-join | 4 | 28 | 2 | No |
| 2024-09-13 | `e97310f7fc27` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #257 from cloud-gov/feat-add-18f.gov/chat-redirect | 3 | 12 | 3 | No |
| 2024-09-13 | `f4acfcc2ad71` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add (www.)18f.gov/chat redirect to google form | 3 | 12 | 3 | No |
| 2024-07-11 | `9941549e7b54` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #252 from cloud-gov/fix-ci-add-app-name-to-nightly-restage-task | 1 | 1 | 0 | No |
| 2024-07-10 | `cf8ae65a585a` | Andrew Burnes <andrew.burnes@gsa.gov> | fix(ci): Add CF_APP_NAME param to nightly restage task | 1 | 1 | 0 | No |
| 2024-07-09 | `25a28d8abc3b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #251 from cloud-gov/chore-ci-refactor-pipelines | 3 | 45 | 63 | No |
| 2024-07-08 | `b5abe7a0be27` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Refactor the ci pipeline to improve dry-ness | 3 | 45 | 63 | No |
| 2024-05-13 | `bee6ab66d26c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #248 from cloud-gov/feat-add-identityequitystudy.gsa.gov | 3 | 12 | 0 | No |
| 2024-05-13 | `ffa282e4e611` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add identityequitystudy.gsa.gov redirect | 3 | 12 | 0 | No |
| 2024-03-26 | `5b83744db0d0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #243 from cloud-gov/add-www.usability.gov-and-accessibility.digital.gov | 4 | 29 | 4 | No |
| 2024-03-26 | `a5128a45ae05` | Andrew Burnes <andrew.burnes@gsa.gov> | adds www.usability.gov and accessibility.digital.gov redirects | 4 | 29 | 4 | No |
| 2024-03-13 | `cae81e450f15` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #241 from cloud-gov/chore-ci-update-general-task-registry-image | 1 | 11 | 2 | No |
| 2024-03-12 | `64f4addead68` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Switch to general-task and registry-image for CI jobs | 1 | 11 | 2 | No |
| 2024-03-04 | `210c12cac861` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #239 from cloud-gov/feat-add-methods-18f-gov-redirect | 2 | 12 | 1 | No |
| 2024-03-04 | `915acc5e3969` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add methods.18f.gov redirect to guides.18f.gov/methods | 2 | 12 | 1 | No |
| 2024-02-15 | `68a070ff5561` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #237 from cloud-gov/chore-update-ci-resources-to-hardened-images | 2 | 49 | 46 | No |
| 2024-02-15 | `bb139eee3d26` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update CI to use hardened resource images | 2 | 49 | 46 | No |
| 2024-01-19 | `333fe30f29f1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #234 from cloud-gov/peterrowland-atf-eregs-perm-redirect | 3 | 4 | 4 | No |
| 2024-01-16 | `38b4d5f1abc7` | Peter Rowland <peter.rowland@gsa.gov> | re-enable atf-eregs redirect | 3 | 4 | 4 | No |
| 2023-11-14 | `fddd2cc80b9c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #226 from cloud-gov/eg-agile-guide-redirect | 2 | 11 | 0 | No |
| 2023-11-13 | `38b954f68e2f` | Andrew Burnes <andrew.burnes@gsa.gov> | Add agile.18f.gov to docker-compose file | 1 | 1 | 0 | No |
| 2023-10-25 | `5b9fbe13c243` | eric-gade <eric.gade@gsa.gov> | Updating agile guide subdomain requests to redirect and rewrite | 1 | 10 | 0 | No |
| 2023-10-19 | `d67bc8db6f8b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #224 from cloud-gov/chore-remove-guides.18f.gov | 5 | 0 | 72 | No |
| 2023-10-19 | `190d8cf54501` | Andrew Burnes <apburnes@gmail.com> | chore: Remove guides.18f.gov | 5 | 0 | 72 | No |
| 2023-10-11 | `9c296c1c8272` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #222 from cloud-gov/guides.18f.gov-redirects | 1 | 53 | 3 | No |
| 2023-09-28 | `eb0f14b15d59` | eric-gade <eric.gade@gsa.gov> | Switch to use existing $scheme and add fallback | 1 | 13 | 11 | No |
| 2023-09-28 | `cd9fb2d5cc3e` | eric-gade <eric.gade@gsa.gov> | Updating new guides.18f.gov redirects | 1 | 49 | 1 | No |
| 2023-09-19 | `7835a70af7cc` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #220 from cloud-gov/chore-update-stack-cflinuxfs4-219 | 12 | 2966 | 1718 | No |
| 2023-09-19 | `5f1539c0c740` | Andrew Burnes <apburnes@gmail.com> | chore: Test node v20 bullseye slim | 4 | 5 | 5 | No |
| 2023-09-19 | `39f30aac7390` | Andrew Burnes <apburnes@gmail.com> | chore: Update update stack and node testing deps #219 | 12 | 2965 | 1717 | No |
| 2023-05-31 | `08be978a601e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #215 from cloud-gov/aduth-design.login.gov-redirect | 3 | 9 | 0 | No |
| 2023-05-05 | `57ca332e98af` | Andrew Duthie <andrew.duthie@gsa.gov> | Signed add design.login.gov redirect configuration | 3 | 9 | 0 | No |
| 2023-04-19 | `b8f006670861` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #212 from cloud-gov/remove-federalist-docs.18f.gov-redirect | 1 | 0 | 1 | No |
| 2023-04-19 | `be215fe49e40` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Remove federalist-docs.18f.gov redirect | 1 | 0 | 1 | No |
| 2023-04-17 | `a9cabf88b2a1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #211 from cloud-gov/ci-verify-commit-gpg-key | 1 | 1 | 0 | No |
| 2023-04-17 | `17025c919535` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 1 | 1 | 0 | No |
| 2023-04-10 | `ab8d5027f458` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #210 from cloud-gov/feat-add-federalistapp-redirect-to-pages | 2 | 5 | 5 | No |
| 2023-04-10 | `85576ecfc862` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Docker compose tests | 1 | 1 | 1 | No |
| 2023-04-10 | `142e5ed08567` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add redirect for fedearlistapp.18f.gov to pages.cloud.gov | 1 | 4 | 4 | No |
| 2023-03-22 | `fba79c8100cd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #209 from cloud-gov/feat-switch-to-hardened-container | 1 | 6 | 2 | No |
| 2023-03-22 | `d93ca2b3c2f9` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Switch to using harden container for cf-image | 1 | 6 | 2 | No |
| 2023-01-30 | `5cce1f2911b7` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #208 from cloud-gov/rebased-ryanwoldatwork_us-digital-registry-staging-redirects | 3 | 10 | 0 | No |
| 2023-01-20 | `84f5a3c2dc74` | Andrew Burnes <andrew.burnes@gsa.gov> | clean up redirect config | 3 | 2 | 5 | No |
| 2023-01-20 | `286a5914a83b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #201 from ryanwoldatwork/us-digital-registry-staging-redirects | 3 | 13 | 0 | No |
| 2023-01-19 | `3d35fb8d569a` | Ryan Wold <ryan.wold@gsa.gov> | usdr redirect to touchpoints | 5 | 9 | 6 | No |
| 2023-01-19 | `5c32f1028608` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #206 from cloud-gov/ci-migrate-to-concourse-205 | 10 | 522 | 93 | No |
| 2023-01-18 | `3e70b47abbc4` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Update PR/branch status checks | 1 | 35 | 35 | No |
| 2023-01-18 | `34488d5bc099` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Remove circleci and update README | 2 | 38 | 57 | No |
| 2023-01-18 | `1905782bd879` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Add nightly restage | 2 | 34 | 26 | No |
| 2023-01-18 | `442fa417ed75` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Fix deploy params | 1 | 2 | 4 | No |
| 2023-01-18 | `554fa1c17af9` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Add deploy job and scripts to pipeline | 4 | 89 | 96 | No |
| 2023-01-18 | `289cda194d34` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove duplicate node dependency | 1 | 0 | 10 | No |
| 2023-01-18 | `248c16c9a4fb` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up testing job | 2 | 44 | 37 | No |
| 2023-01-17 | `0aa3f54ef9eb` | Andrew Burnes <andrew.burnes@gsa.gov> | Update node version and disable PR status check jobs | 3 | 14 | 14 | No |
| 2023-01-17 | `504a59928068` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: ignore PR status put on tests to get to testing phase | 1 | 7 | 7 | No |
| 2023-01-17 | `bdab03c9cd8a` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Add initial docs about ci update | 1 | 3 | 1 | No |
| 2023-01-17 | `1fc9ddf41309` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: cleanup set pipeline of PR | 1 | 1 | 2 | No |
| 2023-01-17 | `c0c7c226aac8` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Fix params for GH PR depth | 1 | 1 | 1 | No |
| 2023-01-17 | `cc6f62202aba` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Initial commit to begin testing in Concourse | 2 | 451 | 0 | No |
| 2023-01-11 | `03c335efabfd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #204 from cloud-gov/chore-update-gh-repo-settings-203 | 9 | 101 | 26 | No |
| 2023-01-11 | `c8f3916d256d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update GH repo settings to close #203 | 9 | 101 | 26 | No |
| 2022-12-21 | `07ed116db206` | Ryan Wold <ryan.wold@gsa.gov> | specify app, route, and redirect | 3 | 10 | 0 | No |
| 2022-12-05 | `1fabcb341200` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #200 from 18F/aduth-redirect-login-partners | 5 | 32 | 1 | No |
| 2022-09-30 | `0524489e97c8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #199 from 18F/feat-add-fac-gov-redirect | 7 | 753 | 1514 | No |
| 2022-09-30 | `d45c3a112959` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update circleci docker-compose version | 1 | 3 | 1 | Yes |
| 2022-09-30 | `cb7621254aaf` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update circleci node version | 1 | 1 | 1 | No |
| 2022-09-30 | `03507982fb9d` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update yarn.lock | 2 | 735 | 1509 | No |
| 2022-09-30 | `e1c0c5a817d2` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add fac.gov redirect to www.fac.gov | 5 | 14 | 3 | No |
| 2022-08-17 | `b07713cf9bfd` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #198 from 18F/add-portfolios-18f-gov | 3 | 10 | 0 | No |
| 2022-08-03 | `01bf1baeafda` | Andrew Burnes <andrew.burnes@gsa.gov> | Add include subdomains preload to www.search.gov | 1 | 2 | 1 | No |
| 2021-01-29 | `1d5147ebebc4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #176 from 18F/apb/redirect-govconnect | 3 | 11 | 1 | No |
| 2021-01-27 | `a6d108be5fa6` | Andrew Burnes <andrew.burnes@gsa.gov> | Update config to redirect govconnect.18f.gov to github repo | 3 | 11 | 1 | No |

Notes:
* Inspect any commit with `git -C pages-redirects show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-mailer`

* Path: `/Users/brianjhurst/Code/pages-mailer`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin/2021-11-22-security-considerations-action, origin, origin/apb/test-pr, origin/dependabot/npm_and_yarn/npm_and_yarn-371a9f96ec, origin/main, origin/pages-mailer_add_security_md_20240408110157
* Remotes: `origin	https://github.com/cloud-gov/pages-mailer.git (fetch)`; `origin	https://github.com/cloud-gov/pages-mailer.git (push)`
* Matching commit count: 34
* Suspicious commit count: 0
* Timeline: 2021-11-22 to 2026-03-17
* Total files changed across matching commits: 63
* Total insertions/deletions: 22736 / 28283
* Top changed file paths: `package-lock.json` (16), `package.json` (14), `ci/pipeline.yml` (14), `.github/workflows/security-considerations.yml` (4), `test/server.test.js` (4), `README.md` (3), `CODEOWNERS` (2), `.gitignore` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `a51ba97b2485` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #64 from cloud-gov/chore-update-fastify-version-5.8.2 | 3 | 734 | 568 | No |
| 2026-03-17 | `9544501a6aba` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update fastify v5.8.2 | 3 | 734 | 568 | No |
| 2026-03-17 | `4cda82f0a9c3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #63 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-mailer | 1 | 0 | 11 | No |
| 2026-03-09 | `b325c17519f9` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #61 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-mailer | 1 | 0 | 15 | No |
| 2025-12-10 | `e274158c053e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #58 from cloud-gov/fix-ci-pipeline-node-version-resource | 1 | 4 | 4 | No |
| 2025-12-10 | `a2802f2769ef` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: CI pipeline Node version resource | 1 | 4 | 4 | No |
| 2025-12-10 | `65cee6c4c845` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #57 from cloud-gov/chore-update-deps-20251210 | 2 | 3198 | 2780 | No |
| 2025-12-10 | `ad14a2684449` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update node dependencies 2025-12-10 | 2 | 3198 | 2780 | No |
| 2025-10-15 | `98f2e23572e2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #55 from cloud-gov/chore-update-node-v22-with-nodemailer-v7 | 3 | 39 | 41 | No |
| 2025-10-15 | `350da4b3e843` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update to Node v22 and Nodemailer v7 | 3 | 39 | 41 | No |
| 2025-10-02 | `d381b37991e8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #53 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `60eb04113bed` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-09-17 | `a349b67953f1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #52 from cloud-gov/chore-quarterly-deps-update-q4fy25 | 2 | 1966 | 1487 | No |
| 2025-09-17 | `a1c8bbfc47e3` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Run dependency update for Q4 FY25 | 2 | 1966 | 1487 | No |
| 2025-07-07 | `9baba1947102` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #51 from cloud-gov/chore-set-security-considerations-read-only | 1 | 3 | 0 | No |
| 2025-07-07 | `049d73003147` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 3 | 0 | No |
| 2025-05-23 | `e41af1f833a4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #49 from cloud-gov/update-contrib-20250522221334 | 1 | 14 | 10 | No |
| 2024-07-05 | `482cef4ab48b` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #46 from cloud-gov/chore-update-deps-and-pipeline-topology | 2 | 434 | 369 | No |
| 2024-07-05 | `1f1ba07b42b1` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update node deps and pipeline topology | 2 | 434 | 369 | No |
| 2024-03-12 | `ea42a819bc97` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #37 from cloud-gov/chore-ci-update-general-task-registry-image | 1 | 11 | 2 | No |
| 2024-03-12 | `89c4a9e8d069` | Andrew Burnes <andrew.burnes@gsa.gov> | chore(ci): Switch to general-task and registry-image for CI jobs | 1 | 11 | 2 | No |
| 2024-01-18 | `e65ac2b3f646` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #31 from cloud-gov/chore-update-tap-dependency-2024-01-18 | 4 | 4046 | 8162 | No |
| 2024-01-18 | `736859c4509c` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Switch testing to vitest from tap | 4 | 4046 | 8162 | No |
| 2023-07-27 | `e94223c3f444` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #29 from cloud-gov/chore-update-deps-for-node-18 | 3 | 900 | 700 | No |
| 2023-07-27 | `80b27b5f94af` | Andrew Burnes <apburnes@gmail.com> | chore: Update update deps for node v18 | 3 | 900 | 700 | No |
| 2023-04-18 | `71854ad71ab3` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #24 from cloud-gov/ci-verify-commit-gpg-key | 1 | 1 | 0 | No |
| 2023-04-17 | `4d0189c408c3` | Andrew Burnes <andrew.burnes@gsa.gov> | ci: Verify git commits with gpg keys | 1 | 1 | 0 | No |
| 2022-08-23 | `c4f1445438d1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #20 from cloud-gov/apb/update-set-pipeline | 1 | 2 | 0 | No |
| 2022-08-22 | `18a1fea340fe` | Andrew Burnes <andrew.burnes@gsa.gov> | Successfully set pipeline before running deploy and nightly tasks | 1 | 2 | 0 | No |
| 2022-08-22 | `42cff52480d2` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #19 from cloud-gov/apb/update-node-version | 3 | 10 | 10 | No |
| 2022-08-22 | `7aeaeeb3781e` | Andrew Burnes <andrew.burnes@gsa.gov> | Update node version to pull lts of node 16 | 3 | 10 | 10 | No |
| 2021-11-22 | `705adb3ffa47` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #8 from cloud-gov/2021-11-22-security-considerations-action | 2 | 12 | 0 | No |
| 2021-11-22 | `22a61da90f19` | Andrew Burnes <andrew.burnes@gsa.gov> | Creating a test PR | 1 | 1 | 1 | No |
| 2021-11-22 | `7d73f2d4cf77` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #6 from cloud-gov/2021-11-22-security-considerations-action | 1 | 11 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-mailer show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-example-staff-dir`

* Path: `/Users/brianjhurst/Code/pages-example-staff-dir`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-codeowners, origin/chore-sec, origin/dependabot/npm_and_yarn/npm_and_yarn-2b901f0e0d, origin/main, origin/make-list-alphabetical
* Remotes: `origin	https://github.com/cloud-gov/pages-example-staff-dir.git (fetch)`; `origin	https://github.com/cloud-gov/pages-example-staff-dir.git (push)`
* Matching commit count: 2
* Suspicious commit count: 0
* Timeline: 2025-10-02 to 2025-10-02
* Total files changed across matching commits: 2
* Total insertions/deletions: 2 / 0
* Top changed file paths: `CODEOWNERS` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2025-10-02 | `54c409e4d830` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #4 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `0b84aa356288` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-example-staff-dir show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-uswds-11ty`

* Path: `/Users/brianjhurst/Code/pages-uswds-11ty`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: bh-set-node-version, main, pages-studio, origin/11ty-template-policies-page, origin, origin/abp/update-node-deps-230822, origin/apb/add-codeql, origin/apb/initial, origin/asset-paths-fix-68, origin/bh-set-node-version, origin/caleywoods-uswds3, origin/chore-add-codeowners (+18 more)
* Remotes: `origin	git@github.com:cloud-gov/pages-uswds-11ty.git (fetch)`; `origin	git@github.com:cloud-gov/pages-uswds-11ty.git (push)`
* Matching commit count: 54
* Suspicious commit count: 2
* Timeline: 2022-03-18 to 2026-05-20
* Total files changed across matching commits: 279
* Total insertions/deletions: 89276 / 42897
* Top changed file paths: `package-lock.json` (23), `package.json` (19), `_data/assetPaths.json` (8), `.eleventy.js` (8), `_includes/menu.html` (8), `README.md` (7), `config/buildAssets.js` (7), `styles/styles.scss` (7)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-05-20 | `96294a4ab790` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #107 from cloud-gov/chore-update-node-version-and-tighten-npmrc | 3 | 54 | 50 | Yes |
| 2026-05-20 | `89a6e8c5bfba` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update to Node v24 and add npmrc rules | 3 | 54 | 50 | Yes |
| 2025-10-02 | `3fa8235b202f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #97 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `33d519f16471` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2024-09-18 | `545a86341cb5` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #62 from cloud-gov/chore-upate-deps-and-switch-to-decap-cms | 5 | 12451 | 11167 | No |
| 2024-09-17 | `f0d21f3a1976` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Update deps and switch to decap-cms | 5 | 12451 | 11167 | No |
| 2024-08-30 | `96ec5ad31d71` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #59 from cloud-gov/upgrade-11ty-v2 | 5 | 715 | 2398 | No |
| 2024-08-29 | `a05441306cda` | Heather Battaglia <heatherjaybillings@gmail.com> | feat: Upgrade 11ty to v2 | 5 | 715 | 2398 | No |
| 2023-01-31 | `820bf58b8d3e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #16 from cloud-gov/dependabot/npm_and_yarn/loader-utils-1.4.2 | 1 | 6 | 6 | No |
| 2023-01-19 | `40459dd4912e` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #22 from cloud-gov/dependabot/npm_and_yarn/json5-1.0.2 | 1 | 12 | 12 | No |
| 2023-01-19 | `7c37fc053eea` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge branch 'main' into dependabot/npm_and_yarn/json5-1.0.2 | 2 | 1107 | 2742 | No |
| 2023-01-17 | `c6ad8caa9c9f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #27 from cloud-gov/dependabot/npm_and_yarn/simple-git-3.16.0 | 1 | 6 | 6 | No |
| 2023-01-17 | `a2debd8dfe60` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #15 from cloud-gov/dependabot/npm_and_yarn/nth-check-and-eleventy-plugin-svg-sprite-2.1.1 | 2 | 653 | 2292 | No |
| 2023-01-17 | `936314ef63a1` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #26 from cloud-gov/chore-lmm/bump-11ty-issue-24 | 2 | 510 | 506 | No |
| 2023-01-17 | `ff3403e9344f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #25 from loganmeetsworld/lmm/bump-11ty | 2 | 510 | 506 | No |
| 2022-09-30 | `de80cd6bf7b4` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #12 from cloud-gov/fix-uswds-readme-version | 1 | 1 | 1 | No |
| 2022-09-30 | `c941a48a3996` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #11 from cloud-gov/rebase-caleywoods-uswds3 | 22 | 87 | 2087 | No |
| 2022-09-30 | `19bedaa5f8b9` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: README to have USWDS v3 | 1 | 1 | 1 | No |
| 2022-09-29 | `092a8f722324` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #8 from caleywoods/uswds3 | 22 | 87 | 2087 | No |
| 2022-09-08 | `adfecaf4a209` | Caley Woods <caley.woods@gsa.gov> | Remove commented CSS for old USWDS 2 override | 1 | 0 | 1 | No |
| 2022-09-08 | `d98448bd61e2` | Caley Woods <caley.woods@gsa.gov> | asset paths have changed | 1 | 7 | 6 | No |
| 2022-09-08 | `6f3ded9c71ae` | Caley Woods <caley.woods@gsa.gov> | Add theme image path to stylesheet | 1 | 4 | 13 | No |
| 2022-09-08 | `3a40495d5ebb` | Caley Woods <caley.woods@gsa.gov> | Pass sass loadpaths for USWDS 3 | 1 | 7 | 6 | No |
| 2022-09-08 | `ffd94f5ca534` | Caley Woods <caley.woods@gsa.gov> | Fix image paths | 3 | 6 | 6 | No |
| 2022-09-08 | `e8b307a68dac` | Caley Woods <caley.woods@gsa.gov> | Update stylesheet to USWDS 3 style | 1 | 9 | 70 | No |
| 2022-09-08 | `c30393f09829` | Caley Woods <caley.woods@gsa.gov> | Remove leftover USWDS 2 files | 10 | 0 | 1945 | No |
| 2022-09-08 | `63d6fc6ffe6b` | Caley Woods <caley.woods@gsa.gov> | Require new USWDS path | 1 | 1 | 1 | No |
| 2022-09-08 | `f576ef188f72` | Caley Woods <caley.woods@gsa.gov> | Update asset build script for USWDS3 | 1 | 7 | 1 | No |
| 2022-09-08 | `60dde40ce5cf` | Caley Woods <caley.woods@gsa.gov> | Update image path for search.gov form | 1 | 1 | 1 | No |
| 2022-09-08 | `0c5c6d9b8e0f` | Caley Woods <caley.woods@gsa.gov> | Load USWDS JS | 1 | 1 | 0 | No |
| 2022-09-08 | `f779c04f2ae7` | Caley Woods <caley.woods@gsa.gov> | Update path to close svg in menu | 1 | 1 | 1 | No |
| 2022-09-08 | `0399768f23be` | Caley Woods <caley.woods@gsa.gov> | Update path to banner icons in header | 1 | 3 | 3 | No |
| 2022-09-08 | `e08095872ab3` | Caley Woods <caley.woods@gsa.gov> | Update path to USWDS svg icons | 1 | 4 | 2 | No |
| 2022-09-08 | `cf7984908a47` | Caley Woods <caley.woods@gsa.gov> | Passthrough copy uswds-init.js to prevent banner flashing | 1 | 3 | 0 | No |
| 2022-09-08 | `6d1ef51800a9` | Caley Woods <caley.woods@gsa.gov> | Add USWDS3 and remove USWDS 2 | 2 | 45 | 43 | No |
| 2022-08-23 | `5a943d9d526d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #6 from cloud-gov/abp/update-node-deps-230822 | 2 | 1522 | 1090 | No |
| 2022-08-23 | `a29e7a7f90bf` | Andrew Burnes <andrew.burnes@gsa.gov> | Update deps | 2 | 1522 | 1090 | No |
| 2022-06-06 | `ef5bf1d9329f` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3 from cloud-gov/apb/add-codeql | 1 | 51 | 0 | No |
| 2022-06-02 | `acf80641a463` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2 from cloud-gov/dependabot/npm_and_yarn/ejs-3.1.7 | 1 | 195 | 59 | No |
| 2022-06-02 | `e19c69b8175c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #4 from cloud-gov/dependabot/npm_and_yarn/sharp-0.30.6 | 1 | 64 | 64 | No |
| 2022-05-03 | `b78d0ba9cc0d` | Andrew Burnes <andrew.burnes@gsa.gov> | Create codeql gh workflow | 1 | 51 | 0 | No |
| 2022-05-03 | `2d5af6116f70` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #1 from cloud-gov/apb/initial | 62 | 27511 | 0 | No |
| 2022-04-29 | `76e2c441a266` | Andrew Burnes <andrew.burnes@gsa.gov> | Add sprite docs and add side article in blog template. | 2 | 18 | 10 | No |
| 2022-04-15 | `c32d249d4464` | Andrew Burnes <andrew.burnes@gsa.gov> | Remove red color for p tags in CMS | 1 | 0 | 3 | No |
| 2022-04-15 | `c788c70c41cc` | Andrew Burnes <andrew.burnes@gsa.gov> | fix admin config string | 1 | 1 | 1 | No |
| 2022-04-15 | `ee882b2445a6` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix admin config path for prefixPath | 1 | 1 | 1 | No |
| 2022-04-15 | `92c4716d4509` | Andrew Burnes <andrew.burnes@gsa.gov> | Fix blog post config for Netlify CMS | 3 | 56 | 4 | No |
| 2022-04-15 | `a335d18271ad` | Andrew Burnes <andrew.burnes@gsa.gov> | Add pathPrefix for image shortcodes | 1 | 7 | 1 | No |
| 2022-04-15 | `836f3dfba9ba` | Andrew Burnes <andrew.burnes@gsa.gov> | Update pathPrefix with BASEURL env | 10 | 42 | 23 | No |
| 2022-04-15 | `73f36a2f9a46` | Andrew Burnes <andrew.burnes@gsa.gov> | Add federalist build script | 1 | 4 | 3 | No |
| 2022-04-07 | `1cd1bfe683c8` | Andrew Burnes <andrew.burnes@gsa.gov> | Update collection pagination and collection items | 12 | 3289 | 969 | No |
| 2022-03-18 | `346953b68f6b` | Andrew Burnes <andrew.burnes@gsa.gov> | Clean up image shortcodes | 1 | 9 | 4 | No |
| 2022-03-18 | `b6b160ab5d72` | Andrew Burnes <andrew.burnes@gsa.gov> | WIP | 58 | 25103 | 0 | No |
| 2022-03-18 | `57d92fbe6fed` | Andrew Burnes <andrew.burnes@gsa.gov> | Initial Commit | 5 | 309 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-uswds-11ty show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `dsd`

* Path: `/Users/brianjhurst/Code/dsd`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/dependabot/github_actions/github-actions-6a98abd9ac, origin/dependabot/pip/python-19f1f3e67a, origin/main
* Remotes: `origin	https://github.com/cloud-gov/dsd.git (fetch)`; `origin	https://github.com/cloud-gov/dsd.git (push)`
* Matching commit count: 0
* Suspicious commit count: 0
* Timeline: none to none
* Total files changed across matching commits: 0
* Total insertions/deletions: 0 / 0
* Top changed file paths: None

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| - | - | - | No matching commits | 0 | 0 | 0 | No |

Notes:
* No matching author or committer entries were found on local reachable refs.

### `pages-images`

* Path: `/Users/brianjhurst/Code/pages-images`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/chore-add-deps-to-python-3.11, origin/feat-add-python3, origin/feat-create-dockerfile, origin/main, origin/pages-images_add_security_md_20240408110358
* Remotes: `origin	https://github.com/cloud-gov/pages-images.git (fetch)`; `origin	https://github.com/cloud-gov/pages-images.git (push)`
* Matching commit count: 20
* Suspicious commit count: 4
* Timeline: 2023-12-20 to 2026-03-17
* Total files changed across matching commits: 52
* Total insertions/deletions: 2635 / 31
* Top changed file paths: `README.md` (8), `dind/v25/Dockerfile` (6), `node/v20/Dockerfile` (4), `node/v22/Dockerfile` (4), `python/v3.11/Dockerfile` (4), `.github/workflows/security-considerations.yml` (3), `.github/workflows/security-considerations.properties.json` (2), `node/v24/docker-entrypoint.sh` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `95071c53388d` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #40 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-images | 1 | 0 | 8 | No |
| 2026-01-12 | `aec7327387f8` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #35 from cloud-gov/feat-add-node-v24 | 4 | 140 | 3 | No |
| 2026-01-12 | `45546ef83371` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add nodejs v24 and update to latest for node v20 and v22 | 4 | 140 | 3 | Yes |
| 2025-10-09 | `490b59f99ea0` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #30 from cloud-gov/feat-add-node-v22 | 2 | 137 | 0 | No |
| 2025-10-08 | `9bc49ef3aba8` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Nodejs v22 | 2 | 137 | 0 | Yes |
| 2025-10-02 | `ee85c884e807` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #29 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `67ac17667106` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |
| 2025-07-07 | `f1b08288d703` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #27 from cloud-gov/chore-set-security-considerations-read-only | 1 | 4 | 1 | No |
| 2025-07-07 | `ba88d4feaaed` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Set security considerations action to read only | 1 | 4 | 1 | No |
| 2024-07-31 | `eff9dfa322c8` | Andrew Burnes <andrew.burnes@gsa.gov> | fix: Zap image to pass USG audit | 1 | 0 | 2 | No |
| 2024-02-13 | `b42ae63bc03c` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #3 from cloud-gov/chore-add-deps-to-python-3.11 | 2 | 3 | 0 | No |
| 2024-02-13 | `8d0978ac47b2` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add libpq and curl to python v3.11 image | 2 | 3 | 0 | No |
| 2024-02-08 | `892bdc22a069` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #2 from cloud-gov/feat-add-python3 | 3 | 82 | 2 | No |
| 2024-02-07 | `0a8a1d11e5c8` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Add Python base image | 3 | 82 | 2 | Yes |
| 2024-02-06 | `6dca5e576f41` | Andrew Burnes <andrew.burnes@gsa.gov> | Merge pull request #1 from cloud-gov/feat-create-dockerfile | 7 | 905 | 4 | No |
| 2024-02-06 | `35f302c5cb10` | Andrew Burnes <andrew.burnes@gsa.gov> | Add CI workflow to README | 1 | 4 | 0 | No |
| 2024-02-06 | `a7d802f3b2d5` | Andrew Burnes <andrew.burnes@gsa.gov> | Fill out docs on local build | 1 | 23 | 0 | No |
| 2024-02-06 | `c0cee71560b0` | Andrew Burnes <andrew.burnes@gsa.gov> | Update README.md | 1 | 1 | 1 | No |
| 2024-01-30 | `cb2b81af472c` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: Create images for dind and node | 7 | 878 | 4 | Yes |
| 2023-12-20 | `da8929ded9a0` | Andrew Burnes <andrew.burnes@gsa.gov> | feat: init commit | 7 | 90 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-images show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-research-spider`

* Path: `/Users/brianjhurst/Code/pages-research-spider`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/cleanup/security-considerations/cloud-gov-pages-research-spider, origin/dependabot/pip/pip-1fc43f3722, origin/main, origin/prototype
* Remotes: `origin	https://github.com/cloud-gov/pages-research-spider.git (fetch)`; `origin	https://github.com/cloud-gov/pages-research-spider.git (push)`
* Matching commit count: 1
* Suspicious commit count: 0
* Timeline: 2026-03-17 to 2026-03-17
* Total files changed across matching commits: 1
* Total insertions/deletions: 0 / 8
* Top changed file paths: `.github/workflows/security-considerations.properties.json` (1)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2026-03-17 | `54f0db0ab995` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #7 from cloud-gov/cleanup/security-considerations/cloud-gov-pages-research-spider | 1 | 0 | 8 | No |

Notes:
* Inspect any commit with `git -C pages-research-spider show <sha>`. Matching commits were deduplicated by SHA within this repository.

### `pages-404-page`

* Path: `/Users/brianjhurst/Code/pages-404-page`
* Current branch: `main`
* Readable: yes
* Available branches/remotes: main, origin, origin/css-improvements, origin/main, origin/wcag-improvements
* Remotes: `origin	https://github.com/cloud-gov/pages-404-page.git (fetch)`; `origin	https://github.com/cloud-gov/pages-404-page.git (push)`
* Matching commit count: 2
* Suspicious commit count: 0
* Timeline: 2025-10-02 to 2025-10-02
* Total files changed across matching commits: 2
* Total insertions/deletions: 2 / 0
* Top changed file paths: `CODEOWNERS` (2)

| Date | Commit | Author | Subject | Files Changed | Insertions | Deletions | Suspicious? |
|---:|---|---|---|---:|---:|---:|---|
| 2025-10-02 | `60be96f263fe` | Andrew Burnes <apburnes@gmail.com> | Merge pull request #8 from cloud-gov/chore-add-codeowners | 1 | 1 | 0 | No |
| 2025-10-02 | `177b3501a0db` | Andrew Burnes <andrew.burnes@gsa.gov> | chore: Add CODEOWNERS | 1 | 1 | 0 | No |

Notes:
* Inspect any commit with `git -C pages-404-page show <sha>`. Matching commits were deduplicated by SHA within this repository.

## Errors and Skipped Repositories

No repositories were skipped. All listed repositories were readable Git work trees.

## Validation and Method

The report was generated successfully at `./author-commit-audit-report.md`.

Commands and script approach used:

* Parsed `./REPOS.md` as the only repository source of truth.
* Validated each path with `git -C <repo> rev-parse --is-inside-work-tree`.
* Collected refs with `git -C <repo> for-each-ref --format=%(refname:short) refs/heads refs/remotes`.
* Collected commit metadata across all refs with `git -C <repo> log --all --date=iso-strict --format=<sha,parents,author,committer,dates,subject,body>`.
* Filtered author and committer fields with regex `Andrew Burnes\|andrew\.burnes\|apburnes` and deduplicated commits by SHA per repository.
* Collected per-commit stats with `git -C <repo> show --find-renames --numstat --format= <sha>`.
* Collected containing refs where practical with `git -C <repo> branch -a --contains <sha>`.
* Inspected diffs with `git -C <repo> show --find-renames --stat --patch --no-ext-diff --no-color --format=fuller <sha>`.

Limitations:

* The scan used local reachable refs only. It did not fetch from remotes, inspect deleted branches, or inspect GitHub pull request refs that are not present locally.
* Binary diffs and generated lockfile changes were summarized by Git stats; binary contents were not decoded or executed.
* Suspicious finding classification is pattern-based and intentionally cautious. It identifies review candidates, not confirmed malicious intent.
* Branch/ref containment was collected with local refs and capped in the underlying data where there were many containing refs.
* No repository code, build scripts, dependency installation, branch switching, pushes, or project commands were run.

