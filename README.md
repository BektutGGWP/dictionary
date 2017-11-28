# dictionary

print("Здравстуйте, мы предствляем вам англо-русский словарь. Здесь вы можете добавлять слова, а также устраивать себе проверку :) ")
while True:
  dic = {"apple": "яблоко",
        "banana": "банан",
        "vegitable": "овощ",
        "spoon": "ложка",
        "love": "любовь"}
  
  # добавление
  def add(new_e, new_r):
  
    ne = new_e.lower()
    nr = new_r.lower()
    dic[ne] = nr
    dic.update()
    for key in dic:
      print(key, dic[key])
  #  проверка 
  l = len(dic)
  def test():
    points = []
    for i in dic:
      print(i)
      translate = input("give translation: ")
      if dic[i] == translate:
        print("correct")
        points.append(10)
      else:
        print("wrong")
        points.append(-5)
  
    print(points)
    i = 0     
    total = 0
    while i != l:
      total = total + points[i]
      i += 1
      
    print("You have: ", total, "points from 50")

  print("*"*50)
  do = int(input("\n\n\nВыберите действие: \nДОВБАРИТЬ СЛОВО(1)\nПРОВЕРИТЬ СЕБЯ(2)\nВЫЙТИ(3)\n --->"))
  
  
  if do == 1:
    add(input("Введите английское слово: "), input("Введиет слово на русском"))
  if do == 2:
    test()
  if do == 3:
    break
