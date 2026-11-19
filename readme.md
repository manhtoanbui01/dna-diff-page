<div align="center">

# DNA-Diff — Project Page

### Lighting-Aware Diffusion-based Data Augmentation for<br>Robust Low-Light Re-Identification

**Accepted at BMVC 2026**

Toan Manh Bui · Donghyeok Min · Inyoung Oh · Junghyun Cho

[**View the page →**](https://manhtoanbui01.github.io/dna-diff-page/)

</div>

---

## About

This repository holds the source for the DNA-Diff project page. The page presents
qualitative results only: day-to-night renderings against prior work, illumination
diversity for a single identity, and generalisation to vehicle re-identification.

DNA-Diff turns labelled daytime re-identification data into realistic night-time
training images. It uses learned environment tokens for lighting control and an
IP-Adapter for identity preservation, and needs no paired day/night data.

The paper, code and model weights are not released yet. Links will be added here
and on the page once the BMVC 2026 proceedings are online.

## Contents

```
index.html    the whole page — markup, styles and scripts in one file
figures/      the four result figures the page displays
.nojekyll     serve the files as-is, without Jekyll processing
.github/      optional GitHub Actions deployment workflow
```

The page is deliberately self-contained: no build step, no dependencies and no
external requests at runtime. Everything except the figures lives in `index.html`.

## Previewing locally

Open `index.html` directly in a browser, or serve the directory:

```
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deployment

The page is published with GitHub Pages from the `main` branch. Either Pages
source works:

- **Deploy from a branch** — `main` / `/ (root)`. The workflow in `.github/` is
  then unnecessary and can be deleted.
- **GitHub Actions** — the included workflow publishes on every push to `main`.

## Citation

```bibtex
@inproceedings{dnadiff2026,
  title     = {Lighting-Aware Diffusion-based Data Augmentation for Robust Low-Light Re-Identification},
  author    = {Bui, Toan Manh and Min, Donghyeok and Oh, Inyoung and Cho, Junghyun},
  booktitle = {British Machine Vision Conference (BMVC)},
  year      = {2026},
  note      = {To appear}
}
```

## Acknowledgements

The work builds on [DiVE](https://github.com/BorgDiven/DiVE),
[Stable Diffusion v1.5](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5)
and [diffusers](https://github.com/huggingface/diffusers),
[deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid) for OSNet identity
features, and [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter). Results use the
[NightReID](https://github.com/msm8976/NightReID),
[Market-1501](https://zheng-lab-anu.github.io/Project/project_reid.html) and VeRi-776
datasets.

---

Page template released under the
[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) licence.
Generated imagery is for research use only.
