24.12.21  21.44  
tags: [[react]] [[web]] [[frontend]] [[js]]


# react key
- must be unique
- we use it when using map/reduce/filter [[Javascript ES6 Map,Filter,Reduce]] , that loop through stuff.
```js
{emojipedia.map((emojiTerm) => (
          <Entry
            key={emojiTerm.id}
            emoji={emojiTerm.emoji}
            name={emojiTerm.name}
            description={emojiTerm.meaning}
          />
        ))}
```



# Reference
[[The Complete 2023 Web Development Bootcamp]]
