  <Tabs value={tab} onValueChange={setTab} className="flex-1">
    <TabsList className="flex justify-around bg-white shadow">
      <TabsTrigger value="home">Home</TabsTrigger>
      <TabsTrigger value="menu">Menu</TabsTrigger>
      <TabsTrigger value="thanksgiving">Thanksgiving</TabsTrigger>
    </TabsList>

    <TabsContent value="home" className="p-4 space-y-4">
      <h1 className="text-3xl font-bold">Jackson Street Provisions</h1>
      <p className="text-sm">
        Downtown Roseburg, OR<br />
        Wed–Fri 11–3 • Sat 11–1
      </p>
      <Button asChild>
        <a href="tel:5416712375">Call to Order</a>
      </Button>
    </TabsContent>

    <TabsContent value="menu" className="p-4 space-y-4 overflow-y-auto">
      {sandwiches.map((s, i) => (
        <Card key={i} className="overflow-hidden shadow-lg">
          <img src={s.img} alt={s.name} className="w-full object-cover" />
          <CardHeader>
            <CardTitle className="text-orange-700">{s.name}</CardTitle>
          </CardHeader>
          <CardContent>
            <p className="text-sm">{s.desc}</p>
          </CardContent>
        </Card>
      ))}
    </TabsContent>

    <TabsContent value="thanksgiving" className="p-4 space-y-4">
      <Card>
        <CardHeader>
          <CardTitle>Smoked Turkey Holiday Dinner — $200</CardTitle>
        </CardHeader>
        <CardContent className="text-sm text-left">
          <ul className="list-disc pl-6">
            <li>One 14–16 lb smoked turkey</li>
            <li>65.6 oz mashed potatoes</li>
            <li>32 oz gravy</li>
            <li>16 oz cranberry sauce</li>
            <li>Additional 65.6 oz side</li>
            <li>Add a dessert below!</li>
          </ul>
        </CardContent>
      </Card>

      <Card>
        <CardHeader>
          <CardTitle>Holiday Desserts</CardTitle>
        </CardHeader>
        <CardContent className="text-sm text-left">
          <ul className="list-disc pl-6">
            {desserts.map((d, i) => (
              <li key={i}>{d}</li>
            ))}
          </ul>
        </CardContent>
      </Card>
    </TabsContent>
  </Tabs>

  <footer className="p-3 text-xs text-neutral-600 bg-white/70">
    © {new Date().getFullYear()} Jackson Street Provisions
  </footer>
</div>
# Taterbug
Jsp menu apo
