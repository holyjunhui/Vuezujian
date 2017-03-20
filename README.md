# Vuezujian---如果在Google显示
```
[Vue warn]: Error compiling template:


            <table>
                <thead>
                    <tr>
                        <th v-for="col in columns">
                            {{ col | capitalize}}
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="entry in data | filterBy filterKey">
                        <td v-for="col in columns">
                            {{entry[col]}}
                        </td>
                    </tr>
                </tbody>
            </table>
        

- invalid expression: v-for="entry in data | filterBy filterKey"
 
(found in <SimpleGrid>)
```
很大一部分原因是因为导入的cdn不准确导致，建议导入
```
<script>http://cdn.jsdelivr.net/vue/1.0.7/vue.min.js</script>
<script>http://cdnjs.cloudflare.com/ajax/libs/vue/1.0.7/vue.min.js</script>
```
其中的任意一个即可。
