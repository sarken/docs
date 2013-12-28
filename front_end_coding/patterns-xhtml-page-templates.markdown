---
layout: front_end_guide
title: XHTML Page Templates
---
<ol class="diagram">
<li>body
<ol>
<li>ul #skiplinks</li>
<li>div #header</li>
<li class="emphasise">div #main	</li>
<li>div #footer</li>
</ol>
</li>
</ol>

The individual pages on our archive are contained within the division #main.

Some pages (user home, collection home, tag home, admin home) have a dashboard, which by default we display as a sidebar.

					<ol class="diagram">
						<li>body
							<ol>
								<li>ul #skiplinks</li>
								<li>div #header</li>
								<li>div #dashboard</li>
								<li class="emphasise">div #main	.dashboard</li>
								<li>div #footer</li>
							</ol>
						</li>
					</ol>
