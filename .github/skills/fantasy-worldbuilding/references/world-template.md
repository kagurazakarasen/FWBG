# world-settings.yaml 出力テンプレート

このファイルはエージェントが `world-settings.yaml` を生成するためのテンプレートです。
`null` はユーザーが未回答の項目を示します。

---

## テンプレート本文

```yaml
# ============================================================
# ファンタジー世界設定ファイル
# 生成日: <DATE>
# ============================================================

meta:
  world_name: "<世界名>"
  world_type: "original"  # original | alternative_earth
  story_era: "medieval"   # ancient | medieval | renaissance | industrial | modern | other
  primary_region: "<物語の主な舞台となる地域名>"

# ============================================================
# 地理と物理的特徴
# ============================================================
geography:
  planet:
    multiple_suns: false
    moon_count: 1
    notes: null

  terrain:
    major_mountain_ranges:
      - name: null
        description: null
    major_rivers:
      - name: null
        description: null
    notable_regions:
      - name: null
        type: null  # forest | desert | plains | swamp | tundra | etc.
        description: null

  climate:
    general: null  # 気候の概要
    special_zones: []  # 特殊な気候帯・地域

  resources:
    abundant:
      - null  # 豊富な資源
    scarce:
      - null  # 希少な資源
    contested:
      - null  # 争奪されている資源

# ============================================================
# 魔法システム
# ============================================================
magic:
  exists: true
  prevalence: "rare"  # common | uncommon | rare | very_rare | legendary

  source:
    type: null  # divine | natural_energy | life_force | willpower | ley_lines | etc.
    description: null
    is_depletable: false  # 枯渇性資源か

  cost:
    has_cost: null
    cost_description: null  # 消耗するもの（生命力・記憶・寿命など）
    long_term_effects: null

  learning:
    requires_talent: null  # 才能必須か
    training_duration: null
    training_method: null  # apprenticeship | school | self-taught | divine_gift

  casting:
    requires_words: null
    requires_components: null
    requires_ritual: null
    casting_time: null  # instant | minutes | hours | days
    can_combine_casters: null

  social_status:
    general_perception: null  # revered | respected | neutral | feared | persecuted
    legal_status: null  # full_citizen | restricted | licensed | outlawed
    requires_license: null
    political_power: null

  technology_relationship: null  # complement | substitute | rival | independent

  prohibited_magic:
    - null  # 禁じられた魔法の種類

  military_use:
    used_in_warfare: null
    tactical_role: null  # artillery | intelligence | support | frontline

  healing_magic:
    exists: null
    how_it_works: null

# ============================================================
# 種族
# ============================================================
races:
  humans:
    present: true
    dominant: true
    distribution: null

  non_human:
    - name: null  # 種族名（例: エルフ、ドワーフ）
      present: null
      rarity: null  # common | uncommon | rare
      typical_habitat: null
      social_integration: null  # integrated | segregated | isolated | hostile
      magic_affinity: null
      notes: null

# ============================================================
# 歴史
# ============================================================
history:
  age_of_world: null  # 文明の存続期間の概算
  origin_of_people: null  # evolved | created_by_gods | migrated | unknown

  major_events:
    - name: null
      approximate_time: null  # 「約300年前」など相対的な記述でよい
      description: null
      lasting_impact: null

  current_situation:
    ongoing_conflicts: []
    recent_wars:
      - belligerents: null
        outcome: null
        how_long_ago: null

  languages:
    count: null
    common_tongue:
      name: null
      used_by: null
    trade_language:
      name: null
      used_by: null
    other_languages: []

# ============================================================
# 社会と文化（主要な舞台となる地域）
# ============================================================
society:
  population:
    approximate: null
    distribution: null  # 都市・農村の割合など

  social_structure:
    family_unit: null  # nuclear | extended | clan | tribe
    class_system:
      - class: null  # 階層名
        description: null
        mobility: null  # easy | possible | difficult | impossible
    disenfranchised_groups: []  # 権利を制限されたグループ

  customs:
    coming_of_age:
      description: null
      different_by_gender: null
    marriage:
      description: null
      who_sanctions: null  # religious | civil | family | none
    death_burial:
      description: null

  values:
    most_important:
      - null  # 最重要とされる価値観
    acceptable_but_unusual_in_reality:
      - null  # 現実では非常識だがここでは普通なこと
    major_taboos:
      - null

  religion:
    gods_exist: null
    gods_intervene_directly: null
    major_religions:
      - name: null
        deity_count: null
        stance_on_magic: null  # supports | neutral | restricts | bans
        political_power: null
    state_religion: null
    religious_freedom: null

# ============================================================
# 政治（主要な舞台となる地域）
# ============================================================
politics:
  government_type: null  # monarchy | feudal | republic | theocracy | oligarchy | democracy | empire | other
  stability: null  # stable | tense | unstable | civil_war

  head_of_state:
    title: null
    succession: null  # hereditary | elected | appointed | conquest | divine_right

  services_provided:
    - null  # 政府が提供するサービス（軍・裁判所・教育など）

  law:
    written_law: null
    punishment_philosophy: null  # punitive | rehabilitative | deterrent
    notable_laws:
      - null

  foreign_relations:
    allies:
      - null
    rivals:
      - null
    at_war_with:
      - null

# ============================================================
# 経済
# ============================================================
economy:
  primary_industries:
    - null  # 農業・鉱業・漁業・製造業など

  trade:
    exports:
      - null
    imports:
      - null
    importance: null  # critical | important | moderate | minimal

  currency:
    system: null  # coins | barter | magic | mixed
    who_mints: null
    common_denominations: []

  transportation:
    land:
      - null  # 馬・馬車・魔法の乗り物など
    water:
      - null  # 船・魔法など
    magical:
      - null  # テレポート・魔法の絨毯など

  communication:
    methods:
      - null  # 郵便・魔法の鏡・使者など
    speed: null  # 情報が届くまでの速さの概算

# ============================================================
# 技術水準
# ============================================================
technology:
  equivalent_era: null  # ancient_rome | medieval | renaissance | industrial_revolution | mixed
  notable_inventions:
    - null  # この世界特有の重要な発明・技術
  magic_replaced_technology:
    - area: null
      description: null
  underdeveloped_areas:
    - null  # 通常の技術発展で存在するはずなのにない技術

# ============================================================
# 整合性メモ（エージェントが記録）
# ============================================================
consistency_notes:
  resolved_tensions:
    - issue: null
      resolution: null
  tbd_items:
    - null  # まだ未決定の項目
  story_hooks:
    - null  # 世界設定から生まれる物語の種
```

---

## 記入方針

- `null` → ユーザー未回答または「まだ決めていない」
- `TBD` → 後で決める予定
- 自由記述は `"ダブルクォート"` で囲む
- リストは `- 項目` 形式
- コメントは `#` で記述（生成後も可読性のために残す）
