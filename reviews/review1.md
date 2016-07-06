Format: http://matt.might.net/articles/peer-review-rebuttals/

> -- Reviewer 1 --

Thank you for a great review! We really appreciate the thorough review!

Best,
Barret


> In a few places the term "calibrate you eyes" is used. Much better might be
> "train our brains" ... our eyes are just the data acquisition system, the real
> work is happening in our brains, brains that have only ever needed to deal
> with a 3D world, just the flatlanders only needed to deal with a 2D world.
> An alternative would be "visualise", in the context of proving insight into
> complicated or high dimensional data.

Changed to some form of "train our brains". (f3e6ee1)


> Page 1, cube section. Could add a 0-D cube is a point.

Added. (299d9cc)


> Page 1, in the description of the figure 1 I think a bit more rigor could be
> used since this is the first time the notion of imagining a shape in higher
> dimension is done by analogy to lower dimensions. "double the cube" ... how
> about "replicate and shift along an orthogonal axis".

Used similar phrasing as suggested. (7c7bc57)

> Also at the point of figure 1 I don't see mention that it is showing a projection onto a 2D
> surface. Obvious perhaps but explaining this more at the start sets the scene
> for the rest of the examples. Making it clear also of the infinity of
> projections and that some look the same as their lower dimension version (ie:
> along a major axis).

Addressed near beginning of paper and about projecting down to 2 dimensions. (f07ff9b)

Did not want to talk about similar projections, as that is not the focus of this paper.


> "An alternative way to think [of the vertices of a] of a high-dimensional cube
> is that it can be considered ...". Should have "vertices" in there somewhere.

Added! (b19df9a)


> The rule for edges is given, how about the generation rules for faces, or
> hyperfaces?

This is already talked about in the first paragraph of the 'Hollow cube' section.  Methods have also been added to address earlier reviewer points.


> For the hollow cube section, might not regular grids on the faces be
> significantly more insightful that random fills? See later.

Will add a new function for equidistance cube "face" in geozoo R package. %TODO

Will explain both equidistant and random methods. Added in (f2118b9)


> A typo I think in the Sphere section "A sphere can be described as all points
> within a fixed radius of zero  ..." should zero be unity. Or do you mean a
> fixed radius away from the center of the sphere? In general there is a
> tightening up of some of the wording when describing the extensions to higher
> dimensions based upon the same geometry in lower dimensions.

Changed. (7e4ec63)


> In the hollow sphere perhaps the description of how the points are created on
> the surface could be clarified. The "multivariate standard normal
> distribution", perhaps it is well known but it isn't clear to me what this
> means. I think the "hypercube rejection method is used later on ... choose
> coordinates (x,y,z) each uniformly distributed on the interval [-1,1]. If the
> length of this vector is greater than 1 then reject it, otherwise normalise it
> and use it as a sample on the sphere.

Added citation to the book "Statistics on Spheres" that explains the method. (046a202)

We can't use rejection method described by reviewer.  There is more than 99% rejection at higher dimensions. This is talked about in the subsection after ("Don't reject the solid sphere!")


> In the simplex section, the definition there is not what I imagined a simplex
> to be. Happy to stand corrected. I thought a k dimensional simplex was the
> simplest polytope in that dimension, consisting of k+1 vertices. Or am I
> getting confused with a regular simplex?

Correct. A two-simplex is a triangle that lives in the 2D plain. Changed in (aa99906)


> The section on ring torus takes up a disproportionate space (2 pages?) and I
> don't think really adds anything to the paper.

Added (1a4fd12)


> Many of the links in the references don't work. I know this is a problem with
> web links but I suggest many links have not been checked for some time. Not
> sure what the publication policy is on web links but it is the practice in
> some pubications for the reference to include the date at which the link
> existed.

Fixed! (0f47ae2)


> The references also have a "back link" into the paper, is that the style for
> this publication?

Yes. This is in the style provided.  (Thank you RJournal!)


> Main concern
> --------------
>
> The main concern I have with the paper is that the stated goal of facilitating
> understanding of the higher order geometries is not reflected in some of the
> techniques used. Indeed quite the opposite, some of the methods such as volume
> filling serve more to obscure the nature rather than provide insight.
> Similarly it is appreciated that randomly choosing points that form lines in
> N-dimensions can be an elegant way to create those lines, applying that to
> filling in faces also seem to obscure the nature of the geometry. Would it not
> be more informative to use filling techniques that are more geometrically
> related to the faces or hyperfaces? For example, for planar faces such as in a
> cube/hypercube, represent the faces as a regular grid. For triangular faces of
> a simplex use a regular triangular tessellation. For the torus, use cross
> sections, circles through the ring of the torus. These would seem to provide
> greater possibilities to understand their nature.

For visualization, randomization helps the user as regular grid shapes or patterns dominate the user's attention and take away from the object's shape.  For example, using random points in figure 3 (faces of cubes) allows the viewer to perceive volume of each of the faces of a 4-D cube. If the 4-D cube face (a 3-D cube) was presented as a grid, the whole overall shape would difficult to discern what is going on.


> On a similar vein I would urge the authors to think about visualisation
> techniques that may provide additional cues as to the nature. The "depth"
> along edges in the N+1 dimension could be represented as a shading between two
> colours, or intensity. I am not familiar with the graphics capabilities of the
> tools used but note that no mention of representing faces as perhaps
> semitransparent surfaces is discussed, hyperfaces as volumes and so on. Accept
> this last example may be out of the scope of the paper requiring different
> software tools.

Correct, this last point is out of scope for this paper.

Thomas Banchoff's publication of "Illustrating beyond the Third Dimension" (http://www.math.brown.edu/~banchoff/howison/newbanchoff/publications/pdfs/IllustratingBeyond.pdf) show some possibilities of how "depth" can be achieved. Paul Bourke even does his on his website by highlighting the edges according to one dimension (http://paulbourke.net/geometry/hyperspace/). However, these approaches quickly fail when going beyond four dimensions.

The publication on the software package XGobi (https://www.researchgate.net/publication/2248028_XGobi_Interactive_Dynamic_Data_Visualization_in_the_X_Window_System) talks about using a 'tour' to visit whole data space. 'Touring' the data really helps with letting the difference between a solid object and a hollow object.  Points on a surface will move at similar rates, while points in the middle of an object will move at variable rates. The tour is what is currently used to visualize anything that is produced in the geozoo R package. Unfortunately, we can not reproduce the moving tour in the paper.


Furnas and Buja (http://www.jstor.org/stable/1390897) talk about how they use highlighting to visualize sub objects within the over-all object while projecting down to the second dimension.  (Section 6 with examples in section 7)




































<!-- Show a couple videos of the objects in motion?
Quiz on
 4 dim hollow sphere
 4 dim solid sphere
 10 dim sphere
 10 dim cube -->
