# Copyright (c) 2017, Broadband Forum
#
# Redistribution and use in source and binary forms, with or
# without modification, are permitted provided that the following
# conditions are met:
#
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
#
# 2. Redistributions in binary form must reproduce the above
#    copyright notice, this list of conditions and the following
#    disclaimer in the documentation and/or other materials
#    provided with the distribution.
#
# 3. Neither the name of the copyright holder nor the names of its
#    contributors may be used to endorse or promote products
#    derived from this software without specific prior written
#    permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND
# CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES,
# INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
# MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
# DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR
# CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
# SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT
# NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
# LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
# CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT,
# STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
# ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
# ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#
# The above license is used as a license under copyright only.
# Please reference the Forum IPR Policy for patent licensing terms
# <https://www.broadband-forum.org/ipr-policy>.
#
# Any moral rights which are necessary to exercise under the above
# license grant are also deemed granted under this license.

TOPDIR = ..

include $(TOPDIR)/defs.mk

REPORTFLAGS += --allbibrefs

# XXX this is to disable schema validation, because this currently requires
#     schema filenames to include the minor version number
REPORTFLAGS += --loglevel=error

include $(TOPDIR)/rules.mk

# check bibrefs
# XXX "echo | tr" is used to remove the newline and is to avoid use of
#     "echo -n", which isn't always available
BIBREF-CHECK = bibref-check.txt

bibref-check: $(BIBREF-CHECK)

$(BIBREF-CHECK): tr-069-biblio.xml
	(for i in `grep '<hyperlink>' $< | \
	   sed -e 's/.*<hyperlink>//' -e 's/<\/hyperlink>.*//'`; do \
	     echo "$$i: " | tr -d '\012'; \
	     curl -IfsS $$i >/dev/null; \
	     if [ $$? != 0 ]; then \
	       j=$${i/https:/http:}; \
	       echo "$$j " | tr -d '\012'; \
	       curl -IfsS $$j >/dev/null; \
	     fi; \
	     echo; \
	   done \
	) 2>&1 | tee $@
