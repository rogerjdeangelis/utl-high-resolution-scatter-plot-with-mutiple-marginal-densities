# utl-high-resolution-scatter-plot-with-mutiple-marginal-densities
High resolution scatter plot with mutiple marginal densities 
    %let pgm=utl-high-resolution-scatter-plot-with-mutiple-marginal-densities;

    High resolution scatter plot with mutiple marginal densities


    OUTPUT Highres graphs

    http://tinyurl.com/2nankvtp
    https://github.com/rogerjdeangelis/utl-high-resolution-scatter-plot-with-mutiple-marginal-densities/blob/main/marginal.pdf

    https://www.dropbox.com/s/yr1yxja62jwcemo/marginal.pdf?dl=0


    github
    http://tinyurl.com/42ye4w5m
    https://github.com/rogerjdeangelis/utl-high-resolution-scatter-plot-with-mutiple-marginal-densities

    see
    https://www.dropbox.com/s/yr1yxja62jwcemo/marginal.pdf?dl=0


    /*               _     _
     _ __  _ __ ___ | |__ | | ___ _ __ ___
    | `_ \| `__/ _ \| `_ \| |/ _ \ `_ ` _ \
    | |_) | | | (_) | |_) | |  __/ | | | | |
    | .__/|_|  \___/|_.__/|_|\___|_| |_| |_|
    |_|
    */


    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /*         INPUT                                                                                                          */
    /* =====================                                                                                                  */
    /*          SEPAL  PETAL                                                                                                  */
    /*  SPECIES LENGTH LENGTH                                                                                                 */
    /*                                                                                                                        */
    /*  Setosa    50     14                                                                                                   */
    /*  Setosa    46     14                                                                                                   */
    /*  Setosa    46     10                                                                                                   */
    /*  Setosa    51     17                                                                                                   */
    /*  Setosa    55     13                                                                                                   */
    /*  Setosa    48     16                                                                                                   */
    /*  ....                                                                                                                  */
    /*  Virginica 68     30                                                                                                   */
    /*  Virginica 57     25                                                                                                   */
    /*  Virginica 58     28                                                                                                   */
    /*  Virginica 63     33                                                                                                   */
    /*                                                                                                                        */
    /*         PROCESS                                                                                                        */
    /*  ====================                                                                                                  */
    /*  %utl_rbegin;                                                                                                          */
    /*  parmcards4;                                                                                                           */
    /*  library(haven);                                                                                                       */
    /*  library(WVPlots);                                                                                                     */
    /*  have<-read_sas("d:/sd1/iris.sas7bdat");                                                                               */
    /*  have;                                                                                                                 */
    /*  pdf("d:/pdf/marginal.pdf",7,5);                                                                                       */
    /*  ScatterHistC(have,                                                                                                    */
    /*   "SEPALLENGTH","PETALLENGTH","SPECIES"                                                                                */
    /*   ,title = "Petallength vs Sepallength");                                                                              */
    /*  ;;;;                                                                                                                  */
    /*  %utl_rend;                                                                                                            */
    /*                                                                                                                        */
    /*                              OUTPUT                                                                                    */
    /*  ==========================================================================                                            */
    /*                         Petal Length (mm)                                                                              */
    /*                                                                                                                        */
    /*            0        20        40        60        80                                                                   */
    /*   100 ++---+---------+---------+---------+---------+- 100                                                              */
    /*       |                                             |                                                                  */
    /*  D    |                                             |      SPECIES                                                     */
    /*  e 80 +                              V  V           +  80                                                              */
    /*  n    |                            V     V          |     V=Virginica                                                  */
    /*  s    |      s  S                        V          |     S=Setosa                                                     */
    /*  i 60 +   S      S                 V      V         +  60                                                              */
    /*  t    |  S        S              V        V         |                                                                  */
    /*  y    |   S        S          V             V       |                                                                  */
    /*    40 + S          S         V               V      +  40                                                              */
    /*       |            S        V                 V     |                                                                  */
    /*       |              S   V                      V   |                                                                  */
    /*   100 +---+---------+---------+---------+---------+--+---------------| 100                                             */
    /*       |                                             |   V            +                                                 */
    /*       |                                             |      V         |                                                 */
    /*       |                                             |        V       |                                                 */
    /*       |                                             |           V    |                                                 */
    /*  S  80 +                                  * V       +              V +  80                                             */
    /*  e    |                               V *  ** V     |            V   |                                                 */
    /*  p    |                                   * V       |           V    |                                                 */
    /*  a    |                               V ** V        |          V     |                                                 */
    /*  l    |                             V *** V         |        V       |     D                                           */
    /*    70 +                          V **V* V           +         V      +  70 e                                           */
    /*  L    |                          V * *** V          |       VV       |     n                                           */
    /*  e    |                          V * **VV           |         V      |     s                                           */
    /*  n    |                         V ****V* V          |       V        |     i                                           */
    /*  g    |                        V ** ** V            | S    V         |     t                                           */
    /*  t 60 +           S            V *** V              +   S V          +  60 y                                           */
    /*  h    |      S * ** S           V ** V              |  V             |                                                 */
    /*       |         * S               * V               |   S            |                                                 */
    /*       |         *** S                               |     S          |                                                 */
    /*       |       S **** S                              |      S         |                                                 */
    /*    50 +      S *** S            * V                 +    S           +  50                                             */
    /*       |       S ** * S                              |      S         |                                                 */
    /*       |     S * ** S                                |    S           |                                                 */
    /*       |      S ** S                                 |   S            |                                                 */
    /*       |                                             |  S             |                                                 */
    /*    40 +                                             + D              +  40                                             */
    /*       |                                             |                |                                                 */
    /*       ---+---------+---------+---------+---------+--+--+----+---+----+                                                 */
    /*          0        20        40        60        80  0 20   40   60   80                                                */
    /*                                                                                                                        */
    /*                         Petal Length (mm)                                                                              */
    /*                                                                                                                        */
    /*                                                                                                                        */
    /**************************************************************************************************************************/

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    %utlfkil(d:/pdf/marginal.pdf);

    %utl_rbegin;
    parmcards4;
    library(haven);
    library(WVPlots);
    have<-read_sas("d:/sd1/iris.sas7bdat");
    have;
    pdf("d:/pdf/marginal.pdf",7,5);
    ScatterHistC(have,
     "SEPALLENGTH","PETALLENGTH","SPECIES"
     ,title = "Petallength vs Sepallength");
    ;;;;
    %utl_rend;

    /*           _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| `_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    */

    OUTPUT Highres graphs

    http://tinyurl.com/2nankvtp
    https://github.com/rogerjdeangelis/utl-high-resolution-scatter-plot-with-mutiple-marginal-densities/blob/main/marginal.pdf

    https://www.dropbox.com/s/yr1yxja62jwcemo/marginal.pdf?dl=0

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
