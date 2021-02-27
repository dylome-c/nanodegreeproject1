SELECT city, store_id, SUM(amount)
  FROM
  (SELECT r.rental_id, r.staff_id, st.store_id, a.address_id, c.city, p.amount
  FROM rental r
  JOIN payment p
  ON p.rental_id = r.rental_id
  JOIN staff s
  ON s.staff_id = r.staff_id
  JOIN store st
  ON st.store_id = s.store_id
  JOIN address a
  ON a.address_id = st.address_id
  JOIN city c
  ON a.city_id = c.city_id) sub
  GROUP BY 1,2
  ORDER BY 2;
