# ベースイメージの指定
FROM openjdk:17

# ワーキングディレクトリの設定
WORKDIR /app

# アプリケーションのJARファイルをコンテナにコピー
COPY batchmybookshelf.war app.jar

# ポートの公開
# EXPOSE 8080

ENV \
 SPRING_DATASOURCE_URL=jdbc:postgresql://postgres-container:5432/0912 \
 SPRING_DATASOURCE_USERNAME=postgres \
 SPRING_DATASOURCE_PASSWORD=password

# アプリケーションの実行コマンド
ENTRYPOINT ["java", "-jar", "app.jar"]
