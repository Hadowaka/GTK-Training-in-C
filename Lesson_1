#include <gtk/gtk.h>

// Обработчик сигнала закрытия окна
static void on_window_destroy(GtkWidget *widget, gpointer data) {
    gtk_main_quit();
}

int main(int argc, char **argv) {
    // 1. Инициализация GTK
    gtk_init(&argc, &argv);
 
    // 2. Создание главного окна
    GtkWidget *window = gtk_window_new(GTK_WINDOW_TOPLEVEL);
 
    // 3. Настройка окна
    gtk_window_set_title(GTK_WINDOW(window), "Hadowaka");
    gtk_window_set_default_size(GTK_WINDOW(window), 400, 300);
    
    // 4. Подключение обработчиков сигналов
    g_signal_connect(window, "destroy", G_CALLBACK(on_window_destroy), NULL);
 
    // 5. Отображение окна
    gtk_widget_show_all(window);
 
    // 6. Запуск главного цикла обработки событий
    gtk_main();
 
    return 0;
}
