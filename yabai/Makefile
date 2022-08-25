all: restart

restart:
	brew services restart yabai

start:
	brew services start yabai

stop:
	brew services stop yabai

upgrade:
	# src: https://github.com/koekeishiya/yabai/wiki/Installing-yabai-(latest-release)#updating-to-the-latest-release
	# kuba ALL = (root) NOPASSWD: sha256:6ca9d41caee7cb434158ebf35a25cd088609692a3919e194bbdf32aade7cc197 /opt/homebrew/bin/yabai --load-sa
	# stop, and upgrade yabai
	brew services stop yabai
	brew upgrade yabai

	# uninstall the scripting addition
	sudo yabai --uninstall-sa

	# installing the scripting addition will restart Dock.app
	sudo yabai --install-sa

	# finally, start yabai
	brew services start yabai

	open -a "opera GX" https://github.com/koekeishiya/yabai/wiki/Installing-yabai-\(latest-release\)\#macos-big-sur-and-monterey---automatically-load-scripting-addition-on-startup
