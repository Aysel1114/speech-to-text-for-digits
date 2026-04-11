# Spoken Digit Recognition (SDR) with CNN

### Problem
Səsli komandaların və rəqəmlərin avtomatik tanınması insan-kompüter interaksiyası və əlçatanlıq texnologiyaları üçün mühüm əhəmiyyət kəsb edir. Bu layihənin məqsədi audio fayllarındakı insan səsi ilə deyilmiş rəqəmləri (0-9) yüksək dəqiqliklə təsnif edə bilən dərin öyrənmə modeli hazırlamaqdır.

### Data
Layihədə **Free Spoken Digit Dataset (FSDD)** istifadə olunmuşdur. Dataset müxtəlif natiqlər tərəfindən səsləndirilmiş `.wav` formatlı rəqəmlərdən ibarətdir. Məlumat bazası fərqli səs tonları, vurğular və sürətlərdə tələffüz edilmiş minlərlə nümunəni ehtiva edir.

### Nə etdim
* **Data preprocessing:** Audio siqnalların oxunması, kənar küyün təmizlənməsi və səs dalğalarının vizuallaşdırılması.
* **Xüsusiyyətlərin çıxarılması:** Librosa kitabxanası vasitəsilə audio datadan MFCC (Mel-frequency cepstral coefficients) və spektroqramların əldə edilməsi.
* **CNN modeli ilə təsnifat:** Spektroqramları şəkil kimi emal edən çoxqatlı Konvolusiya Neyron Şəbəkəsinin (CNN) qurulması.
* **Modelin train və validation prosesi:** Məlumatların təlim və test dəstlərinə bölünməsi, modelin `EarlyStopping` metodundan istifadə edilərək öyrədilməsi.
* **Test və Qiymətləndirmə:** Modelin real səs nümunələri (məsələn: `Aysel_Voice.wav`) üzərində sınaqdan keçirilməsi və dəqiqlik göstəricilərinin analizi.

### Nəticə
Model səsli rəqəmləri uğurla tanıya bilir və yüksək təsnifat dəqiqliyi nümayiş etdirir. CNN arxitekturası səs spektroqramlarındakı tezlik modellərini effektiv şəkildə öyrənərək, fərqli natiqlərin səslərini belə düzgün rəqəmlərə çevirməyi bacarmışdır.

---

**İstifadə olunan əsas alətlər:** `TensorFlow/Keras`, `Librosa`, `NumPy`, `Matplotlib`.
