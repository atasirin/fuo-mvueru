# client (istemci) değişkeniyle bir bot oluşturalım ve ayrıcalıkları ona aktaralım
client = discord.Client(intents=intents)
def sifre_bul(uzunluk=7):
    karakterler = "adamadam"
    sifre = ""

    for i in range(uzunluk):
        sifre += random.choice(karakterler)

    return sifre

@client.event
async def on_ready():
    print(f'We have logged in as {client.user}')

@client.event
async def on_message(message):
    if message.author == client.user:
        return
    if message.content.startswith('neraba'):
        await message.channel.send("hello!")
    elif message.content.startswith('göruşuruz'):
        await message.channel.send("good bye")
    elif message.content.startswith('şifreadam'):
        await message.channel.send(sifre_bul())
    elif message.content.startswith('\U0001F480'):
        await message.channel.send(":skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull::skull:")














































client.run(token)







