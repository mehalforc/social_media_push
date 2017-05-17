<?php

function social_media_push_get_terms($node) {
  $terms = array();

  foreach (field_info_instances('node', $node->type) as $fieldname => $info) {
    foreach (field_get_items('node', $node, $fieldname) as $item) {
      if (is_array($item) && !empty($item['tid']) && $term = taxonomy_term_load($item['tid'])) {
        $terms[] = $term->name;
      }
    }
  }
  return $terms;
}