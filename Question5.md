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
              .HasMaxLength(100);

        entity.Property(x => x.Description)
              .HasMaxLength(100);
    });

>## Cosa fa il secondo snippet di codice?

&nbsp;

>## Scrivi un breve snippet di codice per inserire una istanza di <code>AltenEntity</code> nel database.
