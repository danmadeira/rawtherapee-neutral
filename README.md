## Perfil de processamento neutro para RawTherapee

Um arquivo de perfil de processamento (.pp3) que contém todas as configurações neutralizadas.

Os perfis de processamento são arquivos de texto que contêm todas as configurações que o RawTherapee aplica à foto associada. Se você estiver familiarizado com outros editores de arquivos RAW, talvez conheça o equivalente deles como "presets".

Estes arquivos podem ser utilizados tanto na versão gráfica como na versão para linha de comando do RawTherapee. A edição direta do arquivo no modo texto supre a necessidade de executar o RawTherapee pela linha de comando.

Os valores dos parâmetros de configuração estão na posição neutra, sem qualquer efeito na imagem crua.

### Alguns parâmetros com os valores mínimos e máximos:

\[Exposure\]
Compensation = -5 .. 0 .. 12
Brightness = -100 .. 0 .. 100
Contrast = -100 .. 0 .. 100
Saturation = -100 .. 0 .. 100
Black = -16384 .. 0 .. 32768
HighlightCompr = 0 .. 500

\[Sharpening\]
Enabled = true
Radius = 0.3 .. 0.5 .. 3
Amount = 1 .. 200 .. 1000

\[Vibrance\]
Enabled = true
Pastels = -100 .. 0 .. 100
Saturated = -100 .. 0 .. 100

\[White Balance\]
Enabled = true
Setting = Custom
Temperature = 1500 .. 6504 .. 60000

\[Directional Pyramid Denoising\]
Enabled = true
Luma = 0 .. 100
Ldetail = 0 .. 100
MethodMed = Lonly

\[EPD\]
Enabled = true
Strength = -1 .. 0.5 .. 2

\[Shadows & Highlights\]
Enabled = true
Highlights = 0 .. 100
HighlightTonalWidth = 10 .. 70 .. 100
Shadows = 0 .. 100
ShadowTonalWidth = 10 .. 30 .. 100

\[Crop\]
Enabled = true
X = 0
Y = 0
W = 6016
H = 4014

### Exemplos de linha de comandos para o RawTherapee CLI:

rawtherapee-cli -o IMG_0123.tif -p profile.pp3 -s -b8 -t -c IMG_0123.CR2

rawtherapee-cli -o IMG_0123.jpg -p profile.pp3 -s -j95 -c IMG_0123.CR2

### Referências:

- RawTherapee Command-Line Options. December 9 2019. Disponível em: <https://rawpedia.rawtherapee.com/Command-Line_Options>

- RawPedia. The encyclopedia of RawTherapee, raw shooting and everything raw. July 6, 2020. Disponível em: <https://rawpedia.rawtherapee.com/Main_Page>
