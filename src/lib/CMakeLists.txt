include(FetchContent)
add_library(searchableutils searchableutils.c)
target_include_directories(searchableutils PUBLIC "${CMAKE_SOURCE_DIR}/src/include")

FetchContent_Declare(
  qpdf
  GIT_REPOSITORY https://github.com/qpdf/qpdf.git
  GIT_TAG 09a36ad62bfa787642778b8076ae5b4ba4a64fcc
)

FetchContent_MakeAvailable(qpdf)

FetchContent_Declare(
  tesseract
  GIT_REPOSITORY https://github.com/tesseract-ocr/tesseract.git
  GIT_TAG 82a7a87b3bc159ef4607adea86100b3c09f406e8
)

FetchContent_MakeAvailable(tesseract)

FetchContent_Declare(
  imagemagick6
  GIT_REPOSITORY https://github.com/ImageMagick/ImageMagick6.git
  GIT_TAG 41d847bac6500b186c8944b6bb5b0fc3b9815d91
)

FetchContent_MakeAvailable(imagemagick6)

target_link_libraries(searchableutils qpdf tesseract imagemagick6)