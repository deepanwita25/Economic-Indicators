```SQL
CREATE DATABASE IMF
```

```SQL
CREATE TABLE imf.`economic_indicators`(
	`id` INT AUTO_INCREMENT PRIMARY KEY,
    `country` VARCHAR(10) NOT NULL,
    `year` INT NOT NULL,
    `value` DECIMAL(15,3) NOT NULL,
    `unit` VARCHAR(50) NOT NULL,
    `economic_indicator` VARCHAR(100) NOT NULL,
    `source` VARCHAR(50) NOT NULL,
    `updated_at` timestamp DEFAULT current_timestamp
		ON UPDATE current_timestamp,
	CONSTRAINT `unique_key` UNIQUE(`country`, `year`, `unit`, `economic_indicator`)
)
ENGINE = InnoDB
DEFAULT CHARSET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;
```

```SQL
	CREATE TABLE IF NOT EXISTS `imf`.`country_code`(
	`id` int auto_increment PRIMARY KEY,
    `country_name` varchar(100) NOT NULL,
    `iso_code_2` varchar(3) NOT NULL,
    `iso_code_3` varchar(4) NOT NULL,
    CONSTRAINT `unique_country_code` UNIQUE (`country_name`)
    )
ENGINE = InnoDB
DEFAULT CHARSET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;
```
	
