# Hemmelig for LazyCat

Hemmelig v7.6.1 (docker.io/hemmeligapp/hemmelig) packaged as a LazyCat LPK (community store).

## Publication

MiaoMiao community store app 668, APPROVED, version 7.6.1. Build run 41128265129 with mirror delivery verification. LPK 37376 bytes; SHA256 e92a385f1e740464b39c241dba41c10d44d66add365dd54e88eff539313d4ca7 downloaded independently and matched at submission.

## Notes

- Single container with healthcheck (/api/health/ready); SQLite + uploads persisted under /lzcapp/var.
- BETTER_AUTH_SECRET via stable_secret; BETTER_AUTH_URL and HEMMELIG_BASE_URL use the {{.S.AppDomain}} template.
- Duplicate check: hemmelig/secret/bin queries all clear in MiaoMiao full catalog (614 apps) before submission.
- No smoke job. Attachments use native browser upload; file-chooser interceptor not wired. Encryption flow not verified on a live device.
