# ansible-role-erlpmd
ansible role for erlpmd - a drop-in replacement for epmd written in Erlang

commands for manual testing:
systemctl daemon-reload
systemctl start erlpmd.service
systemctl status erlpmd.socket
systemctl status erlpmd.service
# if erlpmd.socket is started, connect to port 4369
# this should trigger load of erlpmd.service
telnet localhost 4369
systemctl status erlpmd.service
systemctl stop erlpmd.service
systemctl stop erlpmd.socket
sudo journalctl -xn
