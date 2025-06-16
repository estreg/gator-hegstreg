# Gator

## Disclaimer and Motivation:
I built this sort of multi-player command line tool (for aggregating RSS feeds and viewing the posts) with the help of boot.dev's guided course. So this is a pratice Project. To be honest, without the solution files, it would've taken significantly longer. But I do think I learned quite a bit, and I'll always be able to use this project as a reference. So, if you're looking to learn something with a project like this, I highly recommend boot.dev, even if the guidance was rather sparse, which was in the end a good thing.


## Quick Start

### Installation

Make sure you have the latest [Go toolchain](https://golang.org/dl/) installed as well as a local Postgres database. You can then install `gator` with:

```bash
go install ...
```

### Config

Create a `.gatorconfig.json` file in your home directory with the following structure:

```json
{
  "db_url": "postgres://username:@localhost:5432/database?sslmode=disable"
}
```

Replace the values with your database connection string.

## Usage

Create a new user:

```bash
gator register <name>
```

Add a feed:

```bash
gator addfeed <url>
```

Start the aggregator:

```bash
gator agg 30s
```

View the posts:

```bash
gator browse [limit]
```

There are a few other commands you'll need as well:

- `gator login <name>` - Log in as a user that already exists
- `gator users` - List all users
- `gator feeds` - List all feeds
- `gator follow <url>` - Follow a feed that already exists in the database
- `gator unfollow <url>` - Unfollow a feed that already exists in the database

## 🤝 Contributing

Since this is a practice project, consider this section a bit of practice as well. :)
That said, I’m always happy if someone out there in the vastness of the internet stumbles upon this repo!
It’s a great chance for me to get some hands-on experience with pull requests and open source contributions.
Who knows — maybe this even turns into a small, fun little community project. 😉

### Clone the repo

```bash
git clone https://github.com/estreg/gator-hegstreg
cd gator-hegstreg
```

### Build the project

```bash
go build
```

### Run the project

```bash
./gator-hegstreg
```

### Submit a pull request

If you'd like to contribute, please fork the repository and open a pull request to the `main` branch.
Since I’m still learning and GitHub isn’t quite my second home yet, it might take me a little while to respond to your request.
Please don’t take it as a rejection — I’m just figuring things out as I go. 
