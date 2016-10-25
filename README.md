# apache2-vhosts-manager
Scripts for manipulating Apache 2 virtual hosts. Easiest way to setup or delete virtual hosts on testing webserver under Linux.

WARNING! Apache 2 webserver installed requiered. 

To see help guidelines use -h option. Example:
./create_vhost -h
./delete_vhost -h

# Help guide lines for create_vhost
-- Create_vhost v 1.2 HELP output --
----------------------------------
AUTHOR: Alexander Brodilin
E-MAIL: thealexbrodilin@gmail.com
----------------------------------

DESCRIPTION: Creates an apache virtual host using project directory
			 in /var/www/ folder as virtual host root directory.

----------------------------------

OPTIONS:
	-h	Show this help output
	-f	Create directory for virtual host root directory
		 in /var/www/ if it's NOT EXISTS
	-D	Folder name that will be use as a virtual host
		 root directory (it must be placed in /var/www/)
	-H	Virtual host's name (example: somehost.net)
	-C	Virtual host's configuration file name

----------------------------------

ATTANTION! You must be a root user to create virtualhost
Running example:
	 sudo ~/creat_vhost -f -D somedir -H somehost.net -C somehost.conf

----------------------------------

# Help guide lines for delete_vhost
-- Delete_vhost v 1.1 HELP output --
----------------------------------
AUTHOR: Alexander Brodilin
E-MAIL: thealexbrodilin@gmail.com
----------------------------------

DESCRIPTION: Deletes an apache virtual host
			 wich created by create_vhost script early

----------------------------------

OPTIONS:
	-h	Show this help output
	-r	Remove directory used as virtual host root directory
	-C	Virtual host's configuration file name

----------------------------------

ATTANITION! You must be a root user to create virtualhost
Running example:
	 sudo ~/delete_vhost -r -C somehost.conf

----------------------------------
