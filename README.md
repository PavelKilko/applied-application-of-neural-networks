# Applied application of neural networks

function create_train_test_datasets(font_paths):
  init empty train_dataset
  init empty test_dataset

  for each font_path in font_paths:
    load dataset from font_path
      delete columns 'fontVariant', 
            'm_label', 
            'strength', 
            'italic', 
            'orientation', 
            'm_top',
            'm_left',
            'originalH',
            'originalW',
            'h',
            'w'
            from dataset
      make sample with 950 random rows from dataset
      split sample into train and test samples using 80:20 ratio
      add train_sample into train_dataset
      add test_sample into test dataset

  return train_dataset and test_dataset
      
