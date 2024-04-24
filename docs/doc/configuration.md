# Configuration

## About

The <term:test run> can be configured using multiple configuration files.

The configuration files are yaml based and located in the `etc/settings` directory of your
<term:test project>.

The default configuration file `etc/settings/default.yml` is automatically loaded on each
<term:test run>.

Further configuration files can be loaded using the `--config` argument of the <cmd:run|acre run>
command.

## Sections


### playwright

The playwright configuration allows you to configure different playwright-related
settings for the test run.

#### playwright.browser

config:playwright.browser.headless
:   If set to `true`, the test run will be executed using a headless browser. The
    browser will not be visible during the <term:test run>.

    !!! Example

        ``` yaml
        playwright:
            browser:
                headless: true
        ```

config:playwright.browser.auto
:   Defines when to automatically open and close the browser
    in a test run.

    Available values are:

    | Value | Behaviour |
    | -- | -- |
    | `testrun` | Browser is automatically opened before starting the test run and closed after the test run is finished|
    | `feature` | Browser is automatically opened before each feature and closed after each feature |
    | `scenario` | Browser is automatically opened before each scenario and closed after each scenario |
    | **`off`**  | (default) Browser is neither automatically opened or closed. |

    !!! Example

        ``` yaml
        playwright:
            browser:
                headless: true
                auto: feature
        ```

### testrun

This section contains test run related settings.

config:testrun.delays.step
:   Defines a delay in seconds which acre will wait
    after the execution of each step. Default is 0.

    !!! Example

        ``` yaml
        testun:
            delays:
                steps: 0.5
        ```

### logging

This section contains settings related to the acre logging.

config:logging.level
:   Defines the logging level threshold for the logging messages.
    Default is <loglevel:NOTE>

    !!! Example

        ``` yaml
        logging:
            level: DEBUG
        ```
