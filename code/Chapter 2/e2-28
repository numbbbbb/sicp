(define (fringe items)
	(cond ((null? items) '())
				((pair? (car items)) (append (fringe (car items)) (fringe (cdr items))))
				(else (cons (car items) (fringe (cdr items))))

	)
)

(define x (list (list 1 2) (list 3 4))) 

(fringe x)

(fringe (list x x))
