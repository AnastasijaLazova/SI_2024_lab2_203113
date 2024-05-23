# Анастасија Лазова, 203113

3. Цикломатската комплексност е 10. Пресметката ја направив преку предикатните јазли, односно има 7 if-else услови и 2 for услови, се додава плус 1: 9+1=10.
  
4. Тест 1: allItems е null
 allItems = null, payment = 100
Тест 2: allItems е празна листа
allItems = [], payment = 100
Тест 3: Item со празно име и валиден баркод без попуст
allItems = [new Item("","1234",100,0)], payment = 100
Тест 4: Item со валидно име и невалиден баркод
allItems = [new Item("Item1","1gfg245",100,0)], payment = 100
Тест 5: Item со валиден баркод и попуст
allItems = [new Item("Item1","1234",200,0.2)], payment = 150
Тест 6: Item без баркод
allItems = [new Item("Item1",null,100,0)], payment = 100
Тест 7: Item со цена над 300, попуст и баркод што започнува со '0'
allItems = [new Item("Item1","01234",310,0.1)], payment = 350
Тест 8: Вкупната сума е поголема од payment
allItems = [new Item("Item1","1234",110,0)], payment = 100

5. 8 комбинации
1. true, true, true
item = new Item("Item1", "0123", 350, 0.1), payment = 320

2. true, true, false
item = new Item("Item1", "1123", 350, 0.1), payment = 345

3. true, false, true
item = new Item("Item1", "0123", 350, 0), payment = 350

4. true, false, false
item = new Item("Item1", "1123", 350, 0), payment = 350

5. false, true, true
item = new Item("Item1", "0123", 250, 0.1), payment = 225

6. false, true, false
item = new Item("Item1", "1123", 250, 0.1), payment = 225

7. false, false, true
item = new Item("Item1", "0123", 250, 0), payment = 250

8. false, false, false
item = new Item("Item1", "1123", 250, 0), payment = 250
