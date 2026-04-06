# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

React Testing Library の `act` 警告と `waitFor` の内部実装を検証するプロジェクト。技術記事の主張をテストコードで再現・検証する。

## Commands

```bash
bun test                              # 全テスト実行
bun test src/tests/act-basics.test.tsx # 単一ファイル実行
bun run typecheck                     # 型チェック
```

## Structure

- `docs/understanding-act-and-waitfor.md` — 検証対象の技術記事
- `src/tests/` — 記事の各主張に対応するテストファイル
- `src/global.d.ts` — `IS_REACT_ACT_ENVIRONMENT` 等のグローバル型定義
- `bunfig.toml` — テスト時に `src/tests/setup.ts`（happy-dom登録）をpreload
