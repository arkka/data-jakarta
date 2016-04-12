# DATA JAKARTA

Jakarta curated datasets (with small data cleaning).

### Administrative Area
###### Datasets: [administrative-area.csv](/.datasets/DATA-DKI-MENURUT-NOMOR-KODE-WILAYAH-TAHUN-2014.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/datadkimenurutnomorkodewilayah/resource/79acba1a-0f0f-4323-a6b4-f0fae0967ab7)
###### Fields:
| Fields | Column Name |
|--------| ----------- |
| year | `tahun` |
| province id | nomor_provice |
| province name | nama_province |
| regency id | nomor_kabupaten |
| regency name | nama_kabupaten |
| district id | nomor_kecamatan |
| district name | nama_kecamatan |
| village id | nomor_kelurahan |
| village name | nama_kelurahan |

###### Level Structure

DKI Jakarta: Province
|-- Jakarta Pusat: Regency
|   +-- Setiabudi: District
|   |   +--- Guntur: Village

