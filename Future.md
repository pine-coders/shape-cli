# Main app

* Ability to parse command line arguments.
* Ability to pull down template repo if found.
* Parse `shape-project.json` from the project repo to decide what featured and scaffoldings are available.
    - Template name, template version
    - Development machine (vagrant, docker...) + features
        - Project will have dependent features info:
            - Yii2 requires PHP >=5.4 - development machine needs to have PHP + mbstring extension 
    - Deploy machine (deploy scripts generator templates, docker composer generator, etc...)
        - Deploy machine requirements checker.
    - Project modifiers:
        - Add frontend (angular, vue, react...) - removes frontend folder from current project and sets up this (destructive action)
    - Project features:
        - Add typescript compiler
        - Add webpack
        - Add gulp
        - ...etc
    - Template specific scaffolding generators:
        - Generate app folder
        - Generate module folder
        - ... etc
* Use `shape-project.lock` as a lockfile which holds current added features to the project + info.