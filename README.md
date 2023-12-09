# Scholar-Project-Checkpoint

This is the code update checkpoints for the scholar project with professor Panos

I have done:
remove the ability to add multiple authors
remove the search history
make the requests to use GET instead of POST? (With GET, it is possible to bookmark the results and share them.)

now trying to solve:
I would like to do is build a caching system so that we do not need to query Google Scholar all the time.

The idea is to use the FireStore database and check if the results of a given Google Scholar query are already stored in the database. If not, we query Google Scholar and store the API response in the DB, together with the date of the request. If the data is already in the DB, we check when we fetched the data. If the data is more than a week (or month) old, we query Google Scholar again. If the data is in the DB and fetched within the last week, we just get the data from the DB.

And the best year, get_yearly_data are deleted
