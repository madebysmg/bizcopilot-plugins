# BizCopilot 플러그인

한국 기업 검토·M&A 워크스페이스 [BizCopilot](https://bizcopilot.madebysmg.com)을 Claude와 ChatGPT(Codex) 앱에서 쓰기 위한 플러그인 모음입니다. 이 저장소에는 **연결 주소와 스킬(업무 순서 안내)만** 있습니다. 기업 데이터와 권한은 BizCopilot 서버가 로그인한 사용자별로 정하며, 이 저장소에는 비밀 값이 없습니다.

| 플러그인 | 스킬 | 하는 일 |
|---|---|---|
| `bizcopilot` | `company-brief` | 이름이나 사업자번호로 기업을 확정하고 개요·재무·임원·주주를 한 번에 브리핑 |
| | `company-notes` | 검토 메모 저장과 검색 (삭제는 웹앱에서만) |

## 설치

BizCopilot 계정(관리자 승인을 받은 계정)이 있어야 합니다.

### Claude (claude.ai · 데스크톱)

1. 맞춤 설정 > 플러그인 > 추가 > **마켓플레이스 추가** 에 `madebysmg/bizcopilot-plugins` 를 입력합니다.
2. `bizcopilot` 플러그인을 설치합니다.
3. 맞춤 설정 > **커넥터** 에서 BizCopilot을 `연결`하고 로그인과 승인을 합니다. 플러그인을 설치해도 로그인은 자동으로 되지 않습니다.

Claude Code 에서는 다음과 같습니다.

```sh
/plugin marketplace add madebysmg/bizcopilot-plugins
/plugin install bizcopilot@bizcopilot
```

### ChatGPT 앱 (Codex)

1. 플러그인 > 추가 > **마켓플레이스 추가** 에 이 저장소 주소를 입력합니다.
2. `bizcopilot` 플러그인을 설치하고, 처음 쓸 때 BizCopilot 로그인과 승인을 합니다.

Codex CLI 에서는 다음과 같습니다.

```sh
codex plugin marketplace add madebysmg/bizcopilot-plugins
codex plugin add bizcopilot
```

설치한 뒤 "삼성전자 브리핑 해줘"로 시험해 보세요.

## 사용 조건 (2026-10 기준, 공식 도움말 확인)

| | Claude | ChatGPT |
|---|---|---|
| BizCopilot 연결(커넥터) | 모든 플랜. 무료 플랜은 직접 추가하는 커넥터 1개까지 | 사용자 지정 MCP 앱은 Business·Enterprise·Edu 플랜의 웹(모바일 제외)에서 관리자가 켠 경우 |
| 플러그인 설치, 저장소로 마켓플레이스 추가 | 유료 플랜(Pro·Max·Team·Enterprise). 다른 사람에게 공유·게시는 Team·Enterprise | 플러그인 화면이 있는 앱. 플랜별 지원은 OpenAI 도움말을 확인하세요 |
| 스킬 | 모든 플랜 (설정에서 코드 실행 켜기) | 플러그인에 포함 |

Claude 무료 플랜이라면 플러그인 없이 커넥터 주소(`https://bizcopilot-mcp.madebysmg.com/mcp`)만 추가해도 BizCopilot 도구를 쓸 수 있습니다. 플랜 조건은 바뀔 수 있으니 공식 도움말을 확인하세요: [Claude 커넥터](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Claude 플러그인](https://support.claude.com/en/articles/13837440-use-plugins-in-claude), [ChatGPT 개발자 모드와 MCP 앱](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt-beta).

## 이미 BizCopilot 커넥터를 따로 추가했다면

같은 서버가 두 번 보일 수 있으니 하나만 남기세요.

## 이 저장소를 고치지 마세요

이 저장소는 BizCopilot 개발 저장소에서 만들어 올립니다. 스킬을 고치려면 개발 저장소의 `plugins/` 를 고치고 다시 내보냅니다.
