# DOCS Makefile for should

# this file is part of SHOULD

# Copyright (c) 2009 Claudio Calvelli <should@shouldbox.co.uk>

# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, version 3 of the License.

# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.

# You should have received a copy of the GNU General Public License
# along with this program (see the file COPYING in the distribution).
# If not, see <http://www.gnu.org/licenses/>.

include ../Site.make

.PHONY : install

install :
	install -d $(INSTALLDOC)
	awk '/^doc\// && ! /(Makefile|\.1)$$/ { print substr($$0, 5) }' ../MANIFEST | \
	while read name; do install $$name $(INSTALLDOC); done
	install -d $(INSTALLMAN1)
	awk '/^doc\// && /\.1$$/ { print substr($$0, 5) }' ../MANIFEST | \
	while read name; do install $$name $(INSTALLMAN1); done

