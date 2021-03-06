# Copyright © 2016 Canonical Ltd.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 3 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.
#
# Authored by: Alexandros Frantzis <alexandros.frantzis@canonical.com>

add_executable(
    repowerd-brightness-tool

    brightness_tool.cpp
)

target_link_libraries(
    repowerd-brightness-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

add_executable(
    repowerd-cli

    cli.cpp
)

target_link_libraries(
    repowerd-cli

    repowerd-core
    repowerd-adapters
)

add_executable(
    repowerd-light-tool

    light_tool.cpp
)

target_link_libraries(
    repowerd-light-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

add_executable(
    repowerd-power-source-tool

    power_source_tool.cpp
    ../default_daemon_config.cpp
)

target_link_libraries(
    repowerd-power-source-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

add_executable(
    repowerd-proximity-tool

    proximity_tool.cpp
)

target_link_libraries(
    repowerd-proximity-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

add_executable(
    repowerd-session-tool

    session_tool.cpp
)

target_link_libraries(
    repowerd-session-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

add_executable(
    repowerd-wakeup-tool

    wakeup_tool.cpp
)

target_link_libraries(
    repowerd-wakeup-tool

    repowerd-core
    repowerd-adapters
    repowerd-default-daemon-config
)

install(
    TARGETS
        repowerd-brightness-tool
        repowerd-cli
        repowerd-light-tool
        repowerd-proximity-tool
        repowerd-wakeup-tool
    RUNTIME DESTINATION sbin
)
