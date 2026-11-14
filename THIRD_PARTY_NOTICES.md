# Sources and attribution

The default V5 artist catalog and remote preview URLs were collected from [NovelAI Tag Experiments (NAX), u/Carlyone](https://nax.moe/?gallery=danbooru-artist-tags-2-v5), licensed by its source under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Changes: converted names to underscore tags, deduplicated names, assigned stable IDs, added provenance metadata. Previews are source-hosted generated examples; they are not original artist artworks, male-only tests, or this user's NAI evaluation. Remote assets may change or become unavailable.

[NAI Prompt Studio](https://github.com/shiza2xx/nai-prompt-studio) was consulted to locate the exact NAX V5 gallery and source conventions. Its MIT license does not automatically license third-party images.

Male-appearance counts are independently computed from the latest up to 100 general-rated accessible posts per exact artist tag on [Danbooru's Safebooru mirror](https://safebooru.donmai.us). IDs are deduplicated and character-count tags are tested as a union. Statistics are a partial sample, not an estimate of all works or a model quality score.

[QuickTagCloud V5 artist catalog](https://novelai.quicktagcloud.com/?c=artist_nai5_personal) was inspected: its public v2 release manifest and artist catalog endpoint were identified. Its images/data have not been redistributed in this beta; this integration currently uses NAX as the default catalog. Additional sources can be added without asking the user to prepare JSON.

## QuickTagCloud integration (2026-10-25)

The preceding inspection-only note is superseded: this version links the public V5 personal catalog snapshot from QuickTagCloud. Creator/provider names are retained per entry (including 花枝鱼, 九七, 无冕, 成川姬, W.O.F, community contributors, 雨燕, wwuumm). Source: https://novelai.quicktagcloud.com/?c=artist_nai5_personal . The data release is identified and SHA-256 verified through https://assets.quicktagcloud.com/data/v2/current.json . Catalog version 2026.10.7, site data published 2026-10-21.

Original artwork/example rights remain with their respective creators. The NAX CC BY license does not apply to QuickTagCloud material. Images remain hosted at the source; this project stores only catalog metadata, raw prompts and remote example URLs. Changes: normalized artist names for exact matching, separated the source's single-artist and combination groups, excluded ambiguous individual entries, preserved provider attribution and full combination prompts. No claim is made that original images were generated or evaluated by this application's author.

## Complete source snapshot update

Re-fetched 2026-10-25: catalog version **2026.10.24**, data release `r2-df8200ce521549df946d3cd9c3046cdb814d4dac9c2bbddc6ea7bb7d52159cb7`, published **2026-10-24T16:12:28.930740Z**. All 18,366 source entries are preserved, including the new MayRain collection (12,703 entries). Every entry retains its provider path, raw prompt and remote example/original references; the untouched official JSON is available as `quicktag-original.json`. MayRain is credited per source record alongside the previously listed providers. No rights to remote example images are claimed by this application.


## V4.5 and complete NAX gallery refresh (2026-10-25)

QuickTagCloud [V4.5 personal catalog](https://novelai.quicktagcloud.com/?c=artist_nai45_personal), version 2026.8.23, is now included as metadata with 5,468 source entries (4,334 individual / 1,134 combinations), including 300画师, 千早爱音, 兔兔, W.O.F and 梦神. The official JSON SHA-256 was checked against the release manifest; the original JSON is retained. Rights remain with source creators; no NAX license is asserted for QuickTag material. Preview/source selection and credit appear below each image rather than over the artwork.

The complete current NAX artist galleries were paginated and parsed: danbooru-artist-tags-v5 (9,801), danbooru-artist-tags-2-v5 (17,215), danbooru-artist-tags-male-2-v5 (8,509), danbooru-artist-tags-v4.5 (16,216), danbooru-artist-tags-2-v4.5 (11,282), artists-v4.5 (755). Source: [NAX / u/Carlyone](https://nax.moe/), source license [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Changes: paginated metadata extraction, normalized tags, stable identifiers, model/provider association, per-gallery JSON conversion. Example images are linked remotely without copying image bytes. Captions that cannot safely map to an artist tag remain in the gallery JSON. Artist tags in the transformed NAX records are identifiers, not a transcription of the full generation settings. Different NAX gallery prompts must be consulted at their source pages. These records are not personal evaluations or newly generated tests by this app.

## Kaloscope integration (2026-10-25)

[DraconicDragon/Kaloscope Artist Style Classifier](https://huggingface.co/spaces/DraconicDragon/Kaloscope-artist-style-classifier) is called as an external public service. Its source and model documentation were consulted to validate request/response formats. No model weights, training images, source Python, or model-derived example catalog is bundled by this integration. Model licenses are distinct: the Space source metadata lists Apache-2.0; Kaloscope 3.0 Preview model card lists the DINOv3 license, and Kaloscope 2.0 lists Apache-2.0. Linking an external service does not assert rights to its uploaded images or grant a model license. Inputs are uploaded only when the user starts analysis; prediction scores are not artist identity verification or NovelAI training coverage.

The official `@gradio/client` npm package is used to access the public API. Its npm package metadata declares ISC, while its shipped LICENSE contains the Apache-2.0 text; the shipped LICENSE is reproduced verbatim below. Client-side history is disabled for calls from this app. This app is not affiliated with or endorsed by Kaloscope, Hugging Face, or NovelAI.
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
      outstanding shares, or (iii) beneficial ownership of such entity.

      "You" (or "Your") shall mean an individual or Legal Entity
      exercising permissions granted by this License.

      "Source" form shall mean the preferred form for making modifications,
      including but not limited to software source code, documentation
      source, and configuration files.

      "Object" form shall mean any form resulting from mechanical
      transformation or translation of a Source form, including but
      not limited to compiled object code, generated documentation,
      and conversions to other media types.

      "Work" shall mean the work of authorship, whether in Source or
      Object form, made available under the License, as indicated by a
      copyright notice that is included in or attached to the work
      (an example is provided in the Appendix below).

      "Derivative Works" shall mean any work, whether in Source or Object
      form, that is based on (or derived from) the Work and for which the
      editorial revisions, annotations, elaborations, or other modifications
      represent, as a whole, an original work of authorship. For the purposes
      of this License, Derivative Works shall not include works that remain
      separable from, or merely link (or bind by name) to the interfaces of,
      the Work and Derivative Works thereof.

      "Contribution" shall mean any work of authorship, including
      the original version of the Work and any modifications or additions
      to that Work or Derivative Works thereof, that is intentionally
      submitted to Licensor for inclusion in the Work by the copyright owner
      or by an individual or Legal Entity authorized to submit on behalf of
      the copyright owner. For the purposes of this definition, "submitted"
      means any form of electronic, verbal, or written communication sent
      to the Licensor or its representatives, including but not limited to
      communication on electronic mailing lists, source code control systems,
      and issue tracking systems that are managed by, or on behalf of, the
      Licensor for the purpose of discussing and improving the Work, but
      excluding communication that is conspicuously marked or otherwise
      designated in writing by the copyright owner as "Not a Contribution."

      "Contributor" shall mean Licensor and any individual or Legal Entity
      on behalf of whom a Contribution has been received by Licensor and
      subsequently incorporated within the Work.

   2. Grant of Copyright License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      copyright license to reproduce, prepare Derivative Works of,
      publicly display, publicly perform, sublicense, and distribute the
      Work and such Derivative Works in Source or Object form.

   3. Grant of Patent License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      (except as stated in this section) patent license to make, have made,
      use, offer to sell, sell, import, and otherwise transfer the Work,
      where such license applies only to those patent claims licensable
      by such Contributor that are necessarily infringed by their
      Contribution(s) alone or by combination of their Contribution(s)
      with the Work to which such Contribution(s) was submitted. If You
      institute patent litigation against any entity (including a
      cross-claim or counterclaim in a lawsuit) alleging that the Work
      or a Contribution incorporated within the Work constitutes direct
      or contributory patent infringement, then any patent licenses
      granted to You under this License for that Work shall terminate
      as of the date such litigation is filed.

   4. Redistribution. You may reproduce and distribute copies of the
      Work or Derivative Works thereof in any medium, with or without
      modifications, and in Source or Object form, provided that You
      meet the following conditions:

      (a) You must give any other recipients of the Work or
          Derivative Works a copy of this License; and

      (b) You must cause any modified files to carry prominent notices
          stating that You changed the files; and

      (c) You must retain, in the Source form of any Derivative Works
          that You distribute, all copyright, patent, trademark, and
          attribution notices from the Source form of the Work,
          excluding those notices that do not pertain to any part of
          the Derivative Works; and

      (d) If the Work includes a "NOTICE" text file as part of its
          distribution, then any Derivative Works that You distribute must
          include a readable copy of the attribution notices contained
          within such NOTICE file, excluding those notices that do not
          pertain to any part of the Derivative Works, in at least one
          of the following places: within a NOTICE text file distributed
          as part of the Derivative Works; within the Source form or
          documentation, if provided along with the Derivative Works; or,
          within a display generated by the Derivative Works, if and
          wherever such third-party notices normally appear. The contents
          of the NOTICE file are for informational purposes only and
          do not modify the License. You may add Your own attribution
          notices within Derivative Works that You distribute, alongside
          or as an addendum to the NOTICE text from the Work, provided
          that such additional attribution notices cannot be construed
          as modifying the License.

      You may add Your own copyright statement to Your modifications and
      may provide additional or different license terms and conditions
      for use, reproduction, or distribution of Your modifications, or
      for any such Derivative Works as a whole, provided Your use,
      reproduction, and distribution of the Work otherwise complies with
      the conditions stated in this License.

   5. Submission of Contributions. Unless You explicitly state otherwise,
      any Contribution intentionally submitted for inclusion in the Work
      by You to the Licensor shall be under the terms and conditions of
      this License, without any additional terms or conditions.
      Notwithstanding the above, nothing herein shall supersede or modify
      the terms of any separate license agreement you may have executed
      with Licensor regarding such Contributions.

   6. Trademarks. This License does not grant permission to use the trade
      names, trademarks, service marks, or product names of the Licensor,
      except as required for reasonable and customary use in describing the
      origin of the Work and reproducing the content of the NOTICE file.

   7. Disclaimer of Warranty. Unless required by applicable law or
      agreed to in writing, Licensor provides the Work (and each
      Contributor provides its Contributions) on an "AS IS" BASIS,
      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
      implied, including, without limitation, any warranties or conditions
      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
      PARTICULAR PURPOSE. You are solely responsible for determining the
      appropriateness of using or redistributing the Work and assume any
      risks associated with Your exercise of permissions under this License.

   8. Limitation of Liability. In no event and under no legal theory,
      whether in tort (including negligence), contract, or otherwise,
      unless required by applicable law (such as deliberate and grossly
      negligent acts) or agreed to in writing, shall any Contributor be
      liable to You for damages, including any direct, indirect, special,
      incidental, or consequential damages of any character arising as a
      result of this License or out of the use or inability to use the
      Work (including but not limited to damages for loss of goodwill,
      work stoppage, computer failure or malfunction, or any and all
      other commercial damages or losses), even if such Contributor
      has been advised of the possibility of such damages.

   9. Accepting Warranty or Additional Liability. While redistributing
      the Work or Derivative Works thereof, You may choose to offer,
      and charge a fee for, acceptance of support, warranty, indemnity,
      or other liability obligations and/or rights consistent with this
      License. However, in accepting such obligations, You may act only
      on Your own behalf and on Your sole responsibility, not on behalf
      of any other Contributor, and only if You agree to indemnify,
      defend, and hold each Contributor harmless for any liability
      incurred by, or claims asserted against, such Contributor by reason
      of your accepting any such warranty or additional liability.

   END OF TERMS AND CONDITIONS

   APPENDIX: How to apply the Apache License to your work.

      To apply the Apache License to your work, attach the following
      boilerplate notice, with the fields enclosed by brackets "[]"
      replaced with your own identifying information. (Don't include
      the brackets!)  The text should be enclosed in the appropriate
      comment syntax for the file format. We also recommend that a
      file or class name and description of purpose be included on the
      same "printed page" as the copyright notice for easier
      identification within third-party archives.

   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
