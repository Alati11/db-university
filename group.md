1. Contare quanti iscritti ci sono stati ogni anno
    - SELECT COUNT(*) as `nunero_studenti_anno`, `students`.`enrolment_date` FROM `students` INNER JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id` INNER JOIN `courses` ON `courses`.`degree_id` = `degrees`.`id` GROUP BY `students`.`enrolment_date`;

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
    - SELECT COUNT(*) as `num_teachers`, `office_address` FROM `teachers` GROUP BY `teachers`.`office_address`;

3. Calcolare la media dei voti di ogni appello d'esame
    - SELECT AVG (`vote`) as `media`, `exam_id` FROM `exam_student` GROUP BY `exam_id`;

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
    - SELECT COUNT(*) as `number_of_degrees`, `department_id` FROM `degrees` GROUP BY `department_id`;