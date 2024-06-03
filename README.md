# decision_tree_CART_heart_disease
# Rumusan masalah
# Bagaimana memprediksi serangan jantung berdasarkan:                                           
 1   sex                                             1025 non-null   int64  
 2   Chest Pain Type (CP)                            1025 non-null   int64  
 3   Resting Blood Pressure (trestbps)               1025 non-null   int64  
 4   Serum Cholestoral (chol) mg/dl                  1025 non-null   int64  
 5   Fasting Blood Sugar (fbs) > 120 mg/dl           1025 non-null   int64  
 6   Resting Electrocardiographic Results (restecg)  1025 non-null   int64  
 7   Maximum Heart Rate Achieved (thalach)           1025 non-null   int64  
 8   Exercise Induced Angina (exang)                 1025 non-null   int64  
 9   ST depression (oldpeak)                         1025 non-null   float64
 10  Slope of the ST Segment (slope)                 1025 non-null   int64  
 11  Number of Major Vessels (ca)                    1025 non-null   int64  
 12  Thal                                            1025 non-null   int64  
 13  target                                          1025 non-null   int64  

# tujuan
memprediksi serangan jantung menggunakan decision tree

#algoritma 
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
