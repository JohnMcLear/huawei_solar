# AI Policy (JohnMcLear fork)

This is a personal fork of [wlcrs/huawei_solar](https://github.com/wlcrs/huawei_solar),
maintained for one installation: three SUN2000 inverters with batteries in an RS485
cascade behind a single SDongle.

## In this fork

- AI coding agents may write, test, commit and push changes here, under the owner's
  direction. The owner reviews behaviour on the live installation.
- Every change says why it exists, in the commit message or a code comment.
- Agents must not post issues, pull requests or comments on the upstream repository.

## Upstream

Upstream (wlcrs/huawei_solar) does not allow autonomous agents and expects
contributors to write their own descriptions; see its
[AI policy](https://github.com/wlcrs/huawei_solar/blob/main/AI_POLICY.md).
Anything from this fork that goes upstream is submitted by the owner, in his own
words, under that policy.

## Divergence from upstream

- Fast polling intervals (inverter, power meter, energy storage) scale with the number
  of unit ids sharing the Modbus link, at 20 s per unit id with a 30 s minimum
  (`PER_UNIT_UPDATE_INTERVAL` in `const.py`). One inverter is unchanged at 30 s, and
  three cascaded inverters poll every 60 s.

The fork is rebased on upstream releases. Divergences are kept small and listed above.
