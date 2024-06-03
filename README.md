# decision_tree_CART_heart_disease
# Rumusan masalah
Bagaimana memprediksi serangan jantung berdasarkan:                                           
1. age
2. sex
3. chest pain type (4 values)
4. resting blood pressure
5. serum cholestoral in mg/dl
6. fasting blood sugar > 120 mg/dl
7. resting electrocardiographic results (values 0,1,2)
8. maximum heart rate achieved
9. exercise induced angina
10. oldpeak = ST depression induced by exercise relative to rest
11. the slope of the peak exercise ST segment
12. number of major vessels (0-3) colored by flourosopy
13. thal: 0 = normal; 1 = fixed defect; 2 = reversable defect
The names and social security numbers of the patients were recently removed from the database, replaced with dummy values.                                         

# tujuan
memprediksi serangan jantung menggunakan decision tree

# algoritma 
CART
d = 0, endtree = 0 
Catatan(0) = 1, Node(1) = 0, Node(2) = 0 
sedangkan endtree < 1 
    jika Node(2 d -1) + Node(2 d ) + .... + Node(2 d+1 -2) = 2 - 2 d+1   
         endtree = 1 
    else 
        do i = 2 d -1, 2 d , .... , 2 d+1 -2 
            if Node(i) > - 1 
                Pisahkan pohon 
            else 
                Node(2i+1) = -1 
                Node(2i+2) = -1 
            end if 
        end do 
    end if 
d = d + 1 
end while
