# Supervisor Templates

Native service and timer templates live here in a full installation.

Use the host's own supervisor: launchd on a Mac, systemd on many Linux hosts,
or another deliberately chosen native equivalent. The law is inspectable
startup, restart, cancellation, logging, and recovery—not one supervisor's
name.

Keep service definitions free of secret values. Let them reference an external
credential source and bind network listeners locally unless outward exposure
was separately reviewed.
