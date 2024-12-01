Changes v3.1.0
- Included CANCEL macro for user using the sensor macros instead of their own macros
- Pausing printer due to tangle or runnout detection increases printer timeout to 3600s - 1h (configurable by pause_timeout), timeout set back to default 10m minfter print resume.
- improved temperature restore behavior
- Filament automatic unload after runnout can be disabled by variable disable_autochange.
- messages sent to console shows OS2: prefix
