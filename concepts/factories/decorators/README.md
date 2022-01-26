# Decorators

> In object-oriented programming, the decorator pattern is a design pattern that allows behavior to be added to an individual object, dynamically, without affecting the behavior of other objects from the same class. The decorator pattern is often useful for adhering to the Single Responsibility Principle, as it allows functionality to be divided between classes with unique areas of concern. Decorator use can be more efficient than subclassing, because an object's behavior can be augmented without defining an entirely new object. (↪[wiki](https://en.wikipedia.org/wiki/Decorator\_pattern))

A factory alone may not be enough to generate complex data. For this reason, a special kind of factory, also known as decorators introduced. At this moment, FluentFixture provides nine decorators listed below.

<table>
   <thead>
      <tr>
         <th>Name</th>
         <th>Behavior</th>
         <th data-type="checkbox">Deterministic</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><a href="functional.md"><code>Functional</code></a></td>
         <td><code>modifier</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="nullable.md"><code>Nullable</code></a></td>
         <td><code>conditional</code></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="optional.md"><code>Optional</code></a></td>
         <td><code>conditional</code></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="iterator.md"><code>Iterator</code></a></td>
         <td><code>modifier</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="formatter.md"><code>Formatter</code></a></td>
         <td><code>modifier</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="exporter.md"><code>Exporter</code></a></td>
         <td><code>utility</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="memo.md"><code>Memo</code></a></td>
         <td><code>utility</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="lazy.md"><code>Lazy</code></a></td>
         <td><code>modifier</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="property.md"><code>Property</code></a></td>
         <td><code>modifier</code></td>
         <td>true</td>
      </tr>
   </tbody>
</table>
