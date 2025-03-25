:robot: I have created a release *beep* *boop*
---


<details><summary>accesskit: 0.8.1</summary>

## [0.8.1](https://github.com/forksnd/accesskit/compare/accesskit-v0.18.0...accesskit-v0.8.1) (2025-03-25)


###   BREAKING CHANGES

* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Drop the `is_hovered` property ([#479](https://github.com/forksnd/accesskit/issues/479))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Optimize serialization and make it compatible with more data formats ([#437](https://github.com/forksnd/accesskit/issues/437))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393))
* Drop `SortDirection::Unsorted` ([#391](https://github.com/forksnd/accesskit/issues/391))
* Rename `hierarchical_level` to `level` ([#390](https://github.com/forksnd/accesskit/issues/390))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296))
* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289))
* Drop next/previous focus properties ([#288](https://github.com/forksnd/accesskit/issues/288))
* Drop `Tree::root_scroller` ([#279](https://github.com/forksnd/accesskit/issues/279))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add C bindings ([#230](https://github.com/forksnd/accesskit/issues/230)) ([7f7f4c7](https://github.com/forksnd/accesskit/commit/7f7f4c755890ab8210a5a8bf8e237ba6a51dd205))
* Add role for terminals ([#282](https://github.com/forksnd/accesskit/issues/282)) ([ddbef37](https://github.com/forksnd/accesskit/commit/ddbef37158b57f56217317b480e40d58f83a9c24))
* Add the `owns` relation ([#392](https://github.com/forksnd/accesskit/issues/392)) ([fd668dd](https://github.com/forksnd/accesskit/commit/fd668ddc4b64cb05ab3600972b3d3823a037f2d5))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291)) ([5313860](https://github.com/forksnd/accesskit/commit/531386023257150f49b5e4be942f359855fb7cb6))
* Android adapter ([#500](https://github.com/forksnd/accesskit/issues/500)) ([7e65ac7](https://github.com/forksnd/accesskit/commit/7e65ac77d7e108ac5b9f3722f488a2fdf2e3b3e0))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))


### Bug Fixes

* Add explicit cargo features for `enumn` and `pyo3` ([#425](https://github.com/forksnd/accesskit/issues/425)) ([71ad45b](https://github.com/forksnd/accesskit/commit/71ad45be1651409ee6918cf835b656e6b5e0fe2d))
* Add missing semicolons when not returning anything ([#303](https://github.com/forksnd/accesskit/issues/303)) ([38d4de1](https://github.com/forksnd/accesskit/commit/38d4de1442247e701047d75122a9638a2ed99b1f))
* Bump pyo3; add `rename_all` attribute to enums ([#330](https://github.com/forksnd/accesskit/issues/330)) ([5a4c6f3](https://github.com/forksnd/accesskit/commit/5a4c6f399837d67b066451a8fb4d43d03c8acb8b))
* Derive `PartialOrd` and `Ord` on `NodeId` ([#363](https://github.com/forksnd/accesskit/issues/363)) ([ce3bba1](https://github.com/forksnd/accesskit/commit/ce3bba1e043d650c406d8814b4f33e9104199c8b))
* Document the `role_description` node property ([#331](https://github.com/forksnd/accesskit/issues/331)) ([936fa2c](https://github.com/forksnd/accesskit/commit/936fa2c23190c5d7cd4eb880612295785a009721))
* Don't use a macro to generate Action debug helper function ([#459](https://github.com/forksnd/accesskit/issues/459)) ([ed1fb73](https://github.com/forksnd/accesskit/commit/ed1fb7370780c9dd15028cdfd13e2065642bf490))
* Drop `Tree::root_scroller` ([#279](https://github.com/forksnd/accesskit/issues/279)) ([fc6c4e0](https://github.com/forksnd/accesskit/commit/fc6c4e0091d5b257a3869a468fca144a1453cebc))
* Drop next/previous focus properties ([#288](https://github.com/forksnd/accesskit/issues/288)) ([d35c7c1](https://github.com/forksnd/accesskit/commit/d35c7c149a650dfedf1b031c0668adad585659fa))
* Drop the `is_hovered` property ([#479](https://github.com/forksnd/accesskit/issues/479)) ([95dfdb6](https://github.com/forksnd/accesskit/commit/95dfdb6c88f7d705f6a7283cb8524168a9f542b2))
* Eliminate duplicate definitions ([#461](https://github.com/forksnd/accesskit/issues/461)) ([59826d4](https://github.com/forksnd/accesskit/commit/59826d4500ddfe880181f7087f9fe83ff2209fc4))
* Fix broken intra-doc-link. ([#262](https://github.com/forksnd/accesskit/issues/262)) ([63c1715](https://github.com/forksnd/accesskit/commit/63c17152d1eb8ae6ff19c2bc4a6756372bc490c2))
* Fix some broken links in the documentation ([#484](https://github.com/forksnd/accesskit/issues/484)) ([0a51225](https://github.com/forksnd/accesskit/commit/0a5122561c6f6aca5cf802464220056d763040f8))
* Improve debug representation of `Node` and `NodeBuilder` ([#452](https://github.com/forksnd/accesskit/issues/452)) ([119aa1d](https://github.com/forksnd/accesskit/commit/119aa1dca8fe734112ecbd59568c876b336ccb6c))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Make `NodeClassSet::new` const ([#368](https://github.com/forksnd/accesskit/issues/368)) ([11d2968](https://github.com/forksnd/accesskit/commit/11d2968464d50c3e3f55e9a872d0d454c19e7e51))
* Set appropriate representations on all public types that will be exposed via FFI ([54e82f6](https://github.com/forksnd/accesskit/commit/54e82f673f5c7b46d9077fe5f946305800862bf0))
* Support the enumn crate in all public enums ([#264](https://github.com/forksnd/accesskit/issues/264)) ([b9b3cd1](https://github.com/forksnd/accesskit/commit/b9b3cd18fccdd6526fb4f58c13eb91599452a3d6))
* Support the pyo3 crate in all public enums ([#270](https://github.com/forksnd/accesskit/issues/270)) ([9b12d0c](https://github.com/forksnd/accesskit/commit/9b12d0c3d828d4c847510b611d891872c4666984))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update pyo3 to 0.23 ([#512](https://github.com/forksnd/accesskit/issues/512)) ([93d3a27](https://github.com/forksnd/accesskit/commit/93d3a27ac4af60eef4a1faf26392a6f7ff69cf81))


### Documentation

* Fix outdated documentation for `TreeUpdate` ([#182](https://github.com/forksnd/accesskit/issues/182)) ([dd658c7](https://github.com/forksnd/accesskit/commit/dd658c70df55b2234a0346220362b0b9a40bb41d))


### Code Refactoring

* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289)) ([4fc9c55](https://github.com/forksnd/accesskit/commit/4fc9c55c91812472593923d93ff89d75ff305ee4))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393)) ([e34dad9](https://github.com/forksnd/accesskit/commit/e34dad94448a5321ece9def3f2e054aa5f62dd79))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389)) ([1b153ed](https://github.com/forksnd/accesskit/commit/1b153ed51f8421cdba2dc98beca2e8f5f8c781bc))
* Drop `SortDirection::Unsorted` ([#391](https://github.com/forksnd/accesskit/issues/391)) ([b86f484](https://github.com/forksnd/accesskit/commit/b86f484b7e6645e63362896b744a71ec758f810d))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296)) ([4fc7846](https://github.com/forksnd/accesskit/commit/4fc7846d732d61fb45c023060ebab96801a0053e))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Optimize serialization and make it compatible with more data formats ([#437](https://github.com/forksnd/accesskit/issues/437)) ([5a80d3a](https://github.com/forksnd/accesskit/commit/5a80d3ae46cfe85780d4900f4fa9f4feaba52053))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388)) ([6bc040b](https://github.com/forksnd/accesskit/commit/6bc040b7cf75cdbd6a019cc380d8dbce804b3c81))
* Rename `hierarchical_level` to `level` ([#390](https://github.com/forksnd/accesskit/issues/390)) ([2d61e01](https://github.com/forksnd/accesskit/commit/2d61e01fffff1265b348c141715f6f9b6fe4081b))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476)) ([7d8910e](https://github.com/forksnd/accesskit/commit/7d8910e35f7bc0543724cc124941a3bd0304bcc0))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473)) ([29fa341](https://github.com/forksnd/accesskit/commit/29fa34125a811bd3a0f9da579a9f35c9da90bf29))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))
</details>

<details><summary>accesskit_android: 0.2.0</summary>

## [0.2.0](https://github.com/forksnd/accesskit/compare/accesskit_android-v0.1.1...accesskit_android-v0.2.0) (2025-03-25)


### Features

* Android adapter ([#500](https://github.com/forksnd/accesskit/issues/500)) ([7e65ac7](https://github.com/forksnd/accesskit/commit/7e65ac77d7e108ac5b9f3722f488a2fdf2e3b3e0))


### Bug Fixes

* Eliminate the dependency on `paste` ([#528](https://github.com/forksnd/accesskit/issues/528)) ([4aef05d](https://github.com/forksnd/accesskit/commit/4aef05d0b34b434c0f0ce2e7583adef3e73bda4d))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_consumer bumped from 0.27.0 to 0.28.0
</details>

<details><summary>accesskit_atspi_common: 0.12.0</summary>

## [0.12.0](https://github.com/forksnd/accesskit/compare/accesskit_atspi_common-v0.11.0...accesskit_atspi_common-v0.12.0) (2025-03-25)


###   BREAKING CHANGES

* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add basic text support on Unix ([#362](https://github.com/forksnd/accesskit/issues/362)) ([52540f8](https://github.com/forksnd/accesskit/commit/52540f82cf9fc148358351ed486bab3e7e91f1d6))
* Add list box support to the `consumer` and `atspi-common` crates ([d6dca15](https://github.com/forksnd/accesskit/commit/d6dca15d5c298c797ab7a702f0186043eac33c5c))
* Expose root node ID in `accesskit_atspi_common::Adapter` ([#370](https://github.com/forksnd/accesskit/issues/370)) ([a43b497](https://github.com/forksnd/accesskit/commit/a43b497afbbbcf90e9d15259635a329164d6a791))
* Expose the `is_required` property ([#497](https://github.com/forksnd/accesskit/issues/497)) ([46ed99b](https://github.com/forksnd/accesskit/commit/46ed99bb958ddb32cbf1bee2fcfb7b328bcbe0ab))
* Expose the `orientation` property ([#421](https://github.com/forksnd/accesskit/issues/421)) ([590aada](https://github.com/forksnd/accesskit/commit/590aada070dc812f9b8f171fb9e43ac984fad2a1))
* Expose the `placeholder` property ([#417](https://github.com/forksnd/accesskit/issues/417)) ([8f4a0a1](https://github.com/forksnd/accesskit/commit/8f4a0a1c10f83fcc8580a37d8013fec2d110865b))
* Factor out core AT-SPI translation layer ([#352](https://github.com/forksnd/accesskit/issues/352)) ([8c0ab58](https://github.com/forksnd/accesskit/commit/8c0ab58d441c0d4484e0bc31a554bdfb3f088cd6))
* Feature-gate the `accesskit_atspi_common::simplified` module ([#430](https://github.com/forksnd/accesskit/issues/430)) ([50341f1](https://github.com/forksnd/accesskit/commit/50341f10cf32ef16c904d54725f717a585d21043))
* Implement the `description` property ([#382](https://github.com/forksnd/accesskit/issues/382)) ([d49f406](https://github.com/forksnd/accesskit/commit/d49f40660b5dc23ed074cd72a91e511b130756ae))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))


### Bug Fixes

* Add missing README ([#357](https://github.com/forksnd/accesskit/issues/357)) ([e8cf48e](https://github.com/forksnd/accesskit/commit/e8cf48e21be0146768b2d14289164d192823fd1f))
* Avoid unnecessary repeated checks for text changes ([#432](https://github.com/forksnd/accesskit/issues/432)) ([0e89671](https://github.com/forksnd/accesskit/commit/0e89671fc0cf831d2c86a2cacf0195e247560753))
* Correctly handle recursive filtering ([#438](https://github.com/forksnd/accesskit/issues/438)) ([72f9b42](https://github.com/forksnd/accesskit/commit/72f9b424a5c6e7914df8bf31eeb2fc61be35f47b))
* Derive `Debug` for adapters ([#513](https://github.com/forksnd/accesskit/issues/513)) ([753d904](https://github.com/forksnd/accesskit/commit/753d90473cf57682568c7a17c82474c8e5d00b25))
* Don't fire events for filtered children on Unix ([#414](https://github.com/forksnd/accesskit/issues/414)) ([2bcb1b6](https://github.com/forksnd/accesskit/commit/2bcb1b63e88b801b194a4db50059fa063efbee64))
* Fix a compilation error in atspi-common `Event::new` ([#537](https://github.com/forksnd/accesskit/issues/537)) ([23b4d8d](https://github.com/forksnd/accesskit/commit/23b4d8d49fed378899855a40e63aff10e829f6e8))
* Fix a logic error in suffix calculation for text changes ([#423](https://github.com/forksnd/accesskit/issues/423)) ([1121723](https://github.com/forksnd/accesskit/commit/1121723983cb2fa64b5053626ec64afb851ff6c4))
* Fix platform adapters to support copy-on-write tree snapshots again ([#411](https://github.com/forksnd/accesskit/issues/411)) ([d3a130a](https://github.com/forksnd/accesskit/commit/d3a130a5ec8ae1d9edf0bf85a44f35f0e365242c))
* Improve how coordinates are computed on Unix ([#420](https://github.com/forksnd/accesskit/issues/420)) ([fc5125e](https://github.com/forksnd/accesskit/commit/fc5125e27f8f4f655e1de5049d0d53536284d9a0))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Remove unnecessary explicit lifetimes ([#488](https://github.com/forksnd/accesskit/issues/488)) ([d2bcd6d](https://github.com/forksnd/accesskit/commit/d2bcd6d3048d23df4e132bee6171eb247b2dc2c8))
* Return to handling focus events directly, after generic node changes ([#409](https://github.com/forksnd/accesskit/issues/409)) ([cd2e35e](https://github.com/forksnd/accesskit/commit/cd2e35e43817405199ae6acd64ef90aee445be0b))
* Smarter calculation of AT-SPI extents for the window ([#435](https://github.com/forksnd/accesskit/issues/435)) ([7f40fbc](https://github.com/forksnd/accesskit/commit/7f40fbc811f863e99088cd7eb725994d0f79263f))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update to zbus v4 ([#456](https://github.com/forksnd/accesskit/issues/456)) ([95db8f1](https://github.com/forksnd/accesskit/commit/95db8f1c5f7f56598eab6910a990ccbf9d864dda))
* Update zbus to 5.0 ([#519](https://github.com/forksnd/accesskit/issues/519)) ([4c10b80](https://github.com/forksnd/accesskit/commit/4c10b801b6924c7010b83f4eb44c8c350c860cf6))


### Code Refactoring

* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393)) ([e34dad9](https://github.com/forksnd/accesskit/commit/e34dad94448a5321ece9def3f2e054aa5f62dd79))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493)) ([484fd7c](https://github.com/forksnd/accesskit/commit/484fd7cbfb778222369d3f57d31dd998f6fa80d8))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388)) ([6bc040b](https://github.com/forksnd/accesskit/commit/6bc040b7cf75cdbd6a019cc380d8dbce804b3c81))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473)) ([29fa341](https://github.com/forksnd/accesskit/commit/29fa34125a811bd3a0f9da579a9f35c9da90bf29))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_consumer bumped from 0.27.0 to 0.28.0
</details>

<details><summary>accesskit_consumer: 0.28.0</summary>

## [0.28.0](https://github.com/forksnd/accesskit/compare/accesskit_consumer-v0.27.0...accesskit_consumer-v0.28.0) (2025-03-25)


###   BREAKING CHANGES

* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Restore full copy-on-write tree snapshots, now using `immutable-chunkmap` ([#365](https://github.com/forksnd/accesskit/issues/365))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291))
* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289))
* Drop `Tree::root_scroller` ([#279](https://github.com/forksnd/accesskit/issues/279))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add basic text support on Unix ([#362](https://github.com/forksnd/accesskit/issues/362)) ([52540f8](https://github.com/forksnd/accesskit/commit/52540f82cf9fc148358351ed486bab3e7e91f1d6))
* Add list box support to the `consumer` and `atspi-common` crates ([d6dca15](https://github.com/forksnd/accesskit/commit/d6dca15d5c298c797ab7a702f0186043eac33c5c))
* Add role for terminals ([#282](https://github.com/forksnd/accesskit/issues/282)) ([ddbef37](https://github.com/forksnd/accesskit/commit/ddbef37158b57f56217317b480e40d58f83a9c24))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291)) ([5313860](https://github.com/forksnd/accesskit/commit/531386023257150f49b5e4be942f359855fb7cb6))
* Android adapter ([#500](https://github.com/forksnd/accesskit/issues/500)) ([7e65ac7](https://github.com/forksnd/accesskit/commit/7e65ac77d7e108ac5b9f3722f488a2fdf2e3b3e0))
* Automatically get button and link labels from descendants ([#184](https://github.com/forksnd/accesskit/issues/184)) ([ec5c38e](https://github.com/forksnd/accesskit/commit/ec5c38ef3001a10b7a135df1438901246463f3e1))
* Basic Unix platform adapter ([#198](https://github.com/forksnd/accesskit/issues/198)) ([1cea32e](https://github.com/forksnd/accesskit/commit/1cea32e44ee743b778ac941ceff9087ae745cb37))
* Expose the `is_required` property ([#497](https://github.com/forksnd/accesskit/issues/497)) ([46ed99b](https://github.com/forksnd/accesskit/commit/46ed99bb958ddb32cbf1bee2fcfb7b328bcbe0ab))
* Expose the `orientation` property ([#421](https://github.com/forksnd/accesskit/issues/421)) ([590aada](https://github.com/forksnd/accesskit/commit/590aada070dc812f9b8f171fb9e43ac984fad2a1))
* Expose the `placeholder` property ([#417](https://github.com/forksnd/accesskit/issues/417)) ([8f4a0a1](https://github.com/forksnd/accesskit/commit/8f4a0a1c10f83fcc8580a37d8013fec2d110865b))
* Expose the class name property ([#385](https://github.com/forksnd/accesskit/issues/385)) ([53dcf2a](https://github.com/forksnd/accesskit/commit/53dcf2ae47546273590c46a9b31b708aa1409837))
* Implement the `description` property ([#382](https://github.com/forksnd/accesskit/issues/382)) ([d49f406](https://github.com/forksnd/accesskit/commit/d49f40660b5dc23ed074cd72a91e511b130756ae))
* Make the consumer crate no-std ([#471](https://github.com/forksnd/accesskit/issues/471)) ([f25d03a](https://github.com/forksnd/accesskit/commit/f25d03ad81736017a29ce0f5ed1b387047534d2d))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))
* Support custom role descriptions ([#316](https://github.com/forksnd/accesskit/issues/316)) ([c8d1a56](https://github.com/forksnd/accesskit/commit/c8d1a5638fa6c33adfa059815c04f7e043c56026))
* Text support on macOS ([#191](https://github.com/forksnd/accesskit/issues/191)) ([3a35dbe](https://github.com/forksnd/accesskit/commit/3a35dbe02122c789fe682995c5b7e022aef5cc36))


### Bug Fixes

* `Node::is_focusable` always returns true if the node is focused ([#451](https://github.com/forksnd/accesskit/issues/451)) ([d286883](https://github.com/forksnd/accesskit/commit/d286883d88b5c1e51f6e8bbfbc2e0e5b1986d9b5))
* Add missing semicolons when not returning anything ([#303](https://github.com/forksnd/accesskit/issues/303)) ([38d4de1](https://github.com/forksnd/accesskit/commit/38d4de1442247e701047d75122a9638a2ed99b1f))
* Avoid reallocations when processing tree updates ([#482](https://github.com/forksnd/accesskit/issues/482)) ([dcb17bc](https://github.com/forksnd/accesskit/commit/dcb17bc1e69eccc2fea6af6a6b61f71c9e73a0b9))
* Clamp character index when getting focus from a text selection ([#428](https://github.com/forksnd/accesskit/issues/428)) ([38e649d](https://github.com/forksnd/accesskit/commit/38e649de6b72c99d1e438b26b3fc1f647ac39e6c))
* Clamp character indices when converting a text selection to a range ([#416](https://github.com/forksnd/accesskit/issues/416)) ([5c550af](https://github.com/forksnd/accesskit/commit/5c550af7afc81b3a32c30d31327ff95b93718545))
* Correctly handle recursive filtering ([#438](https://github.com/forksnd/accesskit/issues/438)) ([72f9b42](https://github.com/forksnd/accesskit/commit/72f9b424a5c6e7914df8bf31eeb2fc61be35f47b))
* Derive `Debug` for adapters ([#513](https://github.com/forksnd/accesskit/issues/513)) ([753d904](https://github.com/forksnd/accesskit/commit/753d90473cf57682568c7a17c82474c8e5d00b25))
* Drop `Tree::root_scroller` ([#279](https://github.com/forksnd/accesskit/issues/279)) ([fc6c4e0](https://github.com/forksnd/accesskit/commit/fc6c4e0091d5b257a3869a468fca144a1453cebc))
* Extend the implicit labelled-by relation to more parent roles ([#448](https://github.com/forksnd/accesskit/issues/448)) ([df518c7](https://github.com/forksnd/accesskit/commit/df518c71934cb4e0071764643968e67f9908a8dd))
* Fix a logic error that sometimes caused filtered traversal to stop prematurely ([#412](https://github.com/forksnd/accesskit/issues/412)) ([9946d38](https://github.com/forksnd/accesskit/commit/9946d38b9d13489517713f43284cf6b96d88cb8c))
* Fix the filtered sibling iterators to use the filtered parent to find the back node ([#408](https://github.com/forksnd/accesskit/issues/408)) ([2f8155c](https://github.com/forksnd/accesskit/commit/2f8155ca260d7e50de5de502744b420769875e83))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234)) ([773389b](https://github.com/forksnd/accesskit/commit/773389bff857fa18edf15de426e029251fc34591))
* Go back to detecting unchanged nodes when processing tree updates ([#415](https://github.com/forksnd/accesskit/issues/415)) ([489302d](https://github.com/forksnd/accesskit/commit/489302db7143a016605145682b989ab18583d59c))
* Improve panic messages ([#401](https://github.com/forksnd/accesskit/issues/401)) ([e6ce021](https://github.com/forksnd/accesskit/commit/e6ce021b3b172f5ea7ee31496c9afaf66b1871f2))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Make `Node::filtered_parent` recursive as it was meant to be ([#203](https://github.com/forksnd/accesskit/issues/203)) ([d2faef5](https://github.com/forksnd/accesskit/commit/d2faef5a2ad61b9e4d3f3d5c89570cdeec6fe6e6))
* More reliable handling of the edge case for wrapped lines ([#192](https://github.com/forksnd/accesskit/issues/192)) ([c626d2c](https://github.com/forksnd/accesskit/commit/c626d2c3028085b076ada7dd31242cf3ca3c0f08))
* Optimize dynamic string building ([#491](https://github.com/forksnd/accesskit/issues/491)) ([a86901d](https://github.com/forksnd/accesskit/commit/a86901ddea5d5ba72ab237e98b53d6adcc6087bb))
* Optimize removal of unreachable nodes ([#486](https://github.com/forksnd/accesskit/issues/486)) ([93d0a72](https://github.com/forksnd/accesskit/commit/93d0a72880901479fe44ed92ef24fa71b7bb4803))
* Optimize the "short node list" helper used in panic messages ([#490](https://github.com/forksnd/accesskit/issues/490)) ([b4a89a3](https://github.com/forksnd/accesskit/commit/b4a89a386474b9a71f22aa36d09c2d07bca084cd))
* Remove unnecessary explicit lifetimes ([#488](https://github.com/forksnd/accesskit/issues/488)) ([d2bcd6d](https://github.com/forksnd/accesskit/commit/d2bcd6d3048d23df4e132bee6171eb247b2dc2c8))
* Support text fields without a value property ([#274](https://github.com/forksnd/accesskit/issues/274)) ([5ae557b](https://github.com/forksnd/accesskit/commit/5ae557b40d395b4a9966a90a2d80e7d97ad50bf9))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update minimum version of immutable-chunkmap ([#419](https://github.com/forksnd/accesskit/issues/419)) ([893f688](https://github.com/forksnd/accesskit/commit/893f68845dd322da5f3ae4d39fc2b1cc01f88888))
* Use common filters across platform adapters ([#287](https://github.com/forksnd/accesskit/issues/287)) ([09c1204](https://github.com/forksnd/accesskit/commit/09c12045ff4ccdb22f0cf643077a27465013572d))


### Code Refactoring

* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289)) ([4fc9c55](https://github.com/forksnd/accesskit/commit/4fc9c55c91812472593923d93ff89d75ff305ee4))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389)) ([1b153ed](https://github.com/forksnd/accesskit/commit/1b153ed51f8421cdba2dc98beca2e8f5f8c781bc))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493)) ([484fd7c](https://github.com/forksnd/accesskit/commit/484fd7cbfb778222369d3f57d31dd998f6fa80d8))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388)) ([6bc040b](https://github.com/forksnd/accesskit/commit/6bc040b7cf75cdbd6a019cc380d8dbce804b3c81))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476)) ([7d8910e](https://github.com/forksnd/accesskit/commit/7d8910e35f7bc0543724cc124941a3bd0304bcc0))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473)) ([29fa341](https://github.com/forksnd/accesskit/commit/29fa34125a811bd3a0f9da579a9f35c9da90bf29))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Restore full copy-on-write tree snapshots, now using `immutable-chunkmap` ([#365](https://github.com/forksnd/accesskit/issues/365)) ([441bf5f](https://github.com/forksnd/accesskit/commit/441bf5ff77d1785dfea228de9109aceff4773da1))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
</details>

<details><summary>accesskit_macos: 0.20.0</summary>

## [0.20.0](https://github.com/forksnd/accesskit/compare/accesskit_macos-v0.19.0...accesskit_macos-v0.20.0) (2025-03-25)


###   BREAKING CHANGES

* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296))
* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add role for terminals ([#282](https://github.com/forksnd/accesskit/issues/282)) ([ddbef37](https://github.com/forksnd/accesskit/commit/ddbef37158b57f56217317b480e40d58f83a9c24))
* Add window-based constructor to macOS subclassing adapter ([#253](https://github.com/forksnd/accesskit/issues/253)) ([022ef04](https://github.com/forksnd/accesskit/commit/022ef045b9f28262b738ee1ca29a4c7303061fb3))
* Expose the `is_required` property ([#497](https://github.com/forksnd/accesskit/issues/497)) ([46ed99b](https://github.com/forksnd/accesskit/commit/46ed99bb958ddb32cbf1bee2fcfb7b328bcbe0ab))
* Expose the `orientation` property ([#421](https://github.com/forksnd/accesskit/issues/421)) ([590aada](https://github.com/forksnd/accesskit/commit/590aada070dc812f9b8f171fb9e43ac984fad2a1))
* Expose the `placeholder` property ([#417](https://github.com/forksnd/accesskit/issues/417)) ([8f4a0a1](https://github.com/forksnd/accesskit/commit/8f4a0a1c10f83fcc8580a37d8013fec2d110865b))
* Implement the `description` property ([#382](https://github.com/forksnd/accesskit/issues/382)) ([d49f406](https://github.com/forksnd/accesskit/commit/d49f40660b5dc23ed074cd72a91e511b130756ae))
* Live regions on macOS ([#196](https://github.com/forksnd/accesskit/issues/196)) ([47d8d9f](https://github.com/forksnd/accesskit/commit/47d8d9f6a567dfe909aa4065886cace07084efb7))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))
* Support custom role descriptions ([#316](https://github.com/forksnd/accesskit/issues/316)) ([c8d1a56](https://github.com/forksnd/accesskit/commit/c8d1a5638fa6c33adfa059815c04f7e043c56026))
* Text support on macOS ([#191](https://github.com/forksnd/accesskit/issues/191)) ([3a35dbe](https://github.com/forksnd/accesskit/commit/3a35dbe02122c789fe682995c5b7e022aef5cc36))
* Workaround for libraries that put the macOS keyboard focus on the window rather than the content view ([#266](https://github.com/forksnd/accesskit/issues/266)) ([c2db1b0](https://github.com/forksnd/accesskit/commit/c2db1b0424e905d87691f8148f28b77405f29926))


### Bug Fixes

* Add list box support to the platform adapters ([6c622cf](https://github.com/forksnd/accesskit/commit/6c622cff4c0c989d9a5f16b775adff9cdacf534c))
* Add properties needed by the Xcode Accessibility Inspector ([#466](https://github.com/forksnd/accesskit/issues/466)) ([295b188](https://github.com/forksnd/accesskit/commit/295b1881936dd097d82a10317ff14d1369f7e4bd))
* Add sub roles to MacOS adapter ([#480](https://github.com/forksnd/accesskit/issues/480)) ([40ad828](https://github.com/forksnd/accesskit/commit/40ad828a8f95c94f3079310d95c94ab7b16e0887))
* Bump objc2 to 0.5.0; bring icrate 0.1.0 ([#323](https://github.com/forksnd/accesskit/issues/323)) ([23b3f2f](https://github.com/forksnd/accesskit/commit/23b3f2f93b9452c80374d1da3e9abeaec60ba9bf))
* Correctly apply the DPI scale factor to coordinates ([#185](https://github.com/forksnd/accesskit/issues/185)) ([d263938](https://github.com/forksnd/accesskit/commit/d263938d68bb63567853a340d3466ff27e076d87))
* Derive `Debug` for adapters ([#513](https://github.com/forksnd/accesskit/issues/513)) ([753d904](https://github.com/forksnd/accesskit/commit/753d90473cf57682568c7a17c82474c8e5d00b25))
* Don't expose the window title in our root element on macOS ([#187](https://github.com/forksnd/accesskit/issues/187)) ([9739b74](https://github.com/forksnd/accesskit/commit/9739b7424328da45c1c43b6db49af142a8789aa5))
* Expose static text as the value rather than the title on macOS ([#186](https://github.com/forksnd/accesskit/issues/186)) ([e3720c8](https://github.com/forksnd/accesskit/commit/e3720c8e2d7c5e8c8601c52ad620dcfcacebc570))
* Expose which accessibility selectors are actually allowed for a particular node ([#181](https://github.com/forksnd/accesskit/issues/181)) ([c4cbb23](https://github.com/forksnd/accesskit/commit/c4cbb23156749d513df4e520dcb9be0a74c697d3))
* Fix macOS leaks ([e8537fc](https://github.com/forksnd/accesskit/commit/e8537fcbdf4a68f39c9bc51cf9fe6960903e26f2))
* Fix new compiler warning in Rust 1.77 ([#376](https://github.com/forksnd/accesskit/issues/376)) ([1de7c63](https://github.com/forksnd/accesskit/commit/1de7c63e7db12bc7eda57a191e913fef0e572f43))
* Fix platform adapters to support copy-on-write tree snapshots again ([#411](https://github.com/forksnd/accesskit/issues/411)) ([d3a130a](https://github.com/forksnd/accesskit/commit/d3a130a5ec8ae1d9edf0bf85a44f35f0e365242c))
* Fix problems related to the root node ([#231](https://github.com/forksnd/accesskit/issues/231)) ([7228494](https://github.com/forksnd/accesskit/commit/7228494361c4f131af6a7fc2af8a98406cd9a63e))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234)) ([773389b](https://github.com/forksnd/accesskit/commit/773389bff857fa18edf15de426e029251fc34591))
* Handle views with flipped coordinates ([#174](https://github.com/forksnd/accesskit/issues/174)) ([d14484c](https://github.com/forksnd/accesskit/commit/d14484cdcfdd99a497354aa3e012a0e130cc3d64))
* Implement the `isAccessibilityEnabled` property on MacOS ([#474](https://github.com/forksnd/accesskit/issues/474)) ([61e4817](https://github.com/forksnd/accesskit/commit/61e48174ed1dd57b7dd919ecaef908f157357ec0))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Make VoiceOver move through nodes in logical order ([#176](https://github.com/forksnd/accesskit/issues/176)) ([f060be4](https://github.com/forksnd/accesskit/commit/f060be409945296ed100cd63ecb3d2bb6bbad89e))
* More reliable handling of the edge case for wrapped lines ([#192](https://github.com/forksnd/accesskit/issues/192)) ([c626d2c](https://github.com/forksnd/accesskit/commit/c626d2c3028085b076ada7dd31242cf3ca3c0f08))
* Optimize use of hash tables in platform adapters ([#485](https://github.com/forksnd/accesskit/issues/485)) ([f4f0bfb](https://github.com/forksnd/accesskit/commit/f4f0bfbf21b8e22e80ab07deb432f9e7e16469ab))
* Pin objc2 dependency to 0.3.0-beta.3 ([#201](https://github.com/forksnd/accesskit/issues/201)) ([0adfed1](https://github.com/forksnd/accesskit/commit/0adfed1192ee255fba34ad82e8483ab9296ac2df))
* Re-export types from objc2 ([#172](https://github.com/forksnd/accesskit/issues/172)) ([1ac67ad](https://github.com/forksnd/accesskit/commit/1ac67ad17587d79b5338cb71e2bc07612fc10c44))
* Remove unnecessary explicit lifetimes ([#488](https://github.com/forksnd/accesskit/issues/488)) ([d2bcd6d](https://github.com/forksnd/accesskit/commit/d2bcd6d3048d23df4e132bee6171eb247b2dc2c8))
* Set proper target to build accesskit_macos documentation ([#226](https://github.com/forksnd/accesskit/issues/226)) ([9cd6bb1](https://github.com/forksnd/accesskit/commit/9cd6bb14d60bf85027b330a51afe912c37723902))
* Support text fields without a value property ([#274](https://github.com/forksnd/accesskit/issues/274)) ([5ae557b](https://github.com/forksnd/accesskit/commit/5ae557b40d395b4a9966a90a2d80e7d97ad50bf9))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Use common filters across platform adapters ([#287](https://github.com/forksnd/accesskit/issues/287)) ([09c1204](https://github.com/forksnd/accesskit/commit/09c12045ff4ccdb22f0cf643077a27465013572d))
* Use new objc2 crates ([#384](https://github.com/forksnd/accesskit/issues/384)) ([b3484c0](https://github.com/forksnd/accesskit/commit/b3484c0fb1fef3ecd41ff9592978336c20b8b4f8))


### Code Refactoring

* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289)) ([4fc9c55](https://github.com/forksnd/accesskit/commit/4fc9c55c91812472593923d93ff89d75ff305ee4))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393)) ([e34dad9](https://github.com/forksnd/accesskit/commit/e34dad94448a5321ece9def3f2e054aa5f62dd79))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389)) ([1b153ed](https://github.com/forksnd/accesskit/commit/1b153ed51f8421cdba2dc98beca2e8f5f8c781bc))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296)) ([4fc7846](https://github.com/forksnd/accesskit/commit/4fc7846d732d61fb45c023060ebab96801a0053e))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179)) ([f35c941](https://github.com/forksnd/accesskit/commit/f35c941f395f3162db376a69cfaaaf770d376267))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493)) ([484fd7c](https://github.com/forksnd/accesskit/commit/484fd7cbfb778222369d3f57d31dd998f6fa80d8))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388)) ([6bc040b](https://github.com/forksnd/accesskit/commit/6bc040b7cf75cdbd6a019cc380d8dbce804b3c81))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476)) ([7d8910e](https://github.com/forksnd/accesskit/commit/7d8910e35f7bc0543724cc124941a3bd0304bcc0))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473)) ([29fa341](https://github.com/forksnd/accesskit/commit/29fa34125a811bd3a0f9da579a9f35c9da90bf29))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_consumer bumped from 0.27.0 to 0.28.0
</details>

<details><summary>accesskit_unix: 0.15.0</summary>

## [0.15.0](https://github.com/forksnd/accesskit/compare/accesskit_unix-v0.14.0...accesskit_unix-v0.15.0) (2025-03-25)


###   BREAKING CHANGES

* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Force a semver-breaking release ([#398](https://github.com/forksnd/accesskit/issues/398))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Lazily activate Unix adapters ([#324](https://github.com/forksnd/accesskit/issues/324))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296))
* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add basic text support on Unix ([#362](https://github.com/forksnd/accesskit/issues/362)) ([52540f8](https://github.com/forksnd/accesskit/commit/52540f82cf9fc148358351ed486bab3e7e91f1d6))
* Add features for async runtimes on Unix ([#248](https://github.com/forksnd/accesskit/issues/248)) ([b56b4ea](https://github.com/forksnd/accesskit/commit/b56b4ea7c967ee5a1dae21a2fa0dcd385346031e))
* Add role for terminals ([#282](https://github.com/forksnd/accesskit/issues/282)) ([ddbef37](https://github.com/forksnd/accesskit/commit/ddbef37158b57f56217317b480e40d58f83a9c24))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291)) ([5313860](https://github.com/forksnd/accesskit/commit/531386023257150f49b5e4be942f359855fb7cb6))
* Basic Unix platform adapter ([#198](https://github.com/forksnd/accesskit/issues/198)) ([1cea32e](https://github.com/forksnd/accesskit/commit/1cea32e44ee743b778ac941ceff9087ae745cb37))
* Expose the `placeholder` property ([#417](https://github.com/forksnd/accesskit/issues/417)) ([8f4a0a1](https://github.com/forksnd/accesskit/commit/8f4a0a1c10f83fcc8580a37d8013fec2d110865b))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))
* Support custom role descriptions ([#316](https://github.com/forksnd/accesskit/issues/316)) ([c8d1a56](https://github.com/forksnd/accesskit/commit/c8d1a5638fa6c33adfa059815c04f7e043c56026))
* Support live regions on Unix ([#299](https://github.com/forksnd/accesskit/issues/299)) ([8d52a5f](https://github.com/forksnd/accesskit/commit/8d52a5fc4271a3b5edcc602b23fd7b920446eab0))
* Support multiple top-level windows on Unix ([#292](https://github.com/forksnd/accesskit/issues/292)) ([43ecf4b](https://github.com/forksnd/accesskit/commit/43ecf4b3ab96d9e8f7d2c2222c7e664c4f4f4abf))


### Bug Fixes

* Add list box support to the platform adapters ([6c622cf](https://github.com/forksnd/accesskit/commit/6c622cff4c0c989d9a5f16b775adff9cdacf534c))
* Bump async-channel dependency to `2.1.1` ([#321](https://github.com/forksnd/accesskit/issues/321)) ([99120b8](https://github.com/forksnd/accesskit/commit/99120b828d65306ab71d41f71979dc67e8b0bf6b))
* Derive `Debug` for adapters ([#513](https://github.com/forksnd/accesskit/issues/513)) ([753d904](https://github.com/forksnd/accesskit/commit/753d90473cf57682568c7a17c82474c8e5d00b25))
* Don't emit focus event twice on Unix ([#354](https://github.com/forksnd/accesskit/issues/354)) ([b39216c](https://github.com/forksnd/accesskit/commit/b39216cb31df692fef377f9b3c3c718fd225cc3c))
* Don't enable the `zbus/tokio` feature on Unix ([#521](https://github.com/forksnd/accesskit/issues/521)) ([9dfad97](https://github.com/forksnd/accesskit/commit/9dfad9796f71563a78bc6a7d5f01b111d80e63e6))
* Don't require tokio rt-multi-thread feature ([#290](https://github.com/forksnd/accesskit/issues/290)) ([cf61e47](https://github.com/forksnd/accesskit/commit/cf61e477adff26b032fa0b24502c0ae0a96c1987))
* Fix some clippy warnings ([#509](https://github.com/forksnd/accesskit/issues/509)) ([579b9c1](https://github.com/forksnd/accesskit/commit/579b9c12dd8abc44ecab41fa3c326a1d8999871d))
* Force a semver-breaking release ([#398](https://github.com/forksnd/accesskit/issues/398)) ([87b8b92](https://github.com/forksnd/accesskit/commit/87b8b92b74a102c7cae48e013d2c2ae1cc2f9598))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234)) ([773389b](https://github.com/forksnd/accesskit/commit/773389bff857fa18edf15de426e029251fc34591))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Lazily activate Unix adapters ([#324](https://github.com/forksnd/accesskit/issues/324)) ([54ed036](https://github.com/forksnd/accesskit/commit/54ed036c99d87428a8eb5bb03fd77e9e31562d4c))
* Make full use of tokio ecosystem if the tokio feature is enabled on Unix ([#336](https://github.com/forksnd/accesskit/issues/336)) ([c034802](https://github.com/forksnd/accesskit/commit/c0348024665a615a30fd8fe2f02e8c93cf9c6332))
* Return a null object for AT-SPI application's parent ([#454](https://github.com/forksnd/accesskit/issues/454)) ([8a84abf](https://github.com/forksnd/accesskit/commit/8a84abf81eaf22dd3672813ca36f1a422b5c0f1e))
* Run our own async executor on Unix ([#337](https://github.com/forksnd/accesskit/issues/337)) ([8f937ba](https://github.com/forksnd/accesskit/commit/8f937baaa510dd96da196501822b82f75f05b595))
* Update atspi dependency ([#217](https://github.com/forksnd/accesskit/issues/217)) ([93f2dc9](https://github.com/forksnd/accesskit/commit/93f2dc9bf0a57a8b7592c3a4cf4aa3885a3356f2))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update to zbus v4 ([#456](https://github.com/forksnd/accesskit/issues/456)) ([95db8f1](https://github.com/forksnd/accesskit/commit/95db8f1c5f7f56598eab6910a990ccbf9d864dda))
* Update zbus to 5.0 ([#519](https://github.com/forksnd/accesskit/issues/519)) ([4c10b80](https://github.com/forksnd/accesskit/commit/4c10b801b6924c7010b83f4eb44c8c350c860cf6))
* Use common filters across platform adapters ([#287](https://github.com/forksnd/accesskit/issues/287)) ([09c1204](https://github.com/forksnd/accesskit/commit/09c12045ff4ccdb22f0cf643077a27465013572d))
* Use the new accesskit_atspi_common crate in the Unix adapter ([#356](https://github.com/forksnd/accesskit/issues/356)) ([b2a468c](https://github.com/forksnd/accesskit/commit/b2a468ccb91ee4e6d3435e73eb00c65cbe75060a))


### Code Refactoring

* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289)) ([4fc9c55](https://github.com/forksnd/accesskit/commit/4fc9c55c91812472593923d93ff89d75ff305ee4))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296)) ([4fc7846](https://github.com/forksnd/accesskit/commit/4fc7846d732d61fb45c023060ebab96801a0053e))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_atspi_common bumped from 0.11.0 to 0.12.0
</details>

<details><summary>accesskit_windows: 0.27.0</summary>

## [0.27.0](https://github.com/forksnd/accesskit/compare/accesskit_windows-v0.26.0...accesskit_windows-v0.27.0) (2025-03-25)


###   BREAKING CHANGES

* Panic if the window is visible when the adapter is created, for adapters where this is a problem ([#529](https://github.com/forksnd/accesskit/issues/529))
* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Update windows to 0.58 on accesskit_windows ([#453](https://github.com/forksnd/accesskit/issues/453))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Update winit to 0.30 ([#397](https://github.com/forksnd/accesskit/issues/397))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296))
* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))
* Update winit to 0.28 ([#207](https://github.com/forksnd/accesskit/issues/207))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179))

### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add role for terminals ([#282](https://github.com/forksnd/accesskit/issues/282)) ([ddbef37](https://github.com/forksnd/accesskit/commit/ddbef37158b57f56217317b480e40d58f83a9c24))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291)) ([5313860](https://github.com/forksnd/accesskit/commit/531386023257150f49b5e4be942f359855fb7cb6))
* Expose the `is_required` property ([#497](https://github.com/forksnd/accesskit/issues/497)) ([46ed99b](https://github.com/forksnd/accesskit/commit/46ed99bb958ddb32cbf1bee2fcfb7b328bcbe0ab))
* Expose the `orientation` property ([#421](https://github.com/forksnd/accesskit/issues/421)) ([590aada](https://github.com/forksnd/accesskit/commit/590aada070dc812f9b8f171fb9e43ac984fad2a1))
* Expose the `placeholder` property ([#417](https://github.com/forksnd/accesskit/issues/417)) ([8f4a0a1](https://github.com/forksnd/accesskit/commit/8f4a0a1c10f83fcc8580a37d8013fec2d110865b))
* Expose the class name property ([#385](https://github.com/forksnd/accesskit/issues/385)) ([53dcf2a](https://github.com/forksnd/accesskit/commit/53dcf2ae47546273590c46a9b31b708aa1409837))
* Implement the `description` property ([#382](https://github.com/forksnd/accesskit/issues/382)) ([d49f406](https://github.com/forksnd/accesskit/commit/d49f40660b5dc23ed074cd72a91e511b130756ae))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))
* Support custom role descriptions ([#316](https://github.com/forksnd/accesskit/issues/316)) ([c8d1a56](https://github.com/forksnd/accesskit/commit/c8d1a5638fa6c33adfa059815c04f7e043c56026))


### Bug Fixes

* Add list box support to the platform adapters ([6c622cf](https://github.com/forksnd/accesskit/commit/6c622cff4c0c989d9a5f16b775adff9cdacf534c))
* Avoid `unnecessary_literal_unwrap` clippy lint ([#346](https://github.com/forksnd/accesskit/issues/346)) ([59a6eae](https://github.com/forksnd/accesskit/commit/59a6eae40ba35069b90d4cc0b765d838f8477c66))
* Bump windows-rs dependency to 0.52 ([#359](https://github.com/forksnd/accesskit/issues/359)) ([69d74f6](https://github.com/forksnd/accesskit/commit/69d74f6947922b76d4aee683eb53d8fbdd2259f2))
* Correct broken UIA method implementation that was incompatible with Windows 11 ATs ([#193](https://github.com/forksnd/accesskit/issues/193)) ([3c527c7](https://github.com/forksnd/accesskit/commit/3c527c76cb4139402d2b5550d2eb1ad12e07ebe5))
* Derive `Debug` for adapters ([#513](https://github.com/forksnd/accesskit/issues/513)) ([753d904](https://github.com/forksnd/accesskit/commit/753d90473cf57682568c7a17c82474c8e5d00b25))
* Eliminate the dependency on `paste` ([#528](https://github.com/forksnd/accesskit/issues/528)) ([4aef05d](https://github.com/forksnd/accesskit/commit/4aef05d0b34b434c0f0ce2e7583adef3e73bda4d))
* Expose password input fields on Windows ([#516](https://github.com/forksnd/accesskit/issues/516)) ([19514da](https://github.com/forksnd/accesskit/commit/19514dabc40bcfc01bee1b1efa77355ec5b0822b))
* Fix platform adapters to support copy-on-write tree snapshots again ([#411](https://github.com/forksnd/accesskit/issues/411)) ([d3a130a](https://github.com/forksnd/accesskit/commit/d3a130a5ec8ae1d9edf0bf85a44f35f0e365242c))
* Fix some clippy warnings ([#509](https://github.com/forksnd/accesskit/issues/509)) ([579b9c1](https://github.com/forksnd/accesskit/commit/579b9c12dd8abc44ecab41fa3c326a1d8999871d))
* Fix Windows 32-bit build errors ([#223](https://github.com/forksnd/accesskit/issues/223)) ([41f28b6](https://github.com/forksnd/accesskit/commit/41f28b670ac457b2d067bbc4ba40aa0fc8842e4d))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234)) ([773389b](https://github.com/forksnd/accesskit/commit/773389bff857fa18edf15de426e029251fc34591))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Make the test focus event handler thread-safe again ([#306](https://github.com/forksnd/accesskit/issues/306)) ([bb479c6](https://github.com/forksnd/accesskit/commit/bb479c69bddff77a1102549a7ff6ea5c7155d90d))
* Make the transition from placeholder to real tree more robust ([#405](https://github.com/forksnd/accesskit/issues/405)) ([928e11d](https://github.com/forksnd/accesskit/commit/928e11d00e7c60b3cafcc0ac623f6377b36f7ea7))
* Make the Windows subclassing test more robust ([#308](https://github.com/forksnd/accesskit/issues/308)) ([0078f79](https://github.com/forksnd/accesskit/commit/0078f7997f11a3bb1f3c33dc7a91f427b1a60db8))
* More reliable handling of the edge case for wrapped lines ([#192](https://github.com/forksnd/accesskit/issues/192)) ([c626d2c](https://github.com/forksnd/accesskit/commit/c626d2c3028085b076ada7dd31242cf3ca3c0f08))
* Optimize dynamic string building ([#491](https://github.com/forksnd/accesskit/issues/491)) ([a86901d](https://github.com/forksnd/accesskit/commit/a86901ddea5d5ba72ab237e98b53d6adcc6087bb))
* Optimize use of hash tables in platform adapters ([#485](https://github.com/forksnd/accesskit/issues/485)) ([f4f0bfb](https://github.com/forksnd/accesskit/commit/f4f0bfbf21b8e22e80ab07deb432f9e7e16469ab))
* Panic if the window is visible when the adapter is created, for adapters where this is a problem ([#529](https://github.com/forksnd/accesskit/issues/529)) ([c43c37b](https://github.com/forksnd/accesskit/commit/c43c37ba2502656fcae4fd726b9b7db0bb520f31))
* Provide fallback property implementations for the window root ([#194](https://github.com/forksnd/accesskit/issues/194)) ([f3d30b9](https://github.com/forksnd/accesskit/commit/f3d30b9ba2f66e08fb7f78c304ab8a9e83e1aeca))
* Remove unnecessary explicit lifetimes ([#488](https://github.com/forksnd/accesskit/issues/488)) ([d2bcd6d](https://github.com/forksnd/accesskit/commit/d2bcd6d3048d23df4e132bee6171eb247b2dc2c8))
* Support text fields without a value property ([#274](https://github.com/forksnd/accesskit/issues/274)) ([5ae557b](https://github.com/forksnd/accesskit/commit/5ae557b40d395b4a9966a90a2d80e7d97ad50bf9))
* Tell docs.rs to only build accesskit_windows on Windows ([#483](https://github.com/forksnd/accesskit/issues/483)) ([1fead29](https://github.com/forksnd/accesskit/commit/1fead296ed012f83afb482021051ccc1d4946167))
* Update `windows` to `0.54` ([#373](https://github.com/forksnd/accesskit/issues/373)) ([50f112f](https://github.com/forksnd/accesskit/commit/50f112f0085a03f0180f86915d2ac4e5845f6b63))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update windows crate to v0.48 ([#257](https://github.com/forksnd/accesskit/issues/257)) ([cc703ed](https://github.com/forksnd/accesskit/commit/cc703ed33d535aa1803e423a53beff9354b5b0df))
* Update windows to 0.58 on accesskit_windows ([#453](https://github.com/forksnd/accesskit/issues/453)) ([cda35e7](https://github.com/forksnd/accesskit/commit/cda35e77a78f72386c2bfd88e9fd29000106f7e6))
* Update windows-rs to 0.44 ([#220](https://github.com/forksnd/accesskit/issues/220)) ([a6b0a12](https://github.com/forksnd/accesskit/commit/a6b0a124e7511e37760d769b517fd5fc9050160b))
* Update winit to 0.30 ([#397](https://github.com/forksnd/accesskit/issues/397)) ([de93be3](https://github.com/forksnd/accesskit/commit/de93be387c03a438fbf598670207e578686e6bcf))
* Use common filters across platform adapters ([#287](https://github.com/forksnd/accesskit/issues/287)) ([09c1204](https://github.com/forksnd/accesskit/commit/09c12045ff4ccdb22f0cf643077a27465013572d))


### Miscellaneous Chores

* Update winit to 0.28 ([#207](https://github.com/forksnd/accesskit/issues/207)) ([3ff0cf5](https://github.com/forksnd/accesskit/commit/3ff0cf59f982af504499142a3804f7aeeb4defe0))


### Code Refactoring

* Clean up roles and properties ([#289](https://github.com/forksnd/accesskit/issues/289)) ([4fc9c55](https://github.com/forksnd/accesskit/commit/4fc9c55c91812472593923d93ff89d75ff305ee4))
* Clean up table roles and properties ([#393](https://github.com/forksnd/accesskit/issues/393)) ([e34dad9](https://github.com/forksnd/accesskit/commit/e34dad94448a5321ece9def3f2e054aa5f62dd79))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389)) ([1b153ed](https://github.com/forksnd/accesskit/commit/1b153ed51f8421cdba2dc98beca2e8f5f8c781bc))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296)) ([4fc7846](https://github.com/forksnd/accesskit/commit/4fc7846d732d61fb45c023060ebab96801a0053e))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179)) ([f35c941](https://github.com/forksnd/accesskit/commit/f35c941f395f3162db376a69cfaaaf770d376267))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Optimize simple string getters ([#493](https://github.com/forksnd/accesskit/issues/493)) ([484fd7c](https://github.com/forksnd/accesskit/commit/484fd7cbfb778222369d3f57d31dd998f6fa80d8))
* Rename `Checked` to `Toggled`; drop `ToggleButton` role ([#388](https://github.com/forksnd/accesskit/issues/388)) ([6bc040b](https://github.com/forksnd/accesskit/commit/6bc040b7cf75cdbd6a019cc380d8dbce804b3c81))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476)) ([7d8910e](https://github.com/forksnd/accesskit/commit/7d8910e35f7bc0543724cc124941a3bd0304bcc0))
* Rename `Role::InlineTextBox` to `TextRun` ([#473](https://github.com/forksnd/accesskit/issues/473)) ([29fa341](https://github.com/forksnd/accesskit/commit/29fa34125a811bd3a0f9da579a9f35c9da90bf29))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_consumer bumped from 0.27.0 to 0.28.0
</details>

<details><summary>accesskit_winit: 0.27.0</summary>

## [0.27.0](https://github.com/forksnd/accesskit/compare/accesskit_winit-v0.26.0...accesskit_winit-v0.27.0) (2025-03-25)


###   BREAKING CHANGES

* Panic if the window is visible when the adapter is created, for adapters where this is a problem ([#529](https://github.com/forksnd/accesskit/issues/529))
* Make accesskit_android an optional dependency of accesskit_winit ([#524](https://github.com/forksnd/accesskit/issues/524))
* Add event loop parameter to winit adapter constructors ([#517](https://github.com/forksnd/accesskit/issues/517))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434))
* Update winit to 0.30 ([#397](https://github.com/forksnd/accesskit/issues/397))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375))
* Lazily activate Unix adapters ([#324](https://github.com/forksnd/accesskit/issues/324))
* Remove `accesskit_winit::Adapter::update` ([#325](https://github.com/forksnd/accesskit/issues/325))
* Force a semver break for the winit rwh feature additions ([#322](https://github.com/forksnd/accesskit/issues/322))
* Rename `accesskit_winit::Adapter::on_event` to `process_event` ([#307](https://github.com/forksnd/accesskit/issues/307))
* Bump winit to 0.29 ([#256](https://github.com/forksnd/accesskit/issues/256))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205))
* Update winit to 0.28 ([#207](https://github.com/forksnd/accesskit/issues/207))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179))

### deps

* Bump winit to 0.29 ([#256](https://github.com/forksnd/accesskit/issues/256)) ([4eb21ff](https://github.com/forksnd/accesskit/commit/4eb21ff64256fcf0a16ab831554b06b80de9b36e))


### Features

* Add `author_id` property ([#424](https://github.com/forksnd/accesskit/issues/424)) ([0d1c56f](https://github.com/forksnd/accesskit/commit/0d1c56f0bdde58715e1c69f6015df600cb7cb8c1))
* Add features for async runtimes on Unix ([#248](https://github.com/forksnd/accesskit/issues/248)) ([b56b4ea](https://github.com/forksnd/accesskit/commit/b56b4ea7c967ee5a1dae21a2fa0dcd385346031e))
* Allow providing app_name, toolkit_name and toolkit_version in Tree, remove parameters from unix adapter constructor ([#291](https://github.com/forksnd/accesskit/issues/291)) ([5313860](https://github.com/forksnd/accesskit/commit/531386023257150f49b5e4be942f359855fb7cb6))
* Android adapter ([#500](https://github.com/forksnd/accesskit/issues/500)) ([7e65ac7](https://github.com/forksnd/accesskit/commit/7e65ac77d7e108ac5b9f3722f488a2fdf2e3b3e0))
* Basic Unix platform adapter ([#198](https://github.com/forksnd/accesskit/issues/198)) ([1cea32e](https://github.com/forksnd/accesskit/commit/1cea32e44ee743b778ac941ceff9087ae745cb37))
* Feature-gate the Unix adapter in accesskit_winit ([#214](https://github.com/forksnd/accesskit/issues/214)) ([be95807](https://github.com/forksnd/accesskit/commit/be95807dda64f2a49b4d20cc9084b14a7aa2844e))
* Make the core crate no-std ([#468](https://github.com/forksnd/accesskit/issues/468)) ([2fa0d3f](https://github.com/forksnd/accesskit/commit/2fa0d3f5b2b7ac11ef1751c133706f29e548bd6d))


### Bug Fixes

* Account for window decorations when `accesskit_winit::Adapter::process_event` receives a resizing event on Unix ([#312](https://github.com/forksnd/accesskit/issues/312)) ([e2b264c](https://github.com/forksnd/accesskit/commit/e2b264c2e5b0fb699576f2ece905509c38ffc9be))
* Add a `rwh_05` feature flag to `accesskit_winit` ([#319](https://github.com/forksnd/accesskit/issues/319)) ([f4d279c](https://github.com/forksnd/accesskit/commit/f4d279c5ece16df2925c0e31dc82eaf192c40cd0))
* Add missing semicolons when not returning anything ([#303](https://github.com/forksnd/accesskit/issues/303)) ([38d4de1](https://github.com/forksnd/accesskit/commit/38d4de1442247e701047d75122a9638a2ed99b1f))
* Don't force winit's X11 and Wayland features to be enabled ([#209](https://github.com/forksnd/accesskit/issues/209)) ([a3ed357](https://github.com/forksnd/accesskit/commit/a3ed35754ad8f69a8ed54adacc30b6d57c19329a))
* Fix doc build for accesskit_winit ([#281](https://github.com/forksnd/accesskit/issues/281)) ([e3b38b8](https://github.com/forksnd/accesskit/commit/e3b38b8164d0c5442a5a1904165e2b05847376c2))
* Force a semver break for the winit rwh feature additions ([#322](https://github.com/forksnd/accesskit/issues/322)) ([61acdb0](https://github.com/forksnd/accesskit/commit/61acdb0ea083263c88a00ad4db637b25863852c0))
* Force a semver-breaking version bump in downstream crates ([#234](https://github.com/forksnd/accesskit/issues/234)) ([773389b](https://github.com/forksnd/accesskit/commit/773389bff857fa18edf15de426e029251fc34591))
* Increase minimum supported Rust version to `1.70` ([#396](https://github.com/forksnd/accesskit/issues/396)) ([a8398b8](https://github.com/forksnd/accesskit/commit/a8398b847aa003de91042ac45e33126fc2cae053))
* Lazily activate Unix adapters ([#324](https://github.com/forksnd/accesskit/issues/324)) ([54ed036](https://github.com/forksnd/accesskit/commit/54ed036c99d87428a8eb5bb03fd77e9e31562d4c))
* Make accesskit_android an optional dependency of accesskit_winit ([#524](https://github.com/forksnd/accesskit/issues/524)) ([bb17d44](https://github.com/forksnd/accesskit/commit/bb17d449b601eaffad1c7201ec5bf8de241bb8f8))
* Panic if the window is visible when the adapter is created, for adapters where this is a problem ([#529](https://github.com/forksnd/accesskit/issues/529)) ([c43c37b](https://github.com/forksnd/accesskit/commit/c43c37ba2502656fcae4fd726b9b7db0bb520f31))
* Reduce the winit version requirement to match egui ([#170](https://github.com/forksnd/accesskit/issues/170)) ([1d27482](https://github.com/forksnd/accesskit/commit/1d27482221140c1f3b3e3eaf93e7feaf8105611d))
* Remove `accesskit_winit::Adapter::update` ([#325](https://github.com/forksnd/accesskit/issues/325)) ([f121bff](https://github.com/forksnd/accesskit/commit/f121bffe9e651fd2ac6deb882f57e1c9b613b7eb))
* Run our own async executor on Unix ([#337](https://github.com/forksnd/accesskit/issues/337)) ([8f937ba](https://github.com/forksnd/accesskit/commit/8f937baaa510dd96da196501822b82f75f05b595))
* Show an error at compile-time if no raw-window-handle feature is enabled for the winit adapter ([#339](https://github.com/forksnd/accesskit/issues/339)) ([a24f5fd](https://github.com/forksnd/accesskit/commit/a24f5fd443a683a6194b54244052ff3e1cc05de6))
* Update minimum supported Rust version to 1.75 ([#457](https://github.com/forksnd/accesskit/issues/457)) ([fc622fe](https://github.com/forksnd/accesskit/commit/fc622fe7657c80a4eedad6f6cded11d2538b54d5))
* Update winit to 0.30 ([#397](https://github.com/forksnd/accesskit/issues/397)) ([de93be3](https://github.com/forksnd/accesskit/commit/de93be387c03a438fbf598670207e578686e6bcf))
* Update winit to 0.30.9 ([#511](https://github.com/forksnd/accesskit/issues/511)) ([0be21e6](https://github.com/forksnd/accesskit/commit/0be21e6a2979af483b573b1c9b07c677286b871d))
* Use raw-window-handle 0.6 ([#310](https://github.com/forksnd/accesskit/issues/310)) ([3fa69ab](https://github.com/forksnd/accesskit/commit/3fa69ab4d9216b51b651d3cf2a9c8217a77069f4))
* Use the new HWND type on accesskit_winit ([#453](https://github.com/forksnd/accesskit/issues/453)) ([68a2462](https://github.com/forksnd/accesskit/commit/68a24629381f0b18f6ed1ee008fe72ce9330092e))


### Miscellaneous Chores

* Update winit to 0.28 ([#207](https://github.com/forksnd/accesskit/issues/207)) ([3ff0cf5](https://github.com/forksnd/accesskit/commit/3ff0cf59f982af504499142a3804f7aeeb4defe0))


### Code Refactoring

* Add event loop parameter to winit adapter constructors ([#517](https://github.com/forksnd/accesskit/issues/517)) ([0d15f24](https://github.com/forksnd/accesskit/commit/0d15f246a301a68af4424f7602c2f3be25da9327))
* Decouple in-tree focus from host window/view focus ([#278](https://github.com/forksnd/accesskit/issues/278)) ([d360d20](https://github.com/forksnd/accesskit/commit/d360d20cf951e7643b81a5303006c9f7daa5bd56))
* Drop `DefaultActionVerb` ([#472](https://github.com/forksnd/accesskit/issues/472)) ([ef3b003](https://github.com/forksnd/accesskit/commit/ef3b0038224459094f650368412650bc3b69526b))
* Drop `NodeClassSet` ([#389](https://github.com/forksnd/accesskit/issues/389)) ([1b153ed](https://github.com/forksnd/accesskit/commit/1b153ed51f8421cdba2dc98beca2e8f5f8c781bc))
* Drop `Tree::app_name` ([#492](https://github.com/forksnd/accesskit/issues/492)) ([089794c](https://github.com/forksnd/accesskit/commit/089794c8f74957e91a19ae3df508e2a892f39ebc))
* Make `ActionHandler::do_action` take `&mut self` ([#296](https://github.com/forksnd/accesskit/issues/296)) ([4fc7846](https://github.com/forksnd/accesskit/commit/4fc7846d732d61fb45c023060ebab96801a0053e))
* Make `Node` opaque and optimize it for size ([#205](https://github.com/forksnd/accesskit/issues/205)) ([4811152](https://github.com/forksnd/accesskit/commit/48111521439b76c1a8687418a4b20f9b705eac6d))
* Move lazy initialization from the core platform adapter to the caller ([#179](https://github.com/forksnd/accesskit/issues/179)) ([f35c941](https://github.com/forksnd/accesskit/commit/f35c941f395f3162db376a69cfaaaf770d376267))
* Move thread synchronization into platform adapters; drop parking_lot ([#212](https://github.com/forksnd/accesskit/issues/212)) ([5df52e5](https://github.com/forksnd/accesskit/commit/5df52e5545faddf6a51905409013c2f5be23981e))
* New approach to lazy initialization ([#375](https://github.com/forksnd/accesskit/issues/375)) ([9baebdc](https://github.com/forksnd/accesskit/commit/9baebdceed7300389b6768815d7ae48f1ce401e4))
* Rename `accesskit_winit::Adapter::on_event` to `process_event` ([#307](https://github.com/forksnd/accesskit/issues/307)) ([6fbebde](https://github.com/forksnd/accesskit/commit/6fbebdeb9d1e96b1776ed1faf7ad21d9cc0a68df))
* Rename `name` to `label` and use `value` for label content ([#475](https://github.com/forksnd/accesskit/issues/475)) ([e0053a5](https://github.com/forksnd/accesskit/commit/e0053a5399929e8e0d4f07aa18de604ed8766ace))
* Rename `NodeBuilder` to `Node` and the old `Node` to `FrozenNode` ([#476](https://github.com/forksnd/accesskit/issues/476)) ([7d8910e](https://github.com/forksnd/accesskit/commit/7d8910e35f7bc0543724cc124941a3bd0304bcc0))
* Rename the `StaticText` role to `Label` ([#434](https://github.com/forksnd/accesskit/issues/434)) ([7086bc0](https://github.com/forksnd/accesskit/commit/7086bc0fad446d3ed4a0fd5eff641a1e75f6c599))
* Switch to simple unsigned 64-bit integer for node IDs ([#276](https://github.com/forksnd/accesskit/issues/276)) ([3eadd48](https://github.com/forksnd/accesskit/commit/3eadd48ec47854faa94a94ebf910ec08f514642f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * accesskit bumped from 0.18.0 to 0.8.1
    * accesskit_windows bumped from 0.26.0 to 0.27.0
    * accesskit_macos bumped from 0.19.0 to 0.20.0
    * accesskit_unix bumped from 0.14.0 to 0.15.0
    * accesskit_android bumped from 0.1.1 to 0.2.0
</details>

---
This PR was generated with [Release Please](https://github.com/googleapis/release-please). See [documentation](https://github.com/googleapis/release-please#release-please).