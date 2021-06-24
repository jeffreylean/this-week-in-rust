Title: This Week in Rust 396
Number: 396
Date: 2021-06-23
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/rust-lang/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/rust-lang/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/rust-lang/this-week-in-rust/pulls).

## Updates from Rust Community

### Official

### Newsletters

### Project/Tooling Updates
* [rustymind - Parse and visualize brainwaves with Rust](https://github.com/junjunjd/rustymind)
* [ZH] [Build a Gameboy emulator in Rust](https://yodalee.me/2020/12/2020_rust_gameboy/)

### Observations/Thoughts
- [Walking through "The Java Tutorials" with Rust - boxed trait objects and the search for inheritance](https://rust-java-tutorials.netlify.app/blog/5-trait-objects-2/)
* [WABT: A wonderful CLI for manipulating Wasm](https://blog.knoldus.com/wabt-a-wonderful-cli-for-manipulating-wasm/)

### Rust Walkthroughs
* [Rust and AWS Lambda](https://mitchgollub.com/rust-and-aws-lambda/)
* [ZH] [Develop WebAssembly Program in Rust](https://yodalee.me/2021/05/1helloworld/)

### Research

### Miscellaneous

## Crate of the Week

This week has two crates: [nativeshell](https://github.com/nativeshell/nativeshell) gets you a Flutter app in Rust, while [static-rc](https://github.com/matthieu-m/static-rc) is a compile-time reference-counted smart pointer.

Thanks to [Zicklag](https://users.rust-lang.org/t/crate-of-the-week/2704/922) for both nominations

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

## Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

* [cargo - SearchIndexer takes time indexing \target on windows](https://github.com/rust-lang/cargo/issues/8694)
* [cargo - Ability to specify the output name for a bin target different from the crate name](https://github.com/rust-lang/cargo/issues/1706)
* [cargo - Using alternative registries names in text output](https://github.com/rust-lang/cargo/issues/6691)
* [cargo - A dependency on path = "." should have a good error message](https://github.com/rust-lang/cargo/issues/9518)

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

## Updates from Rust Core

289 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2021-06-07..2021-06-14

* [fix force-warns to allow dashes](https://github.com/rust-lang/rust/pull/86117)
* [suggest a trailing comma if a 1-tuple is expected and a parenthesized expression is found](https://github.com/rust-lang/rust/pull/86116)
* [do not suggest to add type annotations for unnameable types](https://github.com/rust-lang/rust/pull/86215)
* [`to_digit` simplification (less jumps)](https://github.com/rust-lang/rust/pull/85630)
* [multiple improvements to `RwLock`s](https://github.com/rust-lang/rust/pull/84687)
* [add `Ipv6Addr::is_unicast`](https://github.com/rust-lang/rust/pull/85791)
* [stabilize `wasm simd intrinsics`](https://github.com/rust-lang/rust/pull/86204)
* [stabilize `maybe_uninit_ref`](https://github.com/rust-lang/rust/pull/86273)
* [stabilize `simd_x86_bittest`](https://github.com/rust-lang/rust/pull/86233)
* [cargo: implement warning for ignored trailing arguments](https://github.com/rust-lang/cargo/pull/9561)
* [clippy: fix `while_let_on_iterator` suggestion in a closure](https://github.com/rust-lang/rust-clippy/pull/7262)
* [clippy: remove requirement of fully qualified path for `disallowed_method`/`type`](https://github.com/rust-lang/rust-clippy/pull/7345)
* [clippy: fix false positive on `semicolon_if_nothing_returned`](https://github.com/rust-lang/rust-clippy/pull/7326)
* [clippy: fix false positive in `default_numeric_fallback` with external macro expansion](https://github.com/rust-lang/rust-clippy/pull/7325)
* [clippy: `Vec` `extend` to `append`](https://github.com/rust-lang/rust-clippy/pull/7270)
* [BPF target support](https://github.com/rust-lang/rust/pull/79608)
* [support for force-warns](https://github.com/rust-lang/rust/pull/85788)
* [improve debugging experience for enums on windows-msvc](https://github.com/rust-lang/rust/pull/85292)
* [parser: ensure that all nonterminals have tokens after parsing](https://github.com/rust-lang/rust/pull/84995)
* [don't suggest unsized indirection in where-clauses](https://github.com/rust-lang/rust/pull/85979)
* [rustc: allow safe `#[target_feature]` on wasm](https://github.com/rust-lang/rust/pull/84988)
* [always go through the `expn_that_defined` query](https://github.com/rust-lang/rust/pull/86002)
* [perf: miscellaneous inlining improvements](https://github.com/rust-lang/rust/pull/85892)
* [perf: only compute the trait map once](https://github.com/rust-lang/rust/pull/85905)
* [stabilize `vecdeque_binary_search`](https://github.com/rust-lang/rust/pull/83362)
* [update standard library for `IntoIterator` implementation of arrays](https://github.com/rust-lang/rust/pull/85930)
* [clippy: don't warn about `cfg!(..)` as a constant in assertions](https://github.com/rust-lang/rust-clippy/pull/7319)
* [clippy: fix `needless_collect` with binding shadowing](https://github.com/rust-lang/rust-clippy/pull/7289)
* [clippy: add lint `manual_str_repeat`](https://github.com/rust-lang/rust-clippy/pull/7265)

### Rust Compiler Performance Triage

A few small regressions on smaller benchmarks (e.g., helloworld), likely
centered around more IR being generated in a few cases.

Triage done by **@simulacrum**.
Revision range: [d192c80..3912083](https://perf.rust-lang.org/?start=d192c80d2284ba6b5146bb3da586354c3762c72b&end=3912083821c5072f700a75589c8af6a9d3e20a21&absolute=false&stat=instructions%3Au)

2 Regressions, 1 Improvements, 0 Mixed; 1 of them in rollups

[Full report here](https://github.com/rust-lang/rustc-perf/blob/master/triage/2021-06-22.md).

### Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments) process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [Type-changing struct update syntax](https://github.com/rust-lang/rfcs/pull/2528)

### Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)

* [disposition: close] [RFC: Add delete and delete_by methods to Iterator](https://github.com/rust-lang/rfcs/pull/2475)

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)

* [disposition: merge] [Redefine ErrorKind::Other and stop using it in std.](https://github.com/rust-lang/rust/pull/85746)
* [disposition: merge] [When using process::Command on Windows, environment variable names must be case-preserving but case-insensitive](https://github.com/rust-lang/rust/pull/85270)
* [disposition: merge] [Tracking Issue for std::io::Seek::rewind()](https://github.com/rust-lang/rust/issues/85149)
* [disposition: merge] [Support forwarding caller location through trait object method call](https://github.com/rust-lang/rust/pull/81360)
* [disposition: merge] [Tracking issue for ops::Bound::cloned()](https://github.com/rust-lang/rust/issues/61356)

### New RFCs

* [Stabilize Cargo's weak-dep-features and namespaced-features.](https://github.com/rust-lang/rfcs/pull/3143)

## Upcoming Events

### Online

* [June 24, 2021, Berlin, DE - Rust Hack and Learn - Berline.rs](https://berline.rs/)
* [June 29. 2021, Dallas, TX, US - Last Tuesday - Dallas Rust](https://www.meetup.com/Dallas-Rust/events/jqxqwryccjbmc/)
* [July 6, 2021, Buffalo, NY, US - Buffalo Rust User Group, First Tuesdays - Buffalo Rust Meetup](https://www.meetup.com/Buffalo-Rust-Meetup/events/jxfdjsycckbjb/)

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

**ChainSafe Systems**

* [Rust Developer (Remote)](https://jobs.smartrecruiters.com/ChainSafeSystemsInc/743999739358248-rust-developer)

**Kollider**

* [Junior Backend Engineer (Remote)](https://kollider.homerun.co/junior-backend-engineer/en)
* [Senior Backend Engineer (Remote)](https://kollider.homerun.co/senior-backend-engineer/en)
* [DevOps Engineer (Remote)](https://kollider.homerun.co/devops-engineer/en)

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

> If manually managing memory is like wielding a gun, the borrow checker is an automatic safety that prevents you from pulling the trigger when you're roughly pointing it at yourself. But it's coarse-grained and errs on the side of caution; it simulates your foot as as the rectangular box that would contain it, not as a detailed 3D mesh. If you *really* think you can aim it between your toes and avoid hitting yourself (for example, "the value returned by this function must remain alive for no more than 15 successive invocations of this function"), unsafe will let you try, but the borrow checker's built-in rules isn't granular enough to help you, though it will still stop you if you accidentally put your hand in front without declaring it.

– [infogulch on Hacker News](https://news.ycombinator.com/item?id=27468885)

Thanks to [StyMaar](https://users.rust-lang.org/t/twir-quote-of-the-week/328/1056) for the suggestion!

[Please submit quotes and vote for next week!](https://users.rust-lang.org/t/twir-quote-of-the-week/328)

*This Week in Rust is edited by: [nellshamrell](https://github.com/nellshamrell), [llogiq](https://github.com/llogiq), and [cdmistman](https://github.com/cdmistman).*

<small>[Discuss on r/rust](https://www.reddit.com/r/rust/comments/k5nsab/this_week_in_rust_367/)</small>