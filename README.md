# List_project
Work on flattening the list and reprinting it starting from the bottom.

1- Bir listeyi düzleştiren (flatten) fonksiyon tipi. Elemanları birden çok ışıklı listelerden ([[3],2] gibi) oluşabileceği gibi, non-skaler göstergelerden de görülebilir. Örnek olarak:

giriş: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

çıktı: [1,'a','cat',2,3,'dog',4,5]




list1 = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
flat_list = []
def flatten(l):
    for i in l:
        if type(i) == list:
            flatten(i)
        else:
            flat_list.append(i)
    return flat_list

print(flatten(list1))
