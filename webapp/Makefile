compile:
	rapydscript compile -b js/folder.pyj > lib/folder.js
	rapydscript compile -b js/jappy.pyj > lib/jappy.js
	riot --config js/riot.config.js --ext tag.html js/ lib/
sw:
	workbox generateSW
watch:
	riot --colors --watch --config js/riot.config.js --ext tag.html js/ lib/
dist_xo:
	python setup.py dist_xo
genpot:
	xgettext js/*.tag.html --language=Python --from-code=utf-8 -o jappy.pot --copyright-holder "Jappy Authors" --package-name="Jappy"
genjson:
	cat po/*.po | rapydscript msgfmt > jappy.json
test:
	pytest --driver Chrome
