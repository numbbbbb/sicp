(define (even? x)
	(= (remainder x 2) 0)
)
(define (same-parity . a)
	(define (filter b even)
		(if (not (null? b))
			(
				cond
					(even (if (even? (car b)) (cons (car b) (filter (cdr b) even)) (filter (cdr b) even)))
					(else (if (not (even? (car b))) (cons (car b) (filter (cdr b) even)) (filter (cdr b) even)))
			)
			'()
		)
	)
	(cons (car a) (filter (cdr a) (even? (car a))))
)

(same-parity 2 3 4 5 6)