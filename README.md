
##### Library yang saya gunakan :
from IPython import display
from rembg import remove
from PIL import Image
import cv2 
from skimage.io import imread

penjelasan mengenai masing-masing baris kode:

from IPython import display: Baris ini mengimport modul display dari library IPython. Modul ini digunakan untuk menampilkan gambar di dalam notebook Jupyter.

from rembg import remove: Baris ini mengimport fungsi remove dari library rembg. Library rembg digunakan untuk melakukan penghapusan latar belakang (background removal) pada gambar dengan menggunakan model deep learning.

from PIL import Image: Baris ini mengimport modul Image dari library PIL (Python Imaging Library). Modul ini menyediakan berbagai fungsi untuk membaca, menulis, dan memanipulasi gambar dalam Python.

import cv2: Baris ini mengimport library cv2 (OpenCV) yang digunakan untuk operasi pengolahan gambar, termasuk manipulasi, deteksi objek, dan analisis gambar.

from skimage.io import imread: Baris ini mengimport fungsi imread dari library skimage.io. Fungsi ini digunakan untuk membaca gambar dari file

import matplotlib.pyplot as plt: Baris ini mengimport modul pyplot dari library matplotlib sebagai plt. Library matplotlib.pyplot digunakan untuk membuat plot grafik, histogram, dan visualisasi data lainnya.

%matplotlib inline: Baris ini adalah sebuah magic command dalam Jupyter Notebook yang memungkinkan hasil visualisasi dari matplotlib ditampilkan langsung di dalam notebook tanpa perlu menampilkan jendela plot terpisah. Ini berguna untuk membuat plot secara interaktif dan memastikan bahwa plot tersebut terlihat di dalam notebook.

with open(output_path, 'wb') as f:: Baris ini membuka file dengan nama output_path untuk ditulis ('wb' menunjukkan mode penulisan biner). Penggunaan with digunakan untuk memastikan bahwa file akan ditutup setelah selesai digunakan.

input_pict = open(input_path,'rb').read(): Baris ini membuka file gambar dari input_path dengan mode baca biner ('rb') dan membaca seluruh isinya menggunakan metode read(). File gambar tersebut kemudian disimpan dalam variabel input_pict.

subject = remove(input_pict): Baris ini menggunakan fungsi remove dari library rembg untuk menghapus latar belakang gambar yang ada dalam input_pict. Hasil penghapusan latar belakang disimpan dalam variabel subject.

f.write(subject): Baris ini menulis isi dari subject (gambar yang telah memiliki latar belakang dihapus) ke file yang sedang dibuka (output_path) menggunakan metode write().