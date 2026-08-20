## Not so rare case - find something in JSONB

Examples:
2) WHERE slug = 'ready_for_theory_exam' AND data @> '{"theory_exam_registration_option": "scheduled_by_driving_school"}';
3) WHERE slug = 'ready_for_theory_exam' AND data->>'theory_exam_registration_option' = 'scheduled_by_driving_school';

---
Bad example

-- Bad
data >> '%"theory_exam_registration_option": "scheduled_by_driving_school"%'

format-sencetive
slow on big tables

