uclalib_role_ffmpeg
=========

Ansible role to install a static binary build of ffmpeg on a RHEL system

Requirements
------------

None.

Role Variables
--------------

* `ffmpeg_base_url` - defines the home page/base url where ffmpeg is made available

* `ffmpeg_version` - defines the version of ffmpeg to obtain (e.g. `4.0.1`)

* `ffmpeg_install_dir` - defines the directory to install ffmpeg

* `ffmpeg_user_path_dir` - define the directory to place a symblink in the user path

FFMpeg Download URL Note
------------------------

The default value for the `ffmpeg_download_url` variable is:

`http://pkgs.library.ucla.edu/ffmpeg/ffmpeg-{{ ffmpeg_version }}-amd64-static.tar.xz`

You can override this variable to obtain ffmpeg from the source by using:

`https://johnvansickle.com/ffmpeg/releases/ffmpeg-{{ ffmpeg_version }}-amd64-static.tar.xz`

Versions of FFMpeg available via the UCLA URL are:

* `4.1`
* `4.1.4`

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: uclalib_role_ffmpeg, ffmpeg_version: '4.1.4' }
