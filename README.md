# Wedding Me

![Static Badge](https://img.shields.io/badge/Team2-WeddingMe-template)
![GitHub top language](https://img.shields.io/github/languages/top/GRIZLI-RGB/wedding-me)
![GitHub](https://img.shields.io/github/license/GRIZLI-RGB/wedding-me)
![GitHub Repo stars](https://img.shields.io/github/stars/GRIZLI-RGB/wedding-me)
![GitHub issues](https://img.shields.io/github/issues/GRIZLI-RGB/wedding-me)


## Общее описание
_____

### Стек технологий:
  - nestjs;
  - postgreSQL;
  - reactjs;
  - flutter.


## Техническое описание
_____

### ER-Diagrams
```mermaid
erDiagram
    USER ||--|{ ALBUM : makes    
    USER {
        int id PK
        date created_at
        string email
        string password
        string surname                
        string name                
        string patr "O"
		
        bool is_admin
    }
    ALBUM {
        int id PK
        string title
        bool visible
		
        int user_id FK       
    }
	ALBUM |o--|{ PHOTO : haves
    PHOTO {
        int id PK
        date created_at
        string title "O"
        string name "O"
        string path
        bool visible
        
        int album_id FK
    }	
    USER |o--|{ PAYMENT : pays_for    
	PAYMENT {
        int id PK
        date created_at
		string title
        int user_id FK       
	}
    USER  |o--|{ LIKE : puts
    PHOTO |o--|{ LIKE : receives    
	LIKE {
		int id PK
		date created_at
				
        int user_id FK       
        int photo_id FK       
    }
```

## Ссылки
_____

[ТЗ](https://docs.google.com/document/d/1KUIepvxzV8rNgzTm7u0jYfLznHQ3HfmMgL96vpWOmVI/edit?usp=sharing)
[Figma](https://www.figma.com/design/7GnydB44IgckzLZvSFkppi/WeddingMe?node-id=58-3&p=f&t=TThJI0oJG8TSWvPJ-0)

## Команда
[Кирейбаев Куаныш](https://github.com/Yamemik)
[Козлов Евгений](https://github.com/GRIZLI-RGB)
