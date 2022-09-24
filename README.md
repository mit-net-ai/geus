# redesigned-octo-guapo
github.com:
    user: M4Kjxcxv
    oauth_token: xxx
    user: mit-net-ai
    oauth_token: xxx
    git_protocol: ssh
    [includeIf "gitdir:~/work/"]
  path = ~/work/.gitconfig
  github.com/google:
  - user: gemployee
    oauth_token: ...

github.com/microsoft:
  - user: msemployee
    oauth_token: ...

github.com:
  - user: personal
    oauth_token: ...
    alias gh_cli=$(which gh)
function gh() {
  if [[ $(pwd) =~ {PATH_TO_PERSONAL_CODE} ]]; then
    GITHUB_TOKEN=$PERSONAL_GH_CLI_TOKEN
  else
    GITHUB_TOKEN=$WORK_GH_CLI_TOKEN
  fi

  GITHUB_TOKEN=$GITHUB_TOKEN gh_cli $@
  unset GITHUB_TOKEN
}
alias gh_cli=$(which gh)
function gh() {
  if [[ $(pwd) =~ {PATH_TO_PERSONAL_CODE} ]]; then
    GITHUB_TOKEN=$PERSONAL_GH_CLI_TOKEN
  else
    GITHUB_TOKEN=$WORK_GH_CLI_TOKEN
  fi

  GITHUB_TOKEN=$GITHUB_TOKEN gh_cli $@
  unset GITHUB_TOKEN
}
[includeIf "gitdir:~/dev/"]
  path = ~/.gitconfig.personal
[includeIf "gitdir:~/workspace/"]
  path = ~/.gitconfig.work
  [M4Kjxcvx][mit-net-ai]
  name = JessieWagg-[pandorumliquidity]-[mit-net-ai]
  email = [pandorumliquiditygenerate@outlook.com][intel.payportal@gmail.com]
