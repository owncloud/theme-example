# Theme Example

<!-- OSPO-managed README | Generated: 2026-04-16 | v2 -->

[![License](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)](LICENSE) [![ownCloud OSPO](https://img.shields.io/badge/OSPO-ownCloud-blue)](https://kiteworks.com/opensource)

Theme Example is a reference implementation for creating custom themes for ownCloud Server. It demonstrates how to override the default branding -- including logos, colors, login page background, copyright text and other visual elements -- by providing a complete, working theme app that administrators can clone, customize and deploy on their ownCloud instances.

> **Note:** This repository is in maintenance/legacy mode and is no longer actively developed.

## Part of Infrastructure / Tooling

This repository is part of the [ownCloud Server (OC10)](https://github.com/owncloud/core) theming infrastructure. It provides a starting point for administrators and integrators who need to customize the look and feel of their ownCloud deployment.

> **Legacy notice:** This repository is archived/legacy. For ownCloud Infinite Scale (oCIS), theming is handled differently through the web frontend configuration.

## Getting Started

1. Clone or [download](https://github.com/owncloud/theme-example/archive/refs/heads/master.zip) this repository to `owncloud/apps/`:

```bash
cd apps
git clone https://github.com/owncloud/theme-example.git
```

2. Set proper permissions:

```bash
chown -R www-data:www-data theme-example
```

3. If you rename the app folder, update the `<id>` in `appinfo/info.xml` to match.

### Customization

- **Images:** Open original images from `core/img` in an image editor, make changes, and overwrite the originals in the theme's directory.
- **Texts:** Edit `defaults.php` to change copyright text, slogans and other display strings.
- **CSS:** Modify `core/css/styles.css` for visual customizations. Use browser developer tools (F12) to discover CSS classes.

### Integrity Check

Since theme files must be editable, the app is unsigned. Add to `config/config.php`:

```php
'integrity.ignore.missing.app.signature' => [
    'theme-example',
],
```

## Documentation

- [ownCloud Server Theming Documentation](https://doc.owncloud.com/server/latest/developer_manual/core/theming.html)
- [ownCloud Server Admin Manual](https://doc.owncloud.com/server/latest/admin_manual/)

## Community & Support

**[Star](https://github.com/owncloud/theme-example)** this repo and **Watch** for release notifications!

- [ownCloud Website](https://owncloud.com)
- [Community Discussions](https://github.com/orgs/owncloud/discussions)
- [Matrix Chat](https://app.element.io/#/room/#owncloud:matrix.org)
- [Documentation](https://doc.owncloud.com)
- [Enterprise Support](https://owncloud.com/contact-us/)
- [OSPO Home](https://kiteworks.com/opensource)

## Contributing

We welcome contributions! Please read the [Contributing Guidelines](CONTRIBUTING.md)
and our [Code of Conduct](CODE_OF_CONDUCT.md) before getting started.

### Workflow

- **Rebase Early, Rebase Often!** We use a rebase workflow. Always rebase on the target branch before submitting a PR.
- **Dependabot**: Automated dependency updates are managed via Dependabot. Review and merge dependency PRs promptly.
- **Signed Commits**: All commits **must** be PGP/GPG signed. See [GitHub's signing guide](https://docs.github.com/en/authentication/managing-commit-signature-verification).
- **DCO Sign-off**: Every commit must carry a `Signed-off-by` line:
  ```
  git commit -s -S -m "your commit message"
  ```
- **GitHub Actions Policy**: Workflows may only use actions that are (a) owned by `owncloud`, (b) created by GitHub (`actions/*`), or (c) verified in the GitHub Marketplace.

## Security

**Do not open a public GitHub issue for security vulnerabilities.**

Report vulnerabilities at **<https://security.owncloud.com>** -- see [SECURITY.md](SECURITY.md).

Bug bounty: [YesWeHack ownCloud Program](https://yeswehack.com/programs/owncloud-bug-bounty-program)

## License

This project is licensed under the [AGPL-3.0](LICENSE).

## About the ownCloud OSPO

The [Kiteworks Open Source Program Office](https://kiteworks.com/opensource), operating under
the [ownCloud](https://owncloud.com) brand, launched on May 5, 2026, to steward the open source
ecosystem around ownCloud's products. The OSPO ensures transparent governance, license compliance,
community health, and sustainable collaboration between the open source community and
[Kiteworks](https://www.kiteworks.com), which acquired ownCloud in 2023.

- **OSPO Home**: <https://kiteworks.com/opensource>
- **GitHub**: <https://github.com/owncloud>
- **ownCloud**: <https://owncloud.com>

For questions about the OSPO or licensing, contact ospo@kiteworks.com.

### License Migration to Apache 2.0

The OSPO is driving a strategic relicensing of ownCloud repositories toward the
[Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0), following
the [Apache Software Foundation's third-party license policy](https://www.apache.org/legal/resolved.html).

Individual repositories will migrate as their audit is completed. The LICENSE file
in each repo reflects its **current** license status (not the target).

**Current license: AGPL-3.0** (Category X per Apache policy -- cannot be included in Apache-2.0 works).

Migration prerequisites for this repository:

- **CLA/DCO coverage**: All past contributors must have signed agreements permitting relicensing
- **Copyleft dependency audit**: All AGPL/GPL dependencies must be replaced or isolated
- **KDE heritage review**: Any code with KDE-era copyrights requires legal analysis
- **Complete relicensing**: AGPL-3.0 is a strong copyleft license; migration requires full relicensing of all files, not just a header change
