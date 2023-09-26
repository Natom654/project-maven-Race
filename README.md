# project-maven-Race
project-maven-template
Завдання: зробити JAR-файл із грою на JavaFX за допомогою графічного рушія JavaRush.
Для цього потрібно:

Зробити fork із репозиторію https://github.com/vasylmalik/project-maven.git.
Завантажити свою версію проєкту на комп'ютер. Далі будемо працювати з файлом pom.xml.
Додати залежності:
org.apache.commons: commons-lang3: 3.12.0
org.openjfx: javafx-controls: 18.0.1
com.javarush: desktop-game-engine:1.0 (стосовно цієї залежності буде окреме завдання)
org.junit.jupiter: junit-jupiter-engine: 5.8.2 (зі scope test)
Додати плагіни для:
установлення залежності com.javarush: desktop-game-engine:1.0 з бібліотеки lib до локального репозиторію (додаткову інформацію радимо пошукати через Google);
плагін maven-compiler-plugin залишити без змін;
плагін, який збере всі залежності (зі scope compile) та розмістить в якусь директорію при складанні;
плагін maven-jar-plugin, який зробить jar файл, що містить код гри та залежності. У цьому плагіні необхідно налаштувати файл MANIFEST.MF, щоб він містив секції: Class-Path, Main-Class і Rsrc-Main-Class
У Class-Path мають бути прописані всі наші JAR-залежності.
У Main-Class має бути прописаний клас org.eclipse.jdt.internal.jarinjarloader.JarRsrcLoader, який вміє використовувати classpath із JAR-файлів, а також вміє стартувати програму на JavaFX.
У Rsrc-Main-Class має бути прописаний стартовий клас гри (com.javarush.games.racer.RacerGame).
У плагіні maven-surefire-plugin створити конфігурацію, щоб тест StrangeTest не запускався при складанні. Інші тести повинні виконуватися.
Додати секцію “resources”, у якій вказати, що зібрані JAR-залежності – це ресурс, щоб плагін maven-jar-plugin склав їх усередину JAR-файлу в папці lib/.
Залити зміни до свого GitHub-репозиторію, надіслати посилання на нього викладачеві.
