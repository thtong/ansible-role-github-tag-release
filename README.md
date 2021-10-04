# thtong.github-tag-release

Ansible role to download tagged/latest release from any GitHub repository

## Requirements

None.

## Role Variables

- gh_repo_name - the github repo e.g. `thtong/ansible-role-github-tag-release`
- gh_repo_tag - the tag e.g `latest`
- gh_repo_download_dir - the path to save the release asset e.g. `/tmp/`
- gh_repo_download_mode - options are `architecture`, `first`, `all` (default), `match`
  - architecture will download assets with name that match target OS architecture e.g. amd64
  - first will download first asset listed
  - all will download all assets listed
  - match will download asset(s) that match the regex specified in `gh_repo_download_match_regex`
- gh_repo_download_match_regex - the regex to use if `gh_repo_download_mode` is set to match

## Dependencies

None.

## Example Playbook

    - hosts: localhost
      roles:
         - { role: thtong.github-tag-release, gh_repo_name: rfjakob/gocryptfs }

## License

BSD

## Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
