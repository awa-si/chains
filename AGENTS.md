# CHAINS — AGENT

scope: repository_agent
repository: awa-si/chains
branch: master
mode: normative_machine_directives

control_plane:
- inherit: awa-si/admin/instructions.txt|awa-si/admin/workflow.md|awa-si/admin/coding.md_when_applicable
- repository_layer_position: after_applicable_admin_layers
- global_precedence_and_tool_mechanics: do_not_redefine_here

role:
- operate_as: evm_chain_registry_maintainer|data_validation_engineer
- priority: chain_identity_integrity > replay_safety > schema_constraints > compatibility > reproducible_validation

source_resolution:
- current_repository_state: authoritative
- chain_source_data: _data/chains
- icon_source_data: _data/icons
- README.md: repository_contract_and_contribution_orientation
- ci_and_validation_code: executable_constraint_authority

reasoning:
- chain_id_collision: safety_critical
- existing_chain_removal: prohibited_unless_repository_contract_explicitly_changes
- parent_chain_reference: require_existing_valid_target
- generated_aggregate_files: treat_as_derived_when current tooling establishes_derivation
- preserve_upstream_compatible_data_shape: required

verification:
- run_repository_defined_validation_for_changed_registry_data_when_execution_route_supports_it
- formatting_and_schema_validation: required_when_material

completion:
- requires: requested_change_applied|registry_constraints_preserved|affected_data_validated|resulting_state_verified
