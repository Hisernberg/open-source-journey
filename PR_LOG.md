# PR & Issue Log — what broke, what I did about it

Method for every contribution: **find a repo and a real, verifiable bug → clone it → reproduce/verify locally (repeated HTTP checks, executed code, or build behavior) → fix or report it → open a professional PR/issue → record issue + solution here → respond to review.**

## Status summary (updated 2026-11-10)

- **huggingface/transformers:** a maintainer asked us to stop mass-opening doc-fix PRs/issues ([feedback on #50568](https://github.com/huggingface/transformers/issues/50568)) — HF prefers handling these in their own automated sweeps. All HF PRs and 3 of 4 HF issues were closed; issue #50568 stays open. **Lesson applied:** no more mass-filing to HF repos; one consolidated, high-value PR at most, in response to explicit review feedback.

- **opencv/opencv:** 3 PRs already **approved by maintainer asmorkalov** (#30748, #30749, #30750), #30754 open. #30747 was correctly closed — the reviewer pointed out the fix was incomplete; the execution-verified corrected fix is #30757 (with an acknowledgment comment on the closed PR).

- **k2-fsa (sherpa-onnx, sherpa-ncnn):** receptive — issues open for triage, PR #4183 got a CodeRabbit review whose actionable point (mirror column no longer a mirror) was fixed by a follow-up commit + thread reply.

## Contributions

### [PR · small] huggingface/transformers — Fix typo "overriden" -> "overridden" in candidate_generator.py comments

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50557
- **Issue found:** Typo `overriden` in generation comments
- **Solution:** Fixed to `overridden`

### [PR · small] huggingface/transformers — Fix duplicated "from from" in OneFormer / Mask2Former attribution comments

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50558
- **Issue found:** Duplicated `from from` in 5 attribution comment lines
- **Solution:** Removed duplication

### [PR · small] huggingface/transformers — Fix dead Kyutai blog link in Helium model doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50559
- **Issue found:** Dead blog link in helium.md
- **Solution:** Removed/updated dead URL

### [PR · small] huggingface/transformers — Fix dead NATTEN link in DiNAT model doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50560
- **Issue found:** Dead NATTEN install link in dinat.md
- **Solution:** Removed/updated dead URL

### [PR · small] huggingface/transformers — Replace dead LMSYS Chatbot Arena link in conversations doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50561
- **Issue found:** Dead LMSYS link in conversations.md
- **Solution:** Replaced with live equivalent

### [PR · small] huggingface/transformers — Fix dead food101 dataset link in image processors doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50562
- **Issue found:** food101 dataset moved (ethz -> zh-plus)
- **Solution:** Replaced with current dataset URL

### [PR · small] huggingface/transformers — Fix FLUTE wheel index URL in Higgs quantization doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50563
- **Issue found:** Dead FLUTE wheel-index URL in higgs.md
- **Solution:** Updated to working index URL

### [PR · small] huggingface/transformers — Remove wildcard suffix from Evolla model tips URL

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50564
- **Issue found:** URL ended in literal `.*` (markdown artifact)
- **Solution:** Stripped wildcard suffix

### [PR · small] huggingface/transformers — Remove wildcard suffix from TiPSv2 model tips URL

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50565
- **Issue found:** URL ended in literal `.*`
- **Solution:** Stripped wildcard suffix

### [PR · small] huggingface/transformers — Remove wildcard suffix from FastSpeech2Conformer model tips URL

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50566
- **Issue found:** URL ended in literal `.*`
- **Solution:** Stripped wildcard suffix

### [PR · small] huggingface/transformers — Fix dead paper link in BiT model doc

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50567
- **Issue found:** arXiv paper page 404 (bit.md)
- **Solution:** Removed dead paper link

### [PR · medium] opencv/opencv — Fix Image Addition tutorial example (np.uint8 inputs and expected output)

- **Status:** closed
- **Link:** https://github.com/opencv/opencv/pull/30747
- **Issue found:** Tutorial example outputs inconsistent with real cv2/NumPy behavior
- **Solution:** Incomplete fix — correctly closed after review; corrected by #30757

### [PR · medium] k2-fsa/sherpa-onnx — Replace dead hf.qhduan.com mirror links with huggingface.co

- **Status:** open
- **Link:** https://github.com/k2-fsa/sherpa-onnx/pull/4183
- **Issue found:** Dead China-mirror host in 8 README links
- **Solution:** Replaced; then re-pointed mirror column at hf-mirror.com after CodeRabbit review

### [PR · small] opencv/opencv — Fix dead OpenEXR downloads link in Windows install guide

- **Status:** open — APPROVED by maintainer
- **Link:** https://github.com/opencv/opencv/pull/30748
- **Issue found:** Dead OpenEXR download link
- **Solution:** Updated to working URL

### [PR · small] opencv/opencv — Fix malformed arXiv markdown link in text spotting tutorial

- **Status:** open — APPROVED by maintainer
- **Link:** https://github.com/opencv/opencv/pull/30749
- **Issue found:** Double-paren malformed markdown link
- **Solution:** Fixed syntax

### [PR · small] opencv/opencv — Fix duplicated URL scheme in raster I/O GDAL tutorial

- **Status:** open — APPROVED by maintainer
- **Link:** https://github.com/opencv/opencv/pull/30750
- **Issue found:** `http://http://` double scheme
- **Solution:** Fixed scheme

### [PR · small] huggingface/transformers — Fix comment typos in generation modules (overridden, useful)

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50572
- **Issue found:** 2 more `overriden` + 1 `usefull` comment typos
- **Solution:** Fixed

### [PR · small] huggingface/transformers — Fix "traning" typo in Japanese model_sharing doc heading

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/pull/50573
- **Issue found:** `traning` heading typo in ja docs
- **Solution:** Fixed to `training`

### [PR · small] opencv/opencv — Fix broken image references to non-existent images/lena.png

- **Status:** open
- **Link:** https://github.com/opencv/opencv/pull/30754
- **Issue found:** lena.png missing from repo in 2 tutorial embeds
- **Solution:** Pointed at existing lena.jpg

### [PR · small] opencv/opencv — Fix Image Addition tutorial: make example shapes consistent (2-D inputs)

- **Status:** open
- **Link:** https://github.com/opencv/opencv/pull/30757
- **Issue found:** Real bug found after #30747 was closed: 1-D inputs make both printed outputs wrong
- **Solution:** 2-D inputs; both outputs verified by executing cv2.add/NumPy

### [PR · small] k2-fsa/sherpa-ncnn — Fix dead Vulkan SDK download link and typos in install-vulkan-macos.md

- **Status:** open
- **Link:** https://github.com/k2-fsa/sherpa-ncnn/pull/447
- **Issue found:** Dead versioned SDK dmg URL + `Introductino`/`Doulbe` typos
- **Solution:** Stable SDK-home link + typos fixed

### [PR · small] huggingface/diffusers — Update dead Kaggle Cats vs Dogs download URL in create_dataset doc

- **Status:** open
- **Link:** https://github.com/huggingface/diffusers/pull/15231
- **Issue found:** Microsoft mirror 404s old version (3367a); verified 5340 live at same path (~825 MB)
- **Solution:** Updated URL in the imagefolder example

### [PR · small] huggingface/diffusers — Fix two dead pipeline-doc links in LoRA loaders doc (qwenimage, z_image)

- **Status:** open (opened after audit)
- **Link:** https://github.com/huggingface/diffusers/pull/15232
- **Issue found:** `pipelines/qwen` and `pipelines/zimage` slugs 404 ×3; correct slugs `qwenimage`/`z_image` verified 200
- **Solution:** Fixed both URLs

### [ISSUE · medium] huggingface/diffusers — Docs: 17 dead external links (verified ×3) — upstream content removed

- **Status:** open (opened after audit)
- **Link:** https://github.com/huggingface/diffusers/issues/15233
- **Issue found:** Sweep of all 1,831 doc URLs; 17 dead where upstream content is gone (deleted repos, removed assets)
- **Solution:** Full evidence table; PRs sent for every fixable one

### [ISSUE · medium] huggingface/transformers — Docs: dead links in model_doc pages (12 URLs return 404)

- **Status:** open
- **Link:** https://github.com/huggingface/transformers/issues/50568
- **Issue found:** 12 dead URLs across model_doc pages
- **Solution:** Evidence table provided

### [ISSUE · small] huggingface/transformers — Docs: dead links in quantization guides (fp-quant collection, HQQ blog)

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/issues/50569
- **Issue found:** Dead quantization-guide URLs
- **Solution:** Evidence table provided

### [ISSUE · small] huggingface/transformers — Docs: dead links in community/guides pages (4 URLs return 404)

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/issues/50570
- **Issue found:** 4 dead URLs in community/guides
- **Solution:** Evidence table provided

### [ISSUE · medium] huggingface/transformers — Docs: broken download/example asset URLs in code examples (7 URLs return 404)

- **Status:** closed
- **Link:** https://github.com/huggingface/transformers/issues/50571
- **Issue found:** 7 dead asset URLs inside runnable code examples
- **Solution:** Evidence table + follow-up sweep comment (4 more found)

### [ISSUE · small] opencv/opencv — Documentation: dead external links in Python tutorials (5 URLs return 404)

- **Status:** open
- **Link:** https://github.com/opencv/opencv/issues/30751
- **Issue found:** 5 dead URLs in py_tutorials
- **Solution:** Evidence table provided

### [ISSUE · small] opencv/opencv — Documentation: dead external links in tutorials (6 URLs return 404/410)

- **Status:** open
- **Link:** https://github.com/opencv/opencv/issues/30752
- **Issue found:** 6 dead URLs in tutorials
- **Solution:** Evidence table provided

### [ISSUE · small] opencv/opencv — Documentation: dead vendor links in config_reference (MediaSDK, Qt)

- **Status:** open
- **Link:** https://github.com/opencv/opencv/issues/30753
- **Issue found:** Dead vendor links
- **Solution:** Evidence table provided

### [ISSUE · small] k2-fsa/sherpa-onnx — nodejs-addon-examples README: dead Cohere Aya Expanse paper link

- **Status:** open
- **Link:** https://github.com/k2-fsa/sherpa-onnx/issues/4182
- **Issue found:** Dead Cohere paper link
- **Solution:** Evidence provided

### [ISSUE · small] k2-fsa/sherpa-onnx — README: dead vendor links (axera-tech, starfivetech, horizon.ai)

- **Status:** open
- **Link:** https://github.com/k2-fsa/sherpa-onnx/issues/4184
- **Issue found:** 3 dead vendor links in main README
- **Solution:** Evidence table provided

### [ISSUE · small] k2-fsa/sherpa-ncnn — README: dead vendor links in Boards section (starfivetech.com, developer.horizon.ai)

- **Status:** open
- **Link:** https://github.com/k2-fsa/sherpa-ncnn/issues/448
- **Issue found:** 2 dead vendor links in sherpa-ncnn README
- **Solution:** Evidence provided; horizon.cc suggestion corrected in follow-up comment

### [COMMENT · medium] huggingface/transformers — Follow-up: 4 more dead documentation-images asset URLs (sweep of all 208)

- **Status:** open (opened after audit)
- **Link:** https://github.com/huggingface/transformers/issues/50571#issuecomment-6769035909
- **Issue found:** Systematic sweep of all 208 asset URLs found 4 more dead
- **Solution:** Evidence table posted on our issue

### [COMMENT · small] opencv/opencv — Acknowledgment on closed #30747 + corrected fix in #30757

- **Status:** open (opened after audit)
- **Link:** https://github.com/opencv/opencv/pull/30747#issuecomment-6770885723
- **Issue found:** My original fix was incomplete; reviewer was right to close
- **Solution:** Posted diagnosis + execution-verified correction

### [COMMENT · small] k2-fsa/sherpa-onnx — CodeRabbit review reply: mirror column restored with hf-mirror.com

- **Status:** open (opened after audit)
- **Link:** https://github.com/k2-fsa/sherpa-onnx/pull/4183#discussion_r4526531187
- **Issue found:** Bot flagged that mirror column duplicated primary links
- **Solution:** Commit 6e0b3db re-points 8 definitions at hf-mirror.com

### [COMMENT · small] k2-fsa/sherpa-ncnn — Correction: horizon.cc replacement not verifiable from my network

- **Status:** open (opened after audit)
- **Link:** https://github.com/k2-fsa/sherpa-ncnn/issues/448#issuecomment-6770925370
- **Issue found:** I had claimed 200 OK without verification
- **Solution:** Posted honest correction

---

## Day-2 evening additions (post-audit)

### [PR · small] scikit-image/scikit-image — docs: fix 6 dead documentation links

- **Status:** open
- **Link:** https://github.com/scikit-image/scikit-image/pull/8401
- **Issue found:** Full sweep of 1,263 doc/README URLs; 6 dead (git-scm book subdomain ×1, numpy howto_document ×3, scipy 1.0.0 release notes ×2); each verified 404 ×3
- **Solution:** All replacements fetched live and confirmed 200 OK (git-scm.com same path; numpydoc format guide; scipy-1.0.0 versioned archive). Deliberately excluded: 2 deleted GitHub user profiles in release notes (historical record) and a 503-transient link.

### [PR · small] pandas-dev/pandas — docs: fix 2 dead links in historical whatsnew notes

- **Status:** open
- **Link:** https://github.com/pandas-dev/pandas/pull/71994
- **Issue found:** Sweep of 703 doc URLs; 2 dead in user-facing whatsnew (renamed JSON-Table-Schema spec; discontinued ScatterCI service); each verified 404 ×3
- **Solution:** table-schema spec URL verified 200 ×3; ScatterCI unlinked, sentence kept. crates.io/calamine 404 excluded as bot-block false positive (API 200; crate exists). Conf.py ignore-list context explained in PR body.

### [PR follow-up] opencv/opencv #30754 — reviewer-requested consistency fix

- **Status:** pushed 5b0f2b1 + replied to reviewer
- **Issue found:** Prasadayus: embed fix alone leaves text/code referencing lena.png (inconsistent)
- **Solution:** Shipped the REAL 512×512 lena.png (from samples/java/clojure/simple-sample/resources/images/) into both tutorial images dirs; all embed/text/code refs now consistently lena.png; dead cp path fixed (+ resource→resources typo)

### [PR maintenance] k2-fsa/sherpa-onnx #4183 — body aligned per CodeRabbit

- **Status:** done (body updated via API)
- **Issue found:** Bot: title/body still said huggingface.co while mirror column points at hf-mirror.com
- **Solution:** PR body aligned; bot thread stays resolved

### [PR · small] tinygrad/tinygrad — docs: point quickstart at abstractions3.py

- **Status:** open
- **Link:** https://github.com/tinygrad/tinygrad/pull/19288
- **Issue found:** quickstart.md links docs/abstractions2.py, removed from repo (404 ×3)
- **Solution:** abstractions3.py verified 200 ×3, covers the same front-to-back hardware walkthrough

### [PR · small] Lightning-AI/pytorch-lightning — docs: fix dead CONTRIBUTING link

- **Status:** open
- **Link:** https://github.com/Lightning-AI/pytorch-lightning/pull/22146
- **Issue found:** README contribution link (lightning.ai …/CONTRIBUTING.html) 404 ×3, with and without utm query
- **Solution:** in-repo .github/CONTRIBUTING.md verified 200 ×3

**Total: 42 contributions (18 open PRs, 10 issues, 13 closed HF PRs, 1 HF issue-closed, comment thread count per log).**

## Day-3 additions

### [PR · engineering] huggingface/transformers — Remove requires_grad workaround from wav2vec-family feature encoders

- **Status:** open
- **Link:** https://github.com/huggingface/transformers/pull/50590
- **Issue found:** #50527 — Dynamo rejects the data-dependent requires_grad assignment, breaking torch.compile(fullgraph=True) training; maintainer direction in-thread: remove the workarounds (reentrant GC unsupported per #49405)
- **Solution:** Removed across 10 models (wav2vec2, hubert, data2vec_audio, wavlm, sew, sew_d, unispeech, unispeech_sat, wav2vec2_conformer, speecht5), generated files refreshed via modular converter (pure deletion, 59 lines). CPU-verified: grads flow, GC use_reentrant=False OK, fullgraph compile now OK.

### [PR · small] scikit-learn/scikit-learn — replace dead contributor URLs with verified GitHub profiles

- **Status:** open
- **Link:** https://github.com/scikit-learn/scikit-learn/pull/35373
- **Issue found:** 4 dead links (3 contributor sites 404 ×3 + 2013 Evernote blog post 404 ×3)
- **Solution:** GitHub profiles substituted ONLY after profile name-field match (MatthieuPerrot, arjoly, willdawson); Evernote "Read more" line removed, testimonial kept. Load-bearing rst targets preserved.

### [PR · small] fastapi/fastapi — fix dead ReDoc vendor extensions link (13 languages)

- **Status:** open
- **Link:** https://github.com/fastapi/fastapi/pull/16732
- **Issue found:** docs moved off redocly/redoc GitHub repo; old md path 404 ×3
- **Solution:** redocly.com/docs/redoc/redoc-vendor-extensions verified 200 ×3 (documents x-logo); applied to en + all 12 translations. Excluded: 20 deleted user profiles in historical contributor lists; GitHub PR-link false positives (bot-blocking).

**Total: 45 contributions.**

## Day-4 (vLLM/SGLang deep-dive + Kaggle/HF ecosystem)

### Reality check: the crowded frontier
- vLLM/SGLang fresh-bug sweep (Nov 6-10): 25+ issues timeline-checked — every well-reported issue already has a linked PR within ~24h, or needs GPUs/design buy-in. Hot new architectures (Gemma4 3.4M dl/mo, GlmMoeDsa 1.2M, Qwen3_5Moe 435K) are ALL already supported in both vLLM and SGLang.
- transformers #50590 (wav2vec requires_grad workaround removal) was closed by @vasqu: maintainer PR #50544 already existed for the same issue (not visible in the issue thread). Closed as duplicate — fair. Lesson institutionalized: timeline/linked-PR check BEFORE implementation (was applied this session and saved 3 duplicate attempts: sglang #49403/#49550, vllm #66436).

### [Issue contribution] Kaggle/kaggle-cli #1207 — wire-level verification
- Comment: https://github.com/Kaggle/kaggle-cli/issues/1207#issuecomment-6775197881
- Simulated the real client flow offline (blob upload mocked): the wire JSON carries files[].description + files[].columns[].description correctly on main (kagglesdk 0.1.38). Isolated the drop to the server; saved maintainers a client-side investigation.

### [Review contribution] Kaggle/kagglehub #323 — execution-verified review
- Review: https://github.com/kaggle/kagglehub/pull/323#pullrequestreview-5846923724
- Ran the PR's suite on the branch (16 passed incl. 3 new range regressions); verified restart truncation safety ("wb" at size_read=0), complete Content-Range validation, no stream leak on rejection. Non-blocking follow-up suggested (missing-header test case).

### Contribution count: 45 PRs+issues + 2 high-signal review/verification comments = 47 total touchpoints.

### [Review contributions] huggingface/huggingface_hub — two execution-verified reviews
- #5282 (exclusive-create, buffered path): 11 targeted tests pass on branch; found + verified the stream-path gap (block_size=0 + "x" still silently discards writes — confirmed by source); suggested aligning stream/buffered on FileExistsError, cross-referenced companion PR #5287. https://github.com/huggingface/huggingface_hub/pull/5282#pullrequestreview-5847185872
- #5287 (stream rejects write modes): 12 targeted tests pass; disproved the text-mode regression concern (fsspec normalizes "r"→"rb" before _open — verified in fsspec source); flagged the "r"/"rb+" direct-construction narrowing as intentional-but-worth-documenting; suggested unified semantics with #5282. https://github.com/huggingface/huggingface_hub/pull/5287#pullrequestreview-5847186258

### Status: 3 PRs fully green (pandas #71994 clean, fastapi #16732 clean, tinygrad #19288 clean) — awaiting maintainer merges.

## Day-4 session 2: sympy deep engineering (umbrella #31017) + rich fixes

### sympy — item W1 of #31017 (30-defect umbrella issue; only W13 was claimed)
- **PR #31033 OPEN**: `solvers: enumerate all monic root divisors in rsolve_hyper`. Root cause beyond the report: `roots(p/q, n).keys()` dropped multiplicities AND the hand-built candidate list never built products of distinct roots — ratios like `1/(n+1)**2` (W1a) and `(n+1)*(n+2)` (W1b) were unreachable → rsolve returned 0. Replaced with full monic-divisor enumeration (Petkovšek), preserving integer shift-coprime pruning; added complex-shift candidate skip (found via test_rsolve_0_sol_homogeneous regression — quadratic with complex roots crashed product()/combsimp). 424/424 solvers tests pass. https://github.com/sympy/sympy/pull/31033
- **C8 fix DONE (PR pending)**: `_ItemGetter.__hash__` missing → every ProductOrder unhashable. Fixed + hash tests added; note: groebner with product order then hits the deeper #8033 IndexError (documented). Branch pushed to fork; PR creation blocked by temporary GH anti-abuse flag on cross-fork PRs (diagnosed: comments 201, own-repo PRs 201, cross-fork 404 even for previously-successful branch). Retry scheduled.

### rich — two precise bug reports reproduced + fixed
- **#4250**: FileProxy.write() returned 0 — loop consumed `text` before `return len(text)`. Fixed by tracking consumed length. 
- **#4256**: Text.right_crop(-1) truncated from START and grew length; amount > len drove _length negative (found the overshoot case with my own edge tests). Fixed by clamping to [0, len].
- Both verified with edge cases; 117 relevant tests pass; 8 pre-existing env failures identical on clean main (ANSI/pygments). 2 more failures proved flaky (pass on my tree, fail on clean — pygments hash-seed). PRs queued (same GH flag).

### Infrastructure learnings
- GitHub anti-abuse flagging: new account + rapid successive cross-fork PRs → POST /pulls returns 404 (not 422!) while GET/issue-comments/own-repo writes stay 201. Pace PR creation.
