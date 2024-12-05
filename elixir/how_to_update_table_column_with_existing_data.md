## Float to integer with a lot of existing data


Here is my example of Ecto migration
```
defmodule Simulators.Repo.Migrations.ConvertScoresToIntegers do
  use Ecto.Migration

  def up do
    # Add new integer columns
    alter table(:user_exercise_reports) do
      add :score_integer, :integer
    end

    alter table(:user_completed_exercises) do
      add :score_integer, :integer
    end

    alter table(:user_exercise_progresses) do
      add :best_score_integer, :integer
    end

    # Convert existing float scores to integers
    execute """
    UPDATE user_exercise_reports 
    SET score_integer = ROUND(score)::integer 
    WHERE score IS NOT NULL
    """

    execute """
    UPDATE user_completed_exercises 
    SET score_integer = ROUND(score)::integer 
    WHERE score IS NOT NULL
    """

    execute """
    UPDATE user_exercise_progresses 
    SET best_score_integer = ROUND(best_score)::integer 
    WHERE best_score IS NOT NULL
    """

    # Drop float columns and rename integer columns
    alter table(:user_exercise_reports) do
      remove :score
    end
    rename table(:user_exercise_reports), :score_integer, to: :score

    alter table(:user_completed_exercises) do
      remove :score
    end
    rename table(:user_completed_exercises), :score_integer, to: :score

    alter table(:user_exercise_progresses) do
      remove :best_score
    end
    rename table(:user_exercise_progresses), :best_score_integer, to: :best_score
  end

  def down do
    # Add float columns back
    alter table(:user_exercise_reports) do
      add :score_float, :float
    end

    alter table(:user_completed_exercises) do
      add :score_float, :float
    end

    alter table(:user_exercise_progresses) do
      add :best_score_float, :float
    end

    # Convert integers back to floats
    execute """
    UPDATE user_exercise_reports 
    SET score_float = score::float 
    WHERE score IS NOT NULL
    """

    execute """
    UPDATE user_completed_exercises 
    SET score_float = score::float 
    WHERE score IS NOT NULL
    """

    execute """
    UPDATE user_exercise_progresses 
    SET best_score_float = best_score::float 
    WHERE best_score IS NOT NULL
    """

    # Drop integer columns and rename float columns
    alter table(:user_exercise_reports) do
      remove :score
    end
    rename table(:user_exercise_reports), :score_float, to: :score

    alter table(:user_completed_exercises) do
      remove :score
    end
    rename table(:user_completed_exercises), :score_float, to: :score

    alter table(:user_exercise_progresses) do
      remove :best_score
    end
    rename table(:user_exercise_progresses), :best_score_float, to: :best_score
  end
end

```
