default: tests.log

test:
	@../test.pl -p -c "python ../../../scripts/cpplint.py"

tests.log: ../test.pl
	@../test.pl -p -c "python ../../../scripts/cpplint.py"

show:
	@for dir in *; do \
		if [ -d "$$dir" ]; then \
			vim -o "$$dir/*.c" "$$dir/*.out"; \
		fi; \
	done;

clean:
	find -name '*.out' -execdir $(RM) '{}' \;
	find -name '*.gb' -execdir $(RM) '{}' \;
	$(RM) tests.log
