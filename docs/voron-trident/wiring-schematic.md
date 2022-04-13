---
layout: default
title: Wiring Schematic
parent: Voron Trident
permalink: /docs/collections/voron-trident/wiring-schematic
nav_order: 4
---

# Wiring Schematic
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}

---

<main>
	<section id="wiring">
		<div id="image-00">
			<img src="../../../../assets/images/wiring-00-hardware.png" id="00-hardware" />
		</div>
		<div id="image-01" style="display:float;">
			<img src="../../../../assets/images/wiring-01-mains.png" id="01-mains" />
		</div>
		<div id="image-02" style="display:float;">
			<img src="../../../../assets/images/wiring-02-bed.png" id="02-bed" />
		</div>
		<div id="image-03" style="display:float;">
			<img src="../../../../assets/images/wiring-03-dc.png" id="03-dc" />
		</div>
		<div id="image-04" style="display:float;">
			<img src="../../../../assets/images/wiring-04-pi.png" id="04-pi" />
		</div>
		</section>
</main>

[All](javascript: void(0)){: .btn .btn-outline .button00 }
[Mains Wiring](javascript: void(0)){: .btn .btn-outline .button01 }
[Bed Cable Hookup](javascript: void(0)){: .btn .btn-outline .button02 }
[DC Power](javascript: void(0)){: .btn .btn-outline .button03 }
[Raspberry Pi](javascript: void(0)){: .btn .btn-outline .button04 }
[Hide All](javascript: void(0)){: .btn .btn-outline .button99 }

<script>
document.addEventListener('DOMContentLoaded', function (event) {
	var wiring = document.getElementById('wiring');
	var image_00 = document.getElementById('image-00');
	var image_01 = document.getElementById('image-01');
	var image_02 = document.getElementById('image-02');
	var image_03 = document.getElementById('image-03');
	var image_04 = document.getElementById('image-04');

	var button00 = document.querySelector('.button00');
	var button01 = document.querySelector('.button01');
	var button02 = document.querySelector('.button02');
	var button03 = document.querySelector('.button03');
	var button04 = document.querySelector('.button04');
	var button99 = document.querySelector('.button99');

	gsap.set(wiring, {height: image_00.offsetHeight});

	button00.addEventListener('click', toggleOpacity);
	button01.addEventListener('click', toggleOpacity);
	button02.addEventListener('click', toggleOpacity);
	button03.addEventListener('click', toggleOpacity);
	button04.addEventListener('click', toggleOpacity);
	button99.addEventListener('click', toggleOpacity);

	function onResize () {
		gsap.set(wiring, {height: image_00.offsetHeight});
		gsap.set(image_01, {y: 0-image_00.offsetHeight});
		gsap.set(image_02, {y: 0-image_00.offsetHeight*2});
		gsap.set(image_03, {y: 0-image_00.offsetHeight*3});
		gsap.set(image_04, {y: 0-image_00.offsetHeight*4});
	}

	function toggleOpacity () {
		var target = this;
		<!--console.log(target.className);-->

		switch (target.className) {
			case "btn btn-outline button00":
				gsap.to(image_01, {duration: .2, opacity: 1});
				gsap.to(image_02, {duration: .2, opacity: 1});
				gsap.to(image_03, {duration: .2, opacity: 1});
				gsap.to(image_04, {duration: .2, opacity: 1});
				break;
			case "btn btn-outline button01":
				gsap.to(image_01, {duration: .2, opacity: 1});
				gsap.to(image_02, {duration: .2, opacity: .1});
				gsap.to(image_03, {duration: .2, opacity: .1});
				gsap.to(image_04, {duration: .2, opacity: .1});
				break;
			case "btn btn-outline button02":
				gsap.to(image_01, {duration: .2, opacity: .1});
				gsap.to(image_02, {duration: .2, opacity: 1});
				gsap.to(image_03, {duration: .2, opacity: .1});
				gsap.to(image_04, {duration: .2, opacity: .1});
				break;
			case "btn btn-outline button03":
				gsap.to(image_01, {duration: .2, opacity: .1});
				gsap.to(image_02, {duration: .2, opacity: .1});
				gsap.to(image_03, {duration: .2, opacity: 1});
				gsap.to(image_04, {duration: .2, opacity: .1});
				break;
			case "btn btn-outline button04":
				gsap.to(image_01, {duration: .2, opacity: .1});
				gsap.to(image_02, {duration: .2, opacity: .1});
				gsap.to(image_03, {duration: .2, opacity: .1});
				gsap.to(image_04, {duration: .2, opacity: 1});
				break;
			case "btn btn-outline button99":
				gsap.to(image_01, {duration: .2, opacity: .1});
				gsap.to(image_02, {duration: .2, opacity: .1});
				gsap.to(image_03, {duration: .2, opacity: .1});
				gsap.to(image_04, {duration: .2, opacity: .1});
				break;
		}
	}

	window.addEventListener('resize', onResize);
	window.addEventListener('load', onResize);
})
</script>