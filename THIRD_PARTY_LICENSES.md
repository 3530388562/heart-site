# 第三方开源许可声明（Third-Party Licenses）

本产品（粒子爱心 · 流星雨 · 手势烟花 APK）包含由 Google LLC 提供的 **MediaPipe Hands** 相关代码与模型文件。  
除下述第三方组件外，本产品的其余全部源代码（粒子爱心渲染、烟花系统、手势状态机、界面逻辑等）均为作者（网名：Guitar）原创，作者保留全部版权。

---

## 1. MediaPipe Hands（Google LLC）

**许可协议**：Apache License, Version 2.0（以下简称 "Apache 2.0"）  
**官方仓库**：<https://github.com/google-ai-edge/mediapipe>  
**许可证全文**：<http://www.apache.org/licenses/LICENSE-2.0>

本产品捆绑并分发了以下 MediaPipe 文件（位于 `app/src/main/assets/mediapipe/`）：

| 文件                                                        | 类型                                                                                         |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| `hands.js`                                                | 运行时脚本（源码头部已含 `Copyright The Closure Library Authors. SPDX-License-Identifier: Apache-2.0`） |
| `hands_solution_simd_wasm_bin.js` / `.wasm`               | WASM 推理引擎                                                                                  |
| `hands_solution_wasm_bin.js` / `.wasm`                    | WASM 推理引擎（非 SIMD 回退）                                                                       |
| `hands_solution_packed_assets_loader.js` / `.data`        | 资源包                                                                                        |
| `hands.binarypb`                                          | 计算图定义                                                                                      |
| `hands_solution_simd_wasm_bin.data`                       | 空占位文件（0 字节，随发行版附带）                                                                         |
| `hand_landmark_full.tflite` / `hand_landmark_lite.tflite` | 手部关键点模型权重（Model Card 注明 `LICENSED UNDER Apache License, Version 2.0`）                      |

上述文件以未修改（as-is）形式分发，作者未对 MediaPipe 源码本身进行修改。

### 版权归属与二进制内含组件（商业分发补充）

- `hands.js` 源码头部载明：`Copyright The Closure Library Authors. SPDX-License-Identifier: Apache-2.0`。
- 其余运行时脚本、WASM 二进制、计算图与 `.tflite` 模型权重的版权归 The MediaPipe Authors / Google LLC 所有。
- `.wasm` / `.data` / `.tflite` 为 Google 发布的预编译产物，内部可能包含 TensorFlow Lite、XNNPACK、Emscripten 运行时等第三方组件，各自许可随 MediaPipe 发行版提供，见官方仓库 <https://github.com/google-ai-edge/mediapipe>。本产品未修改其中任何文件；如日后修改，须逐文件显著标注。
- 本声明的完整可读副本同时内置于 APK 的 `assets/THIRD_PARTY_LICENSES.html`，并在每次构建的 Artifacts 中随 APK 一并提供，以履行 Apache 2.0 第 4 条的附文义务；应用内工具栏也提供「开源许可」入口，可直接点开查看全文（购买者即使只收到 APK 也能查阅）。
- 本产品**未**使用 "Google"、"MediaPipe"、"抖音" 等第三方商标或平台名称作为产品背书、来源暗示或宣传用语；对外描述功能时请使用中性表述。
- 本产品商用时，请连同本文件（或 APK 内置的 HTML 副本）一并提供给购买者。

### Apache 2.0 对使用方的要求摘要

1. 在分发时保留本版权声明与许可证文本（即本文件）。
2. 若修改了前述文件，须明确标注修改。
3. **不得使用 "MediaPipe"、"Google" 名称或商标为本品背书或推广**，除非获得 Google 明确书面许可。
4. 本产品依 "AS IS" 基础提供，不附任何明示或默示担保（含对模型精度、适用性的担保）。

---

## 2. 商标与名义使用限制

"MediaPipe" 及 "Google" 为 Google LLC 的商标。本产品仅在 Apache 2.0 允许范围内使用其开源代码与模型，**未获得 Google 任何形式的合作、认证或背书**。任何将本品描述为"由 Google 提供/认证/推荐"的行为均超出许可范围，作者概不负责。

---


## 3. 作者原创代码声明

本产品的全部业务代码（爱心粒子生成与渲染、流星雨、夜空烟花编排、手势识别状态机、快速通道优化、UI 与构建配置等）由作者（网名：Guitar）独立编写，版权归作者所有。MediaPipe 仅为被调用的本地推理组件，其许可义务已在本文件中单独、完整地披露。

---

以下为 Apache License, Version 2.0 完整文本（应 Apache 2.0 第 4 条要求随分发提供）：

---

```
                             Apache License
                       Version 2.0, January 2004
                    http://www.apache.org/licenses/
```

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

   (a) You must give any other recipients of the Work or Derivative  
   Works a copy of this License; and

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
   of the NOTICE file are for informational purposes only and do  
   not modify the License. You may add Your own attribution notices  
   within Derivative Works that You distribute, alongside or as an  
   addendum to the NOTICE text from the Work, provided that such  
   additional attribution notices cannot be construed as modifying  
   the License.

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

```
  To apply the Apache License to your work, attach the following
  boilerplate notice, with the fields enclosed by brackets "[]"
  replaced with your own identifying information. (Don't include
  the brackets!)  The text should be enclosed in the appropriate
  comment syntax for the file format. We also recommend that a
  file or class name and description of purpose be included on the
  same "printed page" as the copyright notice for easier
  identification within third-party archives.
```

Copyright [yyyy] [name of copyright owner]

Licensed under the Apache License, Version 2.0 (the "License");  
you may not use this file except in compliance with the License.  
You may obtain a copy of the License at

```
   http://www.apache.org/licenses/LICENSE-2.0
```

Unless required by applicable law or agreed to in writing, software  
distributed under the License is distributed on an "AS IS" BASIS,  
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
See the License for the specific language governing permissions and  
limitations under the License.
