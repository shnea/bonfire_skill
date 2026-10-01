# Bonfire Skill

**Bonfire 개발 스킬과 초기 기준 문서를 프로젝트에 구성하는 설치용 스킬입니다.**

`$bonfire`를 호출하면 대상 프로젝트의 기존 지침을 확인하고, 두 기본 스킬과 프로젝트별 기준을 구성합니다. 요구사항·기술 선택·결정 기록은 대상 프로젝트에 남아 Git으로 함께 관리됩니다.

## 설치

스킬 폴더는 [skills/bonfire](skills/bonfire/SKILL.md)입니다. Codex의 skill-installer에 다음처럼 요청할 수 있습니다.

```text
$skill-installer https://github.com/shnea/bonfire_skill 저장소의 skills/bonfire 스킬을 설치해줘.
```

다른 스킬 지원 도구에서는 `skills/bonfire` 폴더 전체를 해당 도구의 설치 방식에 맞춰 가져옵니다. 내부의 `assets`도 함께 필요합니다.

## 사용

대상 프로젝트에서 다음처럼 요청합니다.

```text
$bonfire 이 프로젝트에 Bonfire 기본 구성을 적용해줘.
```

특정 경로를 지정하거나, 이미 적용한 프로젝트의 누락 파일을 보완하도록 요청할 수도 있습니다.

스킬은 다음 구성을 배치합니다.

| 경로 | 역할 |
| --- | --- |
| AGENTS.md | 프로젝트 시작 안내 |
| .agents/skills/workflow/ | 요구사항 정리·구현·검증 절차 |
| .agents/skills/golden-path/ | 핵심 기준·14개 영역·스킬 연결·결정 이력 |

기존 AGENTS.md와 프로젝트 기록을 보존하고, 같은 이름의 다른 스킬이나 충돌하는 지침이 있으면 해당 부분을 확인합니다. 다시 호출해도 기존 기준을 초기 상태로 덮어쓰지 않도록 지시합니다.

## 프로젝트별 사용

설치한 `bonfire`는 초기 구성과 누락 파일 보완을 담당합니다. 구성 후에는 프로젝트 안의 `workflow`와 `golden-path`를 사용합니다.

프로젝트마다 별도의 기준 문서를 갖기 때문에, 한 프로젝트의 기술 선택이나 예외가 다른 프로젝트에 적용되지 않습니다. 프로젝트별 변경은 설치된 스킬의 원본에도 자동 반영되지 않습니다.

## 기반

동봉 템플릿은 [Bonfire v1](https://github.com/shnea/bonfire/tree/ef14ef1be67bd26388ee0e1a80ccd4aa0bc32ee6)을 기반으로 합니다. 원본 버전과 스킬 식별자에 대한 정보는 [SOURCE.md](skills/bonfire/assets/SOURCE.md)에 있습니다.

파일 배치와 병합은 스킬을 실행하는 에이전트가 수행합니다. 자동 인식·호출 방법은 사용하는 도구에서 확인하세요.
