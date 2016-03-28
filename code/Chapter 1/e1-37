(define (cont-frac-recur n d k)
	(define (cont-frac-internal n d k now)
		(if (> now k) 
				0
				(/ (n now) (+ (d now) (cont-frac-internal n d k (+ now 1))))
		)
	)
	(cont-frac-internal n d k 1)
)

(cont-frac-recur (lambda (i) 1.0) (lambda (i) 1.0) 1000)

; above is recursive implement

(define (cont-frac-iter n d k)
	(define (cont-frac-internal n d k result)
		(if (= k 0) 
				result
				(cont-frac-internal n d (- k 1) (/ (n k) (+ (d k) result)))
		)
	)
	(cont-frac-internal n d k 0)
)

(cont-frac-iter (lambda (i) 1.0) (lambda (i) 1.0) 1000)