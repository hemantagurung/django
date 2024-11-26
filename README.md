{% extends "base.html" %} {% block content %}
<div class="container">
  <h1>Update Book</h1>
  <hr />
  <a href="" class="btn btn-secondary">Back</a>
  <hr />
  <form method="post">
    {% csrf_token %}
    <div class="mb-3">
      <label for="name" class="form-label">Name</label>
      <input type="text" class="form-control" id="name" name="name" required />
    </div>
    <div class="mb-3">
      <label for="publication" class="form-label">Publication</label>
      <input
        type="text"
        class="form-control"
        id="publication"
        name="publication"
        required
      />
    </div>
    <div class="mb-3">
      <label for="price" class="form-label">Price</label>
      <input
        type="number"
        class="form-control"
        id="price"
        name="price"
        required
      />
    </div>
    <div class="mb-3">
      <label for="published_date" class="form-label">Published Date</label>
      <input
        type="date"
        class="form-control"
        id="published_date"
        name="published_date"
        required
      />
    </div>
    <div class="mb-3">
      <label for="slug" class="form-label">Slug</label>
      <input type="text" class="form-control" id="slug" name="slug" required />
    </div>
    <div class="mb-3">
      <label for="author_written" class="form-label">Author Written</label>
      <select name="author_written" id="" class="form-control form-select">
        {% for author in authors %}
        <option value="{{author.id}}">{{author.name}}</option>
        {% endfor %}
        {% comment %} <option value="1">Author 1</option>
        <option value="2">Author 2</option>
        <option value="3">Author 3</option> {% endcomment %}
      </select>
    </div>
    <div class="mb-3">
      <label for="author_edited" class="form-label">Author Edited</label>
      <select name="author_edited" id="" class="form-control form-select">
        {% for author in authors%}
        <option value="{{author.id}}">{{author.name}}</option>
        {% endfor %}

        
        {% comment %} <option value="1">Author 1</option>
        <option value="2">Author 2</option>
        <option value="3">Author 3</option> {% endcomment %}
      </select>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
</div>
{% endblock %}
