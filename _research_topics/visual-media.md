---
topic_id: visual-media
title: Visual Media
order: 5
summary: Imaging, restoration, generation, and cinematic quality control for real-world capture.
hero_image: /assets/images/visual-media/framework.png
intro_video: /assets/images/visual-media/video-generation-example.mp4
---

<style>
  article:has(.topic-page-marker[data-topic="visual-media"]) > figure {
    max-width: 70%;
    margin-left: auto;
    margin-right: auto;
  }
  .vm-media-grid {
    display: grid;
    gap: 1rem;
    margin: 1.5rem 0 2.5rem;
  }
  .vm-media-grid.cols-2 { grid-template-columns: repeat(2, 1fr); }
  .vm-media-grid figure { margin: 0; }
  .vm-media-grid img,
  .vm-media-grid video {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 0.75rem;
    box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  }
  .vm-media-grid figcaption {
    font-size: 0.85rem;
    color: #6b7280;
    margin-top: 0.5rem;
    text-align: center;
  }
  .vm-media-single {
    margin: 1.5rem auto 2.5rem;
    max-width: 80%;
  }
  .vm-media-single img,
  .vm-media-single video {
    width: 100%;
    height: auto;
    border-radius: 0.75rem;
    box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  }
  .vm-media-single figcaption {
    font-size: 0.85rem;
    color: #6b7280;
    margin-top: 0.5rem;
    text-align: center;
  }
  @media (max-width: 700px) {
    .vm-media-grid.cols-2 { grid-template-columns: 1fr; }
    .vm-media-single { max-width: 100%; }
  }
</style>
<span class="topic-page-marker" data-topic="visual-media" hidden></span>

Visual media research covers **low-level vision**, **computational photography**, and **generative pipelines** where fidelity and latency both matter. Topics include denoising and deblurring, HDR fusion, reference-guided restoration, and evaluation that aligns with human preference studies rather than single PSNR numbers.

### Image and Video Generation and Editing

Image and video generation and editing aim to synthesize new visual content from text, references, sketches or layouts, and to modify existing content with pixel-level precision — replacing an object, changing the lighting, preserving an identity, completing a missing region — while leaving everything else untouched. The two tasks are not separate: editing is generation under the strongest possible constraint, where the model must simultaneously understand the user's intent and respect every unspecified pixel of the original.

These technologies sit at the entry point of modern visual creation. They underpin smartphone computational photography, professional film and television post-production, e-commerce visual design, advertising, virtual production, dataset synthesis for training other AI systems, and accessible creative tools for non-expert users. As large generative models become the standard substrate for visual content, generation and editing increasingly serve as the upper-level interface through which all downstream low-level tasks — restoration, enhancement, super-resolution — can be reformulated as conditional generation problems. Our work in this direction focuses on controllable, identity-preserving, and reference-aware models that bridge the gap between "looks good" and "is faithful," and on bringing professional-grade control to a single, unified architecture.

<div class="vm-media-grid cols-2">
  <figure>
    <img src="{{ '/assets/images/visual-media/image-generation-example.webp' | relative_url }}" alt="Image generation example" loading="lazy" decoding="async" />
    <figcaption>Image generation example</figcaption>
  </figure>
  <figure>
    <video src="{{ '/assets/images/visual-media/video-generation-example.mp4' | relative_url }}" autoplay muted loop playsinline preload="metadata"></video>
    <figcaption>Video generation example</figcaption>
  </figure>
</div>

### Image and Video Restoration and Enhancement

Image and video restoration and enhancement aim to transform low-quality visuals — those degraded by low resolution, noise, compression artifacts, blur and various other distortions — into high-quality images and videos. Restoration assumes the original signal once existed and seeks to recover it faithfully; enhancement goes one step further to synthesize plausible detail that was never fully captured in the first place. The two share a common backbone: both must invert real-world degradation processes and respect the geometry, identity and temporal coherence of the source.

These technologies are critical across numerous applications, including computational photography on smartphones, the restoration of historical photographs, cultural heritage preservation, artistic creation, digital archiving, medical imaging and autonomous driving. For videos, they significantly improve film production, content generation, streaming quality and surveillance analysis. Beyond delivering visually pleasing results, restoration and enhancement also produce better inputs for downstream perception tasks such as detection, recognition and tracking — making them a foundational layer of the broader visual AI stack. With the rapid advancement of deep learning, the field now faces higher expectations on fidelity, perceptual quality assessment, interpretability and the ability to generalise across truly real-world degradations. Our work in this direction targets exactly these frontiers: pushing low-level vision from "looks better" to "is provably faithful," and from synthetic benchmarks to the long tail of real-world data.

<div class="vm-media-grid cols-2">
  <figure>
    <img src="{{ '/assets/images/visual-media/img2_blur.jpg' | relative_url }}" alt="Degraded input" loading="lazy" decoding="async" />
    <figcaption>Input — degraded</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/images/visual-media/img2_clear.jpg' | relative_url }}" alt="Restored output" loading="lazy" decoding="async" />
    <figcaption>Restored — recovered detail</figcaption>
  </figure>
</div>

<figure class="vm-media-single">
  <img src="{{ '/assets/images/visual-media/hypir-7.gif' | relative_url }}" alt="HYPIR restoration animation" loading="lazy" decoding="async" />
  <figcaption>HYPIR — animated restoration result</figcaption>
</figure>

<div class="vm-media-grid cols-2">
  <figure>
    <img src="{{ '/assets/images/visual-media/hypir-b-1.png' | relative_url }}" alt="HYPIR result 1" loading="lazy" decoding="async" />
    <figcaption>HYPIR — result A</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/images/visual-media/hypir-b-2.png' | relative_url }}" alt="HYPIR result 2" loading="lazy" decoding="async" />
    <figcaption>HYPIR — result B</figcaption>
  </figure>
</div>

### In Cooperation With

Tooling collaborations with broadcast archives and mobile OEMs on perceptual metrics, on-device super-resolution, and dataset curation for under-represented sensors.

<div class="topic-cooperation-logos">
  <a href="https://example.org/sponsor-b" target="_blank" rel="noopener" title="Vision Industry Partner">
    <img src="{{ '/site-covers/sponsors/brand-logo-3.svg' | relative_url }}" alt="Vision Industry Partner" loading="lazy" decoding="async" />
  </a>
  <img src="{{ '/site-covers/sponsors/brand-logo-5.svg' | relative_url }}" alt="University Initiative" loading="lazy" decoding="async" />
</div>
