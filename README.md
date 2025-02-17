# Wedding Me (backend)

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
    ALBUM ||--|{ GROUP : haves
    ALBUM {
        int id PK
        string title
        bool visible
		
        int user_id FK       
    }
	GROUP {
        int id PK
        string title
        bool visible
        int album_id FK       
	}
	ALBUM |o--|{ PHOTO : haves
	GROUP |o--|{ PHOTO : haves
    PHOTO {
        int id PK
        date created_at
        string title "O"
        string name "O"
        string path
        
        int group_id FK
        int album_id FK
    }	
    USER |o--|{ PAYMENT : pays_for    
	PAYMENT {
        int id PK
        date created_at
		string title
        int user_id FK       
	}
    USER  |o--|{ COMMENT : write
    PHOTO |o--|{ COMMENT : haves    
	COMMENT {
		int id
		date created_at
		string text
		
        int user_id FK       
        int photo_id FK       
	}
```

## Ссылки
_____

[ТЗ](https://docs.google.com/document/d/1KUIepvxzV8rNgzTm7u0jYfLznHQ3HfmMgL96vpWOmVI/edit?usp=sharing)
[Figma](https://www.figma.com/design/GUCHADxOs7yYZwBgSe3hOY/photo-albums-(Community)?node-id=0-1&p=f&t=I31a5huFJsgkvldO-0)

## Команда
[Кирейбаев Куаныш](https://github.com/Yamemik)
[Козлов Евгений](https://github.com/GRIZLI-RGB)