# JUnit Reporter for Mocha 

This is fork of https://github.com/michaelleeallen/mocha-junit-reporter for those who want to use `jenkinsClassnamePrefix` option.

## Installation

```shell
$ npm install @prnsml/mocha-junit-reporter@2.1.1 --save-dev
```

or as a global module
```shell
$ npm install -g @prnsml/mocha-junit-reporter@2.1.1
```
### Full configuration options

| Parameter                      | Default                | Effect                                                                                                                  |
| ------------------------------ | ---------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| mochaFile                      | `test-results.xml`     | configures the file to write reports to                                                                                 |
| includePending                 | `false`                | if set to a truthy value pending tests will be included in the report                                                   |
| properties                     | `null`                 | a hash of additional properties to add to each test suite                                                               |
| toConsole                      | `false`                | if set to a truthy value the produced XML will be logged to the console                                                 |
| useFullSuiteTitle              | `false`                | if set to a truthy value nested suites' titles will show the suite lineage                                              |
| suiteTitleSeparatedBy          | ` ` (space)            | the character to use to separate nested suite titles. (defaults to ' ', '.' if in jenkins mode)                         |
| testCaseSwitchClassnameAndName | `false`                | set to a truthy value to switch name and classname values                                                               |
| rootSuiteTitle                 | `Root Suite`           | the name for the root suite. (defaults to 'Root Suite')                                                                 |
| testsuitesTitle                | `Mocha Tests`          | the name for the `testsuites` tag (defaults to 'Mocha Tests')                                                           |
| outputs                        | `false`                | if set to truthy value will include console output and console error output                                             |
| attachments                    | `false`                | if set to truthy value will attach files to report in `JUnit Attachments Plugin` format (after console outputs, if any) |
| antMode                        | `false`                | set to truthy value to return xml compatible with [Ant JUnit schema][ant-schema]                                        |
| antHostname                    | `process.env.HOSTNAME` | hostname to use when running in `antMode`  will default to environment `HOSTNAME`                                       |
| jenkinsMode                    | `false`                | if set to truthy value will return xml that will display nice results in Jenkins                                        |
| jenkinsClassnamePrefix         | `undefined`            | adds a prefix to a classname when running  in `jenkinsMode`                                                             |
