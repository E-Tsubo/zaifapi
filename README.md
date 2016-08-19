zaifapi
======================
zaif�����J���Ă���API���ȒP�ɌĂׂ�p�ɂ��܂����B
�����p�͎��ȐӔC�ł����R�ɂǂ���

�g����
------
�P�Dpip�R�}���h�����s���A���W���[�����_�E�����[�h���Ă�������

    pip install zaifapi

�Q�D�N���X���C���|�[�g���A���L��̗p�Ɏg�p���Ă�������

    from zaifapi.impl import ZaifPublicApi, ZaifPrivateApi
    zaif = ZaifPublicApi()
    print(zaif.last_price('btc_jpy'))
    
    zaif = ZaifPrivateApi(key, secret)
    print(zaif.get_info())


�@�\�Љ�
------
### ZaifPublicApi
#### Zaif�����J���Ă���F�؏�񂪗v��Ȃ�API�����s����N���X�ł�
***
last_price(currency_pair):�I�l���擾

ticker(currency_pair):�e�B�b�J�[

trades(currency_pair):�S�Ă̎������

depth(currency_pair):���

streaming(currency_pair):websocket�𗘗p�������A���^�C�����ƏI�l

| ���O | �K�{ | ���� | �f�t�H���g�l | 
|:-----------|:------------:|:-----------|:-----------| 
| currency_pair | �� | �擾����ʉ݃y�A | - | 
�߂�l�Fjson

currency_pair��btc_jpy�Axem_jpy�Amona_jpy�Amona_btc���w��\�ł�

�ڍׂ͉��L�Q�l���䗗���������B
[�Q�l](https://corp.zaif.jp/api-docs/)
***

### ZaifPrivateApi
#### Zaif�����J���Ă���F�؏�񂪕K�v��API�����s����N���X�ł�
***
�C���X�^���X�������ɁAzaif�Ŕ��s�o����key��secret�̕�������w�肵�Ă��������B
���̍ہA�����ݒ�ɂ����ӂ��������B

���s�o���郁�\�b�h����p�����[�^�͉��L�Q�l�y�[�W���̂܂܂Ȃ̂ŁA�������������������B

�������Afrom�p�����[�^��from_num�Ǝw�肵�Ă��������B

�߂�l�͂��ׂ�json�ƂȂ��Ă��܂��B

[�Q�l](https://corp.zaif.jp/api-docs/trade-api/)
***
  
�֘A���
--------
1. [�O�O���J�X(�u���O)](http://gugurekasu.blogspot.jp/)
2. [LinkedIn](https://jp.linkedin.com/in/akirataniguchi1)
 
���C�Z���X
----------
Distributed under the [MIT License][mit].
[MIT]: http://www.opensource.org/licenses/mit-license.php
