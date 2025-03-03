# create_action_step

動的に`GitHub App`の`Step`を作成する`Composite Action`

## uses

```yaml
- name: Composite action local
  uses: ./.github/actions
  with:
    working-dir: fixtures/usecase1 # ベースとなるaction.yml
    step_name: "Step hoge" # 実行するStep名
    uses_action: ./fixtures/common # 実行したいComposite Action
```

## Develop

```shell
act workflow_dispatch -W ./.github/workflows/test_composite.yml
```