EXTRA_DIST = setup.py suricatasc.in src/__init__.py src/suricatasc.py

if HAVE_PYTHON
all-local:
	mkdir -p $(top_builddir)/scripts/suricatasc/src
	$(PYTHON) $(srcdir)/setup.py build;

install-exec-local:
	$(PYTHON) $(srcdir)/setup.py install --prefix $(DESTDIR)$(prefix)

clean-local:
	$(PYTHON) $(srcdir)/setup.py clean;
	rm -rf $(top_builddir)/scripts/suricatasc/build

uninstall-local:
	[ ! -f "$(DESTDIR)$(prefix)/bin/suricatasc" ] || rm -f "$(DESTDIR)$(prefix)/bin/suricatasc"
	find "$(DESTDIR)$(prefix)/lib" -name "suricatasc-*.egg-info" -delete ||true

distclean-local:
	-rm -rf $(top_builddir)/scripts/suricatasc/src

endif
