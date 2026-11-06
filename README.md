# act-speaking-exercise-frontend
A demo that shows how to execute action


## AI English Gym changelog summary

The private frontend dispatches `changelog-summary` with an inclusive UTC+8
period and optional `backend,aiTutor,website,cms` source keys. Product scope is
always AI English Gym / Think & Speak, including when CMS is selected; other
CMS modules are excluded without a scope switch. The shared runner keeps its
single-release defaults and reuses ACTION_TOKEN, AWS and SSM settings. Keep
`quiet` enabled; reports attach only to private frontend releases. Publish
api-meter summary migrations and repo-toolkit main before enabling this path.

The same module boundary applies to the normal single-release `joint` changelog:
a declared `cms` tag contributes its Think & Speak pages, including teacher/admin
changes with no student-app change. Other CMS modules remain excluded even when
they mention Think & Speak. Deploy api-meter route migration `e2513a0d7f26`
before enabling CMS diff reads.
[中文](README.zh-CN.md).
