# Copyright (C) 2006 MySQL AB
# 
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA

include_directories ( ${CMAKE_SOURCE_DIR}/dbug )

set ( DBUG_SOURCES dbug.c factorial.c sanity.c )

if ( NOT SOURCE_SUBLIBS )
  include_directories ( ${CMAKE_SOURCE_DIR}/include )
  add_library ( dbug STATIC ${DBUG_SOURCES} )
endif ( NOT SOURCE_SUBLIBS )
