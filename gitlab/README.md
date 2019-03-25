# GitLab-CI

## include

https://docs.gitlab.com/ee/ci/yaml/#include

```yml
include:
  - project: 'group/subgroup/project'
    ref: master
    file: .gitlab-ci-template.yml
```

다른 저장소에 있는 파일을 include 할 수 있다.
