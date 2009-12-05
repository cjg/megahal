man_MANS = megahal.8

EXTRA_DIST = megahal.8.in paper.txt

%: %.in
	sed -e "s/#VERSION#/$(VERSION)/" $< > $@

clean-generic:
	-rm -f megahal.8
