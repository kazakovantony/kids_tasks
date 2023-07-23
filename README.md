import telebot

bot = telebot.TeleBot('j')

@bot.message_handler(commands=["start"])
def main(messege):
    bot.send_message( messege.chat.id, 'Привет я бот' )

@bot.message_handler(commands=["Привет"])
def main(messege):
    bot.send_message( messege.chat.id, 'Привет я бот' )

@bot.message_handler(commands=["как дела"])
def main(messege):
    bot.send_message( messege.chat.id, 'хорошо' )

@bot.message_handler(commands=["что-ты любишь"])
def main(messege):
    bot.send_message( messege.chat.id, 'электричество' )

@bot.message_handler(commands=["help"])
def main(messege):
    bot.send_message( messege.chat.id, 'вот что я могу:как дела,Привет,что-ты любишь' )

bot.polling(none_stop=True)
