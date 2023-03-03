# Domanda 5 - Esercizio

Supponiamo di avere una classe, chiamata <code>AltenEntity</code>, così definita:

    public class AltenEntity
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public string Description { get; set; } 
    }

E supponiamo di aver invocato - *da qualche parte* - la seguente porzione di codice:

    modelBuilder.Entity<AltenEntity>(entity =>
    {
        entity.HasKey(x => x.Id);

        entity.HasIndex(entity => entity.Name)
              .IsUnique(true);

        entity.Property(x => x.Name)
              .HasMaxLength(30);

        entity.Property(x => x.Description)
              .HasMaxLength(100);
    });

>## Cosa fa il secondo snippet di codice?

&nbsp;

>## Scrivi un breve snippet di codice per inserire una istanza di <code>AltenEntity</code> nel database.

&nbsp;

Supponiamo ora di avere le seguenti due istanze di <code>AltenEntity</code> che abbiamo instanziato nel modo seguente e che desideriamo inserire nella base dati:

    AltenEntity entity_1 = new()
    {
        Id = 1,
        Name = "Arch Linux",
        Description = string.Empty        
    };
    
    AltenEntity entity_2 = new()
    {
        Id = 2,
        Name = "Arch Linux",
        Description = "A lightweight and flexible Linux distribution"        
    };

>## Usando lo snippet precedentemente creato, l'inserimento delle due suddette istanze va a buon fine? Come possiamo modificarlo per informare l'utente che qualcosa è andato storto?
