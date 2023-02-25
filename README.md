# Bugrock JSON UI Schemas

VSCode Settings Example
```json
"json.schemas": [
  {
    "url": "https://kalmemarq.github.io/Bugrock-JSON-UI-Schemas/ui.schema.json",
    "fileMatch": [
      "*.ui.json",
      "*.uidx",
      "ui/**/*.json",
      "!_global_variables.json",
      "!_ui_defs.json"
    ]
  },
  {
    "url": "https://kalmemarq.github.io/Bugrock-JSON-UI-Schemas/ui_defs.schema.json",
    "fileMatch": [
      "ui/_ui_defs.json"
    ]
  },
  {
    "url": "https://kalmemarq.github.io/Bugrock-JSON-UI-Schemas/global_variables.schema.json",
    "fileMatch": [
      "ui/_global_variables.json"
    ]
  }
]
```

## UI Element Types

| Name                      | Allowed Properties                                                                                                                                                                   |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```panel```               | [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                                            |
| ```stack_panel```         | [Stack Panel](#stack-panel), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                               |
| ```image```               | [Sprite](#sprite), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                         |
| ```label```               | [Text](#text), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                             |
| ```input_panel```         | [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                         |
| ```grid```                | [Grid](#grid), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                             |
| ```button```              | [Button](#button), [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                      |
| ```toggle```              | [Toggle](#toggle), [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                      |
| ```slider```              | [Slider](#slider), [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                      |
| ```slider_box```          | [Slider Box](#slider-box), [Input](#input), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                |
| ```screen```              | [Screen](#screen), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                        |
| ```dropdown```            | [Dropdown](#dropdown), [Toggle](#toggle), [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)               |
| ```edit_box```            | [Text Edit](#text-edit), [Input](#input), [Focus](#focus), [Sound](#sound), [Button](#button), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)             |
| ```custom```              | [Custom](#custom), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                         |
| ```scroll_view```         | [Scroll View](#scroll-view), [Input](#input), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                              |
| ```scroll_box```          | [Input](#input), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                           |
| ```scroll_track```        | [Input](#input), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                           |
| ```factory```             | [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                                                                            |
| ```selection_wheel```     | [Selection Wheel](#selection-wheel), [Input](#input), [Focus](#focus), [Sound](#sound), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                    |
| ```grid_page_indicator``` | [Grid Page Indicator](#grid-page-indicator), [Grid](#grid), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                |
| ```label_cycler```        | [Label Cycler](#label-cycler), [Cycler](#cycler), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                          |
| ```image_cycler```        | [Image Cycler](#image-cycler), [Cycler](#cycler), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                          |

### Unused/No Longer Work

| Name                 | Type                                                                                                                               |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| ```tab```            | [Tab](#tab-unusedno-longer-works), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                       |
| ```carousel_label``` | [Carousel Label](#carousel-label-unusedno-longer-works), [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding) |
| ```grid_item```      | [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                          |
| ```scrollbar```      | [Controls](#control), [Layout](#layout) and [Data Binding](#data-binding)                                                          |

## Properties

### Control

| Name                            | Type                                                                                                   |
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| ```controls```                  | array of UI elements                                                                                   |
| ```variables```                 | object or array of objects                                                                             |
| ```visible```                   | boolean                                                                                                |
| ```ignored```                   | boolean                                                                                                |
| ```modifications```             | array of modifications                                                                                 |
| ```anims```                     | array of strings                                                                                       |
| ```disable_anim_fast_forward``` | boolean                                                                                                |
| ```animation_reset_name```      | string                                                                                                 |
| ```visible```                   | boolean                                                                                                |
| ```enabled```                   | boolean                                                                                                |
| ```layer```                     | integer                                                                                                |
| ```alpha```                     | float (>=0.0 and <= 1.0)                                                                               |
| ```propagate_alpha```           | boolean                                                                                                |
| ```clips_children```            | boolean                                                                                                |
| ```allow_clipping```            | boolean                                                                                                |
| ```clip_offset```               | Vector [x, y]                                                                                          |
| ```clip_state_change_event```   | string                                                                                                 |
| ```enabled_scissor_test```      | boolean                                                                                                |
| ```property_bag```              | object                                                                                                 |
| ```selected```                  | boolean                                                                                                |
| ```use_child_anchors```         | boolean                                                                                                |
| ```grid_position```             | Vector [column, row]                                                                                   |
| ```debug```                     | ```white```, ```black```, ```gray```, ```red```, ```blue```, ```green```, ```yellow``` or ```purple``` |

#### Unused/No Longer Works

| Name          | Type      |
|---------------|-----------|
| ```z_order``` | integer   |

### Layout

| Name                            | Type                                                                                                                                                                 |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```anchor_from```               | ```top_left```, ```top_middle```, ```top_right```, ```left_middle```, ```center```, ```right_middle```, ```bottom_left```, ```bottom_middle``` or ```bottom_right``` |
| ```anchor_to```                 |```top_left```, ```top_middle```, ```top_right```, ```left_middle```, ```center```, ```right_middle```, ```bottom_left```,```bottom_middle``` or ```bottom_right```   |
| ```contained```                 | boolean                                                                                                                                                              |
| ```draggable```                 | boolean                                                                                                                                                              |
| ```follows_cursor```            | boolean                                                                                                                                                              |
| ```offset```                    | Vector [x, y]                                                                                                                                                        |
| ```size```                      | Vector [width, height]                                                                                                                                               |
| ```max_size```                  | Vector [width, height]                                                                                                                                               |
| ```min_size```                  | Vector [width, height]                                                                                                                                               |
| ```inherit_max_sibling_width``` | boolean                                                                                                                                                              |
| ```inherit_max_sibling_height```| boolean                                                                                                                                                              |
| ```use_anchored_offset```       | boolean                                                                                                                                                              |

### Data Binding

| Name           | Type                                  |
|----------------|---------------------------------------|
| ```bindings``` | array of [BindingItem](#bindingitem)  |

#### BindingItem

| Name                            | Type                                                                                           |
|---------------------------------|------------------------------------------------------------------------------------------------|
| ```ignored```                   | boolean                                                                                        |
| ```binding_type```              | ```global```, ```collection```, ```collection_details``` or ```view```                         |
| ```binding_name```              | string                                                                                         |
| ```binding_name_override```     | string                                                                                         |
| ```binding_collection_name```   | string                                                                                         |
| ```binding_collection_prefix``` | string                                                                                         |
| ```binding_condition```         | ```always```, ```visible```, ```once```, ```always_when_visible``` or ```visibility_changed``` |
| ```source_control_name```       | string                                                                                         |
| ```source_property_name```      | string                                                                                         |
| ```target_property_name```      | string                                                                                         |
| ```resolve_sibling_scope```     | boolean                                                                                        |

### Stack Panel

| Name              | Type                                 |
|-------------------|--------------------------------------|
| ```orientation``` | ```vertical``` and ```horizontal```  |

### Text

| Name                           | Type
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```text```                     | string                                                                                                                                                                                |
| ```color```                    | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |
| ```locked_color```             | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |
| ```shadow```                   | boolean                                                                                                                                                                               |
| ```font_size```                | ```small```, ```normal```, ```large``` or ```extra_large```                                                                                                                           |
| ```font_scale_factor```        | float (0 >=)                                                                                                                                                                          |
| ```localize```                 | boolean                                                                                                                                                                               |
| ```line_padding```             | number                                                                                                                                                                                |
| ```font_type```                | string                                                                                                                                                                                |
| ```backup_font_type```         | string                                                                                                                                                                                |
| ```text_alignment```           | ```left```,```center``` and ```right```                                                                                                                                               |
| ```hide_hypen```               | boolean                                                                                                                                                                               |
| ```locked_alpha```             | float (0.0 >= and <= 1.0)                                                                                                                                                             |
| ```enable_profanity_filter```  | boolean                                                                                                                                                                               |
| ```notify_on_ellipses```       | array of strings                                                                                                                                                                      |

#### Unused/No Longer Works

| Name                           | Type                                                                                                                                                                                 |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```alignment```                | ```left```,```center``` or ```right```                                                                                                                                               |
| ```use_place_holder```         | boolean                                                                                                                                                                              |
| ```place_holder_text```        | string                                                                                                                                                                               |
| ```place_holder_text_color```  | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |

### Sprite

| Name                               | Type                                                                                                                                                                               |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```texture```                      | string                                                                                                                                                                             |
| ```uv```                           | Vector [u, v]                                                                                                                                                                      |
| ```uv_size```                      | Vector [width, height]                                                                                                                                                             |
| ```nineslice_size```               | integer, Vector [x, y] or Vector [x0, y0, x1, y1]                                                                                                                                  |
| ```base_size```                    | Vector [width, height]                                                                                                                                                             |
| ```color```                        | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray```, ```blue``` |
| ```tiled```                        | boolean, ```x```,  ```y```, ```xy``` or ```yx```                                                                                                                                   |
| ```tiled_scale```                  | Vector [x, y]                                                                                                                                                                      |
| ```clip_direction```               | ```left```, ```right```, ```up```, ```down``` or ```center```                                                                                                                      |
| ```clip_ratio```                   | float (0.0 >= and <= 1.0)                                                                                                                                                          |
| ```clip_pixelperfect```            | boolean                                                                                                                                                                            |
| ```keep_ratio```                   | boolean                                                                                                                                                                            |
| ```bilinear```                     | boolean                                                                                                                                                                            |
| ```fill```                         | boolean                                                                                                                                                                            |
| ```grayscale```                    | boolean                                                                                                                                                                            |
| ```force_texture_reload```         | boolean                                                                                                                                                                            |
| ```$fit_to_witdh```                | boolean                                                                                                                                                                            |
| ```zip_folder```                   | string                                                                                                                                                                             |
| ```texture_file_system```          | ```RawPath``` or ```InAppPackage```                                                                                                                                                |
| ```allow_debug_missing_texture```  | boolean                                                                                                                                                                            |

#### Unused/No Longer Works

| Name                | Type     |
|---------------------|----------|
| ```pixel_perfect``` | boolean  |

### TTS

| Name                                        |
|---------------------------------------------|
| ```tts_name```                              |
| ```tts_control_header```                    |
| ```tts_section_header```                    |
| ```tts_control_type_order_priority```       |
| ```tts_index_priority```                    |
| ```tts_toggle_on```                         |
| ```tts_toggle_off```                        |
| ```tts_override_control_value```            |
| ```tts_inherit_siblings```                  |
| ```tts_value_changed```                     |
| ```ttsSectionContainer```                   |
| ```tts_ignore_count```                      |
| ```tts_skip_message```                      |
| ```tts_skip_children```                     |
| ```tts_value_order_priority```              |
| ```tts_play_on_unchanged_focus_control```   |
| ```tts_ignore_subsections```                |
| ```text_tts```                              |

### Sound

| Name               | Type               |
|--------------------|--------------------|
| ```sound_name```   | string             |
| ```sound_pitch```  | string             |
| ```sound_volume``` | float              |
| ```sounds```       | array of SoundItem |

#### SoundItem

| Name                            | Type   |
|---------------------------------|--------|
| ```sound_name```                | string |
| ```sound_pitch```               | float  |
| ```sound_volume```              | float  |
| ```min_seconds_between_plays``` | number |
| ```event_type```                | string |
| ```button_name```               | string |

### Button

| Name                  | Type    |
|-----------------------|---------|
| ```default_control``` | string  |
| ```hover_control```   | string  |
| ```pressed_control``` | string  |
| ```locked_control```  | string  |

### Toggle

| Name                                | Type    |
|-------------------------------------|---------|
| ```radio_toggle_group```            | boolean |
| ```toggle_name```                   | string  |
| ```toggle_default_state```          | boolean |
| ```toggle_group_forced_index```     | integer |
| ```toggle_group_default_selected``` | integer |
| ```reset_on_focus_lost```           | boolean |
| ```toggle_on_hover```               | string  |
| ```toggle_on_button```              | string  |
| ```toggle_off_button```             | string  |
| ```enable_directional_toggling```   | boolean |
| ```toggle_grid_collection_name```   | string  |
| ```checked_control```               | string  |
| ```unchecked_control```             | string  |
| ```checked_hover_control```         | string  |
| ```unchecked_hover_control```       | string  |
| ```checked_locked_control```        | string  |
| ```unchecked_locked_control```      | string  |
| ```checked_locked_hover_control```  | string  |
| ```unchecked_locked_hover_control```| string  |

### Slider

| Name                              | Type                               |
|-----------------------------------|------------------------------------|
| ```slider_track_button```         | string                             |
| ```slider_small_decrease_button```| string                             |
| ```slider_small_increase_button```| string                             |
| ```slider_steps```                | integer                            |
| ```slider_direction```            | ```vertical``` or ```horizontal``` |
| ```slider_timeout```              | number                             |
| ```slider_collection_name```      | string                             |
| ```slider_name```                 | string                             |
| ```slider_select_on_hover```      | string                             |
| ```slider_selected_button```      | string                             |
| ```slider_deselected_button```    | string                             |
| ```slider_box_control```          | string                             |
| ```background_control```          | string                             |
| ```background_hover_control```    | string                             |
| ```progress_control```            | string                             |
| ```progress_hover_control```      | string                             |

#### Unused/No Longer Works

| Name                                             | Type                                                                                                                                                                                 |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```slider_render_bar_background_color```         | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |
| ```slider_render_bar_progress_color```           | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |
| ```slider_render_bar_outline_color```            | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |
| ```slider_render_bar_background_hover_color```   | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |
| ```slider_render_bar_progress_hover_color```     | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |
| ```slider_render_bar_outline_hover_color```      | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue``` |

### Slider Box

| Name                  | Type   |
|-----------------------|--------|
| ```indent_control```  | string |

### Dropdown

| Name                           | Type   |
|--------------------------------|--------|
| ```dropdown_name```            | string |
| ```dropdown_content_control``` | string |
| ```dropdown_area```            | string |

### Grid

| Name                             | Type                                |
|----------------------------------|-------------------------------------|
| ```grid_dimensions```            | Vector[columns, rows]               |
| ```maximum_grid_items```         | integer (0 >=)                      |
| ```grid_dimension_binding```     | string                              |
| ```grid_rescaling_type```        | ```vertical``` or ```horizontal```  |
| ```grid_fill_direction```        | ```vertical``` or ```horizontal```  |
| ```precached_grid_item_count```  | integer                             |
| ```grid_item_template```         | string                              |

### Text Edit

| Name                                     | Type                                                            |
|------------------------------------------|-----------------------------------------------------------------|
| ```text_box_name```                      | string                                                          |
| ```text_edit_box_grid_collection_name``` | string                                                          |
| ```constrain_to_rect```                  | boolean                                                         |
| ```enabled_newline```                    | boolean                                                         |
| ```text_type```                          | ```ExtendedASCII```, ```IdentifierChars``` or ```NumberChars``` |
| ```max_length```                         | integer (0 >=)                                                  |
| ```text_control```                       | string                                                          |
| ```place_holder_control```               | string                                                          |
| ```can_be_deselected```                  | boolean                                                         |
| ```always_listening```                   | boolean                                                         |
| ```virtual_keyboard_buffer_control```    | string                                                          |

### Scroll View

| Name                                         | Type    |
|----------------------------------------------|---------|
| ```scrollbar_track_button```                 | string  |
| ```scrollbar_touch_button```                 | string  |
| ```scroll_speed```                           | number  |
| ```gesture_control_enabled```                | boolean |
| ```always_handle_scrolling```                | boolean |
| ```touch_mode```                             | boolean |
| ```scrollbar_box```                          | string  |
| ```scrollbar_track```                        | string  |
| ```scroll_view_port```                       | string  |
| ```scroll_content```                         | string  |
| ```scroll_box_and_track_panel```             | string  |
| ```jump_to_bottom_on_update```               | boolean |
| ```allow_scroll_even_when_content_fits```    | boolean |

### Focus

| Name                                 | Type                                                                   |
|--------------------------------------|------------------------------------------------------------------------|
| ```default_focus_precedence```       | integer                                                                |
| ```focus_enabled```                  | boolean                                                                |
| ```focus_wrap_enabled```             | boolean                                                                |
| ```focus_magnet_enabled```           | boolean                                                                |
| ```focus_identifier```               | string                                                                 |
| ```focus_change_down```              | string                                                                 |
| ```focus_change_up```                | string                                                                 |
| ```focus_change_left```              | string                                                                 |
| ```focus_change_right```             | string                                                                 |
| ```focus_mapping```                  | array of [FocusMappingItem](#focusmappingitem)                         |
| ```focus_container```                | boolean                                                                |
| ```use_last_focus```                 | boolean                                                                |
| ```focus_navigation_mode_left```     | string                                                                 |
| ```focus_navigation_mode_right```    | string                                                                 |
| ```focus_navigation_mode_down```     | string                                                                 |
| ```focus_navigation_mode_up```       | string                                                                 |
| ```focus_container_custom_left```    | ```contained```, ```none```, ```custom```, ```stop``` or empty string  |
| ```focus_container_custom_right```   | array of [FocusCustomItem](#focuscustomitem)                           |
| ```focus_container_custom_down```    | array of [FocusCustomItem](#focuscustomitem)                           |
| ```focus_container_custom_up```      | array of [FocusCustomItem](#focuscustomitem)                           |

#### Unused/No Longer works

These properties were misspelled. It took a while for the devs to notice. Classic json ui devs...

| Name                                 | Type   |
|--------------------------------------|--------|
| ```focus_nagivation_mode_right```    | string |
| ```focus_nagivation_mode_left```     | string |
| ```focus_nagivation_mode_down```     | string |
| ```focus_nagivation_mode_up```       | string |

#### FocusMappingItem

| Name                     | Type   |
|--------------------------|--------|
| ```focus_identifier```   | string |
| ```focus_change_right``` | string |
| ```focus_change_left```  | string |
| ```focus_change_up```    | string |
| ```focus_change_down```  | string |

#### FocusCustomItem

| Name                             | Type   |
|----------------------------------|--------|
| ```other_focus_container_name``` | string |

### Input

| Name                                     | Type                                               |
|------------------------------------------|----------------------------------------------------|
| ```button_mappings```                    | array of [ButtonMappingItem](#buttonmappingitem)   |
| ```modal```                              | boolean                                            |
| ```inline_modal```                       | boolean                                            |
| ```always_listen_to_input```             | boolean                                            |
| ```always_handle_pointer```              | boolean                                            |
| ```always_handle_controller_direction``` | boolean                                            |
| ```hover_enabled```                      | boolean                                            |
| ```prevent_touch_input```                | boolean                                            |
| ```consume_event```                      | boolean                                            |
| ```consume_hover_events```               | boolean                                            |
| ```gesture_tracking_button```            | string                                             |

#### ButtonMappingItem

| Name                                    | Type                                                                                   |
|-----------------------------------------|----------------------------------------------------------------------------------------|
| ```from_button_id```                    | string                                                                                 |
| ```to_button_id```                      | string                                                                                 |
| ```button_up_right_of_first_refusal```  | boolean                                                                                |
| ```mapping_type```                      | ```global```, ```focused```, ```pressed``` or ```double_pressed```                     |
| ```ignored```                           | boolean                                                                                |
| ```input_mode_condition```              | ```any```, ```gaze```, ```not_gaze```, ```not_gamepad``` or ```gamepad_and_not_gaze``` |
| ```ignore_input_scope```                | boolean                                                                                |
| ```scope```                             | ```global```, ```view``` or ```controller```                                           |
| ```consume_event```                     | boolean                                                                                |
| ```handle_select```                     | boolean                                                                                |
| ```handle_deselect```                   | boolean                                                                                |

### Screen

| Name                                         | Type    |
|----------------------------------------------|---------|
| ```render_only_when_topmost```               | boolean |
| ```screen_not_flushable```                   | boolean |
| ```always_accepts_input```                   | boolean |
| ```render_game_behind```                     | boolean |
| ```absorbs_input```                          | boolean |
| ```is_showing_menu```                        | boolean |
| ```is_modal```                               | boolean |
| ```should_steal_mouse```                     | boolean |
| ```low_frequency_rendering```                | boolean |
| ```screen_draws_last```                      | boolean |
| ```vr_mode```                                | boolean |
| ```force_render_below```                     | boolean |
| ```send_telemetry```                         | boolean |
| ```close_on_player_hurt```                   | boolean |
| ```cache_screen```                           | boolean |
| ```load_screen_immediately```                | boolean |
| ```gamepad_cursor```                         | boolean |
| ```gamepad_cursor_deflection_mode```         | boolean |
| ```should_be_skipped_during_automation```    | boolean |

### Custom

| Name           | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```renderer``` | ```hover_text_renderer```, ```3d_structure_renderer```, ```splash_text_renderer```, ```ui_holo_cursor```, ```trial_time_renderer```, ```panorama_renderer```, ```actor_portrait_renderer```, ```banner_pattern_renderer```, ```live_player_renderer```, ```web_view_renderer```, ```hunger_renderer```, ```bubbles_renderer```, ```mob_effects_renderer```, ```cursor_renderer```, ```progress_indicator_renderer```, ```camera_renderer```, ```horse_jump_renderer```, ```armor_renderer```, ```horse_heart_renderer```, ```heart_renderer```, ```hotbar_cooldown_renderer```, ```hotbar_renderer```, ```hud_player_renderer```, ```live_horse_renderer```, ```holographic_postrenderer```, ```enchanting_book_renderer```, ```debug_screen_renderer```, ```gradient_renderer```, ```paper_doll_renderer```, ```name_tag_renderer```, ```flying_item_renderer```, ```inventory_item_renderer```, ```credits_renderer```, ```vignette_renderer```, ```progress_bar_renderer```, ```debug_overlay_renderer```, ```background_renderer```, ```bundle_renderer```, ```editor_gizmo_renderer```, ```dash_renderer```, ```bohr_model_renderer``` or ```toast_renderer```<br>Also in Netease Edition: ```netease_paper_doll_renderer``` or ```netease_mini_map_renderer``` |

#### Progress Bar Renderer

| Name                   | Type                                                                                                                                                                                  |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```primary_color```    | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |
| ```secondary_color```  | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |

#### Gradient Renderer

| Name                      | Type                                                                                                                                                                                  |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```gradient_direction```  | ```vertical``` or ```horizontal```                                                                                                                                                    |
| ```color1```              | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |
| ```color2```              | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |

#### Name Tag Renderer

| Name                   | Type                                                                                                                                                                                         |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```text_color```       | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```         |
| ```background_color``` | Vector [red, green, blue, alpha] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```  |

#### Paper Doll Renderer

| Name                         | Type    |
|------------------------------|---------|
| ```camera_tilt_degrees```    | number  |
| ```starting_rotation```      | number  |
| ```use_selected_skin```      | boolean |
| ```use_uuid```               | boolean |
| ```use_skin_gui_scale```     | boolean |
| ```use_player_paperdoll```   | boolean |
| ```rotation```               | number  |

##### Also In Netease Edition

| Name                   | Type     |
|------------------------|----------|
| ```modelsize```        | number   |
| ```animation_looped``` | boolean  |
| ```animation```        | string   |

#### Netease Paper Doll Renderer

| Name                       | Type          |
|----------------------------|---------------|
| ```screen_offset```        | Vector [x, y] |
| ```screen_scale```         | float         |
| ```mob_body_rot_y```       | number        |
| ```mob_head_rot_y```       | number        |
| ```init_rot_y```           | number        |
| ```skeleton_model_name```  | string        |
| ```entity_identifier```    | string        |
| ```modelsize```            | number        |
| ```animation_looped```     | boolean       | 
| ```animation```            | string        |

#### Netease MiniMap Renderer

| Name                          | Type
|-------------------------------|--------------
| ```use_default_face_icon```   | boolean
| ```face_icon_bg_color```      | Vector [red, green, blue, alpha] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```
| ```enable_live_update```      | boolean
| ```live_update_interval```    | integer
| ```highest_y```               | ```0``` or ```-1``` 

### Grid Page Indicator

| Name                                    | Type   |
|-----------------------------------------|--------|
| ```grid_item_when_current```            | string |
| ```grid_item_when_not_current```        | string |
| ```cycler_manager_size_control_target```| string |

### Selection Wheel

| Name                            | Type             |
|---------------------------------|------------------|
| ```inner_radius```              | number           |
| ```outer_radius```              | number           |
| ```state_controls```            | array of strings |
| ```slice_count```               | integer          |
| ```button_name```               | string           |
| ```iterate_left_button_name```  | string           |
| ```iterate_right_button_name``` | string           |
| ```initial_button_slice```      | integer          |

### Cycler

| Name                            | Type   |
|---------------------------------|--------|
| ```target_cycler_to_compare```  | string |
| ```next_sub_page_button_name``` | string |
| ```prev_sub_page_button_name``` | string |

### Label Cycler

| Name              | Type               |
|-------------------|--------------------|
| ```text_labels``` | array of strings   |

### Image Cycler

| Name         | Type               |
|--------------|--------------------|
| ```images``` | array of ImageItem |

#### ImageItem

| Name               | Type   |
|--------------------|--------|
| ```texture_path``` | string |

### Tab (Unused/No Longer Works)

| Name               | Type    |
|--------------------|---------|
| ```tab_index```    | integer |
| ```tab_control```  | string  |
| ```tab_content```  | string  |

### Carousel Label (Unused/No Longer Works)

| Name                | Type
|---------------------|-------------
| ```always_rotate``` | boolean
| ```rotate_speed```  | number
| ```hover_color```   | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```
| ```hover_alpha```   | float (0.0 >= and <= 1.0) 
| ```pressed_color``` | Vector [red, green, blue] or ```white```, ```black```, ```yellow```, ```orange```, ```green```, ```purple```, ```nil```, ```cyan```, ```red```, ```grey```, ```gray``` or ```blue```
| ```pressed_alpha``` | float (0.0 >= and <= 1.0)


## Operations

### In Size/Offset/MaxSize/MinSize/Variables

\+ and -

### In Bindings

<, >, +, -, * and /