�����ˁI�J�E���^�[
====

�^�e���r�ԑg�́u�ց`�v�{�^���̂悤�Ȋ��o�ŁA�u�����ˁI�v�{�^����A�Ł��݂�Ȃŋ��L�o����c�[���ł��B  
LT��v���[���Ȃǂ𐷂�グ��̂ɖ𗧂�������܂���B

�Г��̂��傢�C�x���g�ŗ��p���邽�߂ɊJ�������c�[����heroku�̖����g�ŉғ�����O��ō���Ă��܂��B  
�V���O���C���X�^���X�ł̂ݓ��삷��̂�2x�Ƃ��ɂ���Ɛ���ɓ����܂���B
���̏����̃c�[���Ƃ��č���Ă���̂ł��قǒ��J�ɂ͍���Ă��܂���B

�N�����ăX�}�z�̃u���E�U�ŊJ���ƁA�ڑ����Ă���S���ł����ˁI�̐������L�ł��܂��B

WebSocket���g���Ă���̂�Android��4.4�ȍ~�̕W���u���E�U��Chrome���T�|�[�g���Ă܂��B  
iOS�͂��ƌÂ��o�[�W�����ł����삵�܂��B


## �g����

heroku�ɂ��̂܂܃f�v���C���ė��p���܂��B
�N������h���C����``example.herokuapp.com``�Ƃ��܂��B

### ���C�����
https://example.herokuapp.com/

���̉�ʂ��X�}�z�ŊJ���āA�݂�Ȃł����ˁI�������܂���܂��B

### ���j�^�[���
https://example.herokuapp.com/monitor.html

�v���[����ʂȂǂ̕Ћ��ɕ\�����Ă����ˁI���J�E���g�A�b�v�����l�q��\���ł��܂��B

### �J�E���^�[�̃��Z�b�g
https://example.herokuapp.com/admin.html

�p�X���[�h��``heroku config:set ADMIN_PW=1111``�̂悤�ɐ��p�X���[�h��ݒ肵�Ă��������B  
�N���e�B�J���ȃc�[���ł͂Ȃ����߃n�b�V�����Ȃǂ͂��Ă��܂���A���ŗ��p���Ă���p�X���[�h�̗��p�͔����Ă��������B

### �f�[�^�̕ۑ�
�I���������ŉғ�����A�v���Ȃ̂�heroku�ŃA�v���P�[�V�����T�[�o���ċN�����ꂽ��f�[�^������������Ă��܂��܂��B
������PostgreSQL��heroku�ɕR�t���Ă����΃�������̃f�[�^��5�b�����Ɏ����ۑ����čċN�����ɑO��̃f�[�^�������p���܂��B

``heroku addons:add heroku-postgresql:hobby-dev``�ŃA�v����DB��ǉ������玩���I��``DATABASE_URL``���ݒ肳��܂��B  
�ǉ����``heroku config:get DATABASE_URL``�Ő������ݒ肳��Ă��鎖���m�F���Ă��������B

�������ǉ��ł�����``heroku pg:psql``�Őڑ����ĉ��LDDL/DML�����s���Ă��������B
```
create table storage (
	key varchar(100) not null,
	value text,
	primary key (key)
);

insert into storage(key, value) values ('like_user', '{}');
```
