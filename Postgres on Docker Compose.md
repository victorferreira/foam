[[postgres]] on [[Docker]] compose

```yml
services:
	db:
		image: postgres:latest
	environment:
		POSTGRES_PASSWORD: postgres
	volumes:
		- data:/var/lib/postgresql/data
	ports:
		- "5432:5432"
```