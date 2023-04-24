# letterboxdHueSort

A utility that automatically sorts films in a letterboxd list by poster colour.
\
\
Given a CSV file that was generated by the Letterboxd exporter (or that fits Letterboxd's [import format](https://letterboxd.com/about/importing-data/)), the program
\
outputs an identical CSV file, except that films are sorted by the colour of their posters.

## Inspiration for the project

Inspiration for this project came from browsing a number of visually appealing, user-generated
\
film lists on [Letterboxd](https://letterboxd.com/), a popular film discovery website.
\
The lists in question often contain films in the hundreds, and even thousands.
\
Here are only a few of these publicly available lists:

- [Movie posters sorted by color](https://letterboxd.com/sprudelheinz/list/movie-posters-sorted-by-color/) by Sprudelheinz
- [Horror Movie Posters Organized by Color](https://letterboxd.com/cwspnn/list/horror-movie-posters-organized-by-color-1/) by  fanny 🕷
- [My Favorite Films (Sorted by Color*)](https://letterboxd.com/cinemacardboard/list/my-favorite-films-sorted-by-color/) by  Cinematic Cardboard
- [my favorite movies but organized by color](https://letterboxd.com/rachel_remeny/list/my-favorite-movies-but-organized-by-color/) by  rachel remeny

## The problem

At the time of writing, many of these lists are manually ordered by the users themselves.
\
Letterboxd does not offer "Order by film poster color" functionality for users that wish to do so.
\
\
Manually ordering movie posters from a list of 50 films is hard enough.
\
Manually ordering movie posters from a list of a few thousand films is a nightmare to say the least.
\
\
\
To illustrate the pain further, here are some sample conversations on two separate Letterboxd lists:
\
\
![user-tried-to-sort-by-color-but-failed](images/problem-to-solve/tried-and-failed.jpeg)
\
\
![user-does-not-have-free-time-to-sort-by-color](images/problem-to-solve/no-free-time.jpeg)

## Examples

For a visual representation of this type of "hue sorting" (aside from the letterboxd examples listed above), here is a **manually sorted**
\
representation of movie posters from the `images/sample-images` folder.
\
\
![approximate-order-of-manually-sorted-film-posters](images/manual-sort-examples/manual-sort-of-test-images.jpg)
\
\
_Note_: The film posters above are just a visual aid, and not actually output from the letterboxdHueSort program.
\
The sort order of the letterboxdHueSort program will differ from the above manually generated order.

## Demo

The following demo uses the csv file `sample_list.csv` inside the `samples` folder

### Downloading film posters

When the program is run with an absolute path to the existing film csv file, posters are downloaded
\
in a folder named `posters`, which is created in the same location as the csv file.
\
\
![posters-being-downloaded-into-posters-folder](images/gifs/get-posters.gif)
\
\
The program was ended before the poster for 'I ORIGINS' was completely saved.
\
In this case, the program will continue (the next time it is ran) from the latest film whose poster
\
was not saved. Films with already downloaded posters are skipped.
\
\
![existing-posters-being-skipped](images/gifs/resume-downloads.gif)
\
\
The above two runs of the program downloaded the posters of the films into the `posters` folder
\
\
![posters-downloaded-into-the-posters-folder](images/posters-folder/downloaded-posters.png)
