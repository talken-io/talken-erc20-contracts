# CLAUDE.md — Talken ERC20 Contracts
> 📖 팀 가이드: [colligence-claude-guide](https://github.com/talken-io/colligence-claude-guide)

> 상위 가이드 상속 (talken-io/CLAUDE.md). 여기서는 반복하지 않음.

## Overview

원본 TALK ERC20. **레거시 참조 전용.** 신규 스왑/브릿지는 `talken-contracts`, 멀티체인 토큰은 `talken-oft-contracts`. | 상태: Maintenance

## Do not apply modern contract rules

- Truffle 5 + OpenZeppelin **2.5** (Solidity 0.8 / Hardhat / OZ 5 아님)
- workspace `.claude/rules/contracts.md` 경로에서 제외됨
- 이 트리에 Hardhat 배포/업그레이드 패턴을 이식하지 않는다

## Architecture

```text
source/
├── contracts/Talken.sol
├── contracts/erc20/          # ERC20* 확장
├── contracts/library/        # Ownable, Pausable, Freezable, SafeMath
├── test/                     # JS Truffle tests
└── truffle-config.js
audit_report/                 # 감사 PDF
```

## Commands

`source/`에서 실행:

```bash
cd source
npm test                      # 또는 scripts/test.sh
```

루트 `package.json` 없음.

## Notes

- origin: `git@github.com:talken-io/talken-erc20-contracts.git`
- `talken-contracts`에 push하지 않는다. 레포가 다르다
- 감사: `audit_report/Talken_Smart_Contract_Audit_Report_TALK_v1.0.pdf`
