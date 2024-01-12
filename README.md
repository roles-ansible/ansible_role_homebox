[![Ansible Galaxy](https://ansible.l3d.space/svg/l3d.homebox.svg)](https://galaxy.ansible.com/ui/standalone/roles/l3d/homebox/)
[![BSD-3 Clause](https://ansible.l3d.space/svg/l3d.homebox_license.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.homebox_maintainance.svg)](https://ansible.l3d.space/#l3d.homebox)

 ansible role homebox
=======================
Ansible role to install [homebox](https://github.com/hay-kot/homebox.git), the inventory and organization system built for Home User. With a focus on simplicity and ease of use, Homebox is the perfect solution for your home inventory, organization, and management needs.

## Variables
### Version and Unix
| name | default | description |
| | |
| ``homebox__version`` | ``latest`` | latest for latest github release or specify a version |
| ``homebox__executable_path`` | ``/usr/local/bin/homebox`` | path to binary |
| ``homebox__user`` | ``homebox`` | Unix User |
| ``homebox__group`` | ``homebox`` | Unix Group |
| ``homebox__home`` | ``/var/lib/homebox`` | project homebox system home |
| ``homebox__user_home`` | ``{{ homebox__home }}`` | Unix User home |

### Systemd and Configuration
| name | default | description |
| | |
| ``homebox__env_mode`` | ``production`` | development or production |
| ``homebox__env_web_host`` | ``*`` | where to bind service *(127.0.0.1 possible)* |
| ``homebox__env_web_port`` | ``7745`` | Port for application |
| ``homebox__env_web_max_upload_size`` | ``10`` | max upload size |
| ``homebox__env_web_read_timeout`` | ``10`` | web read timeout |
| ``homebox__env_web_write_timeout`` | ``10`` | web write timeout |
| ``homebox__env_web_idle_timeout`` | ``30`` | web idle timeout |
| ``homebox__env_storage_data`` | ``{{ homebox__home }}/data`` | data storage |
| ``homebox__env_storage_sqlite_url`` | *(see dafaults/main.yml)* | sqlite database path |
| ``homebox__env_log_level`` | ``warning`` | log level |
| ``homebox__env_log_format`` | ``text`` | log format |
| ``homebox__set_mail`` | ``false`` | configure mail parameters |
| ``homebox__env_mailer_host`` | | |
| ``homebox__env_mailer_port`` | | |
| ``homebox__env_mailer_username`` | | |
| ``homebox__env_mailer_password`` | | |
| ``homebox__env_mailer_from`` | | |
| ``homebox__env_demo`` | ``false`` | demo mode |
| ``homebox__env_debug_enabled`` | ``false`` | debugging |
| ``homebox__env_debug_port`` | ``4000`` | debugging port |
| ``homebox__env_options_allow_registration`` | ``true`` | allow registration without invite link |
| ``homebox__env_options_auto_increment_asset_id`` | ``true`` | |
| ``homebox__systemd_cap_net_bind_service`` | ``false`` | |
| ``submodules_versioncheck`` | ``false`` | optionally enable simple ansible versionscheck |
