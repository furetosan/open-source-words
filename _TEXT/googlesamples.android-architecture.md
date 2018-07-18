android architecture blueprints the android framework provides a lot of flexibility in deciding how to organize and architect an android app while this freedom is very valuable it can also lead to apps with large classes inconsistent naming schemes as well as mismatching or missing architectures these types of issues can make testing maintaining and extending your apps difficult the android architecture blueprints project demonstrates strategies to help solve or avoid these common problems this project implements the same app using different architectural concepts and tools you can use the samples in this project as a learning reference or as a starting point for creating your own apps the focus of this project is on demonstrating how to structure your code design your architecture and the eventual impact of adopting these patterns on testing and maintaining your app you can use the techniques demonstrated here in many different ways to build apps your own particular priorities will impact how you implement the concepts in these projects so you should not consider these samples to be canonical examples to ensure the focus is kept on the aims described above the app uses a simple ui explore the samples this project hosts each sample app in separate repository branches for more information see the readme md file in each branch stable samples java sample description todo‑mvp demonstrates a basic model‑view‑presenter mvp architecture and provides a foundation on which the other samples are built this sample also acts as a reference point for comparing and contrasting the other samples in this project todo‑mvp‑clean uses concepts from clean architecture todo‑mvp‑dagger uses dagger 2 to add support for dependency injection todo‑mvp‑rxjava uses rxjava 2 to implement concurrency and abstract the data layer todo‑mvvm‑databinding based on the todo databinding sample this version incorporates the model‑view‑viewmodel pattern todo‑mvvm‑live uses viewmodels and livedata from architecture components and the data binding library with an mvvm architecture stable samples kotlin sample description todo mvp kotlin conversion of todo mvp to kotlin todo mvvm live kotlin conversion of todo mvvm live to kotlin external samples external samples are variants that may not be in sync with the rest of the branches in this repository sample description todo‑mvp‑fragmentless uses view objects instead of fragment objects todo‑mvp‑conductor uses the conductor framework to refactor the app to use a single activity architecture todo‑mvi rxjava adapts the model view intent pattern to android to create a fully reactive architecture todo‑mvp kotlin coroutines replaces the asynchronous operations with kotlins coroutines deprecated samples these samples are no longer being maintained but their implementation is still valid sample description todo‑mvp‑loaders fetches data using the loaders api todo‑databinding replaced by todo‑mvvm‑databinding todo‑mvp‑contentproviders based on the todo mvp loaders sample this version fetches data using the loaders api and also makes use of content providers samples in progress sample description dev‑todo‑mvvm‑rxjava based on the todo rxjava sample this version incorporates the model‑view‑viewmodel pattern for information about planned samples see new sample issues why a to do app the app in this project aims to be simple enough that you can understand it quickly but complex enough to showcase difficult design decisions and testing scenarios for more information see the apps specification the following screenshot illustrates the ui of the app choose a sample for your app each sample includes a dedicated readme md file where you can find related metrics as well as subjective assessments and observations by contributors the following factors are worth considering when selecting a particular sample for your app the size of the app you are developing the size and experience of your team the amount of maintenance that you are expecting to have to do whether you need a tablet layout whether you need to support multiple platforms your preference for the compactness of your codebase for more information on choosing and comparing samples see the following pages samples at a glance how to compare samples open a sample in android studio to open one of the samples in android studio begin by checking out one of the sample branches and then open the todoapp directory in android studio the following series of steps illustrate how to open the todo‑mvp sample note the master branch does not compile clone the repository git clone git github com googlesamples android architecture git checkout the todo mvp sample git checkout todo mvp note to review a different sample replace todo mvp with the name of sample you want to check out finally open the todoapp directory in android studio contributors this project is built by the community and curated by google as well as other core maintainers external contributors david gonzález core developer mvp content providers sample karumi developers mvp clean architecture sample natalie masse core developer erik hellman developer mvp rxjava sample saúl molinero developer mvp dagger sample mike nakhimovich developer mvp dagger sample voicu klein developer mvp rxjava sample googlers jose alcérreca lead core developer mustafa kurtuldu ux design stephan linzner core developer florina muntenescu core developer sharif salah technical writer doug sigelbaum kotlin conversion ben weiss kotlin conversion for more information on joining the project see how to become a contributor and the contributors guide