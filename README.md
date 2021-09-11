# Kint
To use:
<?php
  \Kint\Kint::dump($datas);
#resoult:

  * Ex1:
    $addresses array (1)
    ⇄⧉0 => array (4)
    ⇄⧉0 => Magento\Customer\Model\Data\Address (5)
    ⇄⧉1 => Magento\Customer\Model\Data\Address (5)
    ⇄⧉2 => Magento\Customer\Model\Data\Address (5)
    ⇄⧉3 => Magento\Customer\Model\Data\Address (5)

  * Ex2:
    $addresses array (1)
    ⇄⧉0 => Magento\Customer\Model\Data\Address (5)

# Nếu kết quả là 1 array chứa cá lớp Magento\Customer\Model\Data\Address :
      + foreach sau đó tìm vào trong lớp để gọi hàm data:
            foreach ($addresses as $address){
                \Kint\Kint::dump($address->getExtensionAttributes()->setAddressName('addressName'));
            }
# Nếu kết quả là các lớp vd: Magento\Customer\Model\Data\Address:
      + chỉ cần tìm vào trong lớp và gọi data.
