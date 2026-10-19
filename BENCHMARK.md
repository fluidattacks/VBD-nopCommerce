# VBD-nopCommerce: synthetic vulnerability benchmark

This fork is a **synthetic, openly labelled benchmark**. It is not the upstream project
and must not be used as one. Each sample is an isolated pair of branches off `baseline`:

- `baseline`: the pinned upstream commit plus any hardening; the common ancestor.
- `smpl/<NNN>/safe`: the genuine negative (validated control) of sample `NNN`.
- `smpl/<NNN>/vuln`: `safe` plus exactly one commit that weakens the control.

The class and the coordinates of every sample live only in `GROUND_TRUTH.csv` on this
orphan branch, never in the analysed branches.

| sample | file | class |
|---|---|---|
| 001 | `src/Libraries/Nop.Services/Security/AclService.cs` | F115 |
| 002 | `src/Presentation/Nop.Web.Framework/Mvc/Filters/ValidateIpAddressAttribute.cs` | F115 |
| 003 | `src/Presentation/Nop.Web.Framework/Mvc/Filters/ValidatePasswordAttribute.cs` | F115 |
| 004 | `src/Presentation/Nop.Web.Framework/Mvc/Filters/ForceMultiFactorAuthenticationAttribute.cs` | F115 |
| 005 | `src/Presentation/Nop.Web.Framework/Mvc/Filters/CheckAccessClosedStoreAttribute.cs` | F115 |
| 006 | `src/Plugins/Nop.Plugin.Misc.PunchOut/Infrastructure/PunchOutSessionGuardAttribute.cs` | F345 |
| 007 | `src/Libraries/Nop.Services/Security/AclService.cs` | F115 |
| 008 | `src/Libraries/Nop.Services/Security/PermissionService.cs` | F115 |
| 009 | `src/Libraries/Nop.Services/Security/PermissionService.cs` | F115 |
