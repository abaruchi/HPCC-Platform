################################################################################
#    HPCC SYSTEMS software Copyright (C) 2018 HPCC Systems®.
#
#    Licensed under the Apache License, Version 2.0 (the "License");
#    you may not use this file except in compliance with the License.
#    You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
#    Unless required by applicable law or agreed to in writing, software
#    distributed under the License is distributed on an "AS IS" BASIS,
#    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#    See the License for the specific language governing permissions and
#    limitations under the License.
################################################################################

FILE(GLOB xsdFiles "${CMAKE_CURRENT_SOURCE_DIR}/*xsd")
FOREACH( xsdFile ${xsdFiles} )
    get_filename_component( xsdFile2 "${xsdFile}" NAME )
    configure_file(${xsdFile} ${CMAKE_CURRENT_BINARY_DIR}/${xsdFile2})
    Install ( FILES ${CMAKE_CURRENT_BINARY_DIR}/${xsdFile2} DESTINATION componentfiles/configschema/xsd COMPONENT Runtime)
ENDFOREACH ()
