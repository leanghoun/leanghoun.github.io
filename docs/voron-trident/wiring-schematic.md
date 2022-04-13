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
		</section>
</main>

[Mains Wiring](javascript: void(0)){: .btn .btn-outline .button01 }
[Bed Cable Hookup](javascript: void(0)){: .btn .btn-outline .button02 }

<script>
document.addEventListener('DOMContentLoaded', function (event) {
	var wiring = document.getElementById('wiring');
	var image_00 = document.getElementById('image-00');
	var image_01 = document.getElementById('image-01');
	var image_02 = document.getElementById('image-02');

	var button01 = document.querySelector('.button01');
	var button02 = document.querySelector('.button02');

	gsap.set(wiring, {height: image_00.offsetHeight});

	button01.addEventListener('click', toggleOpacity);
	button02.addEventListener('click', toggleOpacity);

	function onResize () {
		gsap.set(wiring, {height: image_00.offsetHeight});
		gsap.set(image_01, {y: 0-image_00.offsetHeight});
		gsap.set(image_02, {y: 0-image_00.offsetHeight*2});
	}

	function toggleOpacity () {
		var target = this;
		<!--console.log(target.className);-->

		switch (target.className) {
			case "btn btn-outline button01":
				gsap.to(image_01, {duration: .2, delay: .3, opacity: 1});
				gsap.to(image_02, {duration: .2, opacity: .2});
				break;
			case "btn btn-outline button02":
				gsap.to(image_01, {duration: .2, opacity: .2});
				gsap.to(image_02, {duration: .2, delay: .3, opacity: 1});
				break;
		}
	}

	window.addEventListener('resize', onResize);
	window.addEventListener('load', onResize);
})
</script>