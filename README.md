# spring-boot-project

JDBC
~~~java
public class CategoryDAO{
  private Connection connection;
  
  
  public CategoryDAO(){
    this.connection = new ConncetionFactory().getConnection()
  }
  
public void insert(Category category) throws SQL Exception {
  String sql = "Insert into category(name, active) values (?, ?)";
  PreparedStatment stmt = this.connection.prepareStatemetn(sql);
  stmt.setString(1, category.getName());
  stmt.execute();
  stmt.close();
  }
}
~~~

JPA

~~~java
public class CategoryDAO {
 @PersistenceContext
 private EntityManager entityManager;
 
 public void insere(Category category) {
 entityManager.persist(category)
 }
}
~~~



<img width="894" alt="Captura de Tela 2023-04-28 às 00 34 53" src="https://user-images.githubusercontent.com/79465402/235050410-59b41e6e-3e51-486b-adec-7626111db889.png">
