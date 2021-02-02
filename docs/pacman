---
permalink: /pacman
---

searchcode small logo
Home About API searchcode server
/src/js/pacman10-hp.3.js
https://github.com/wiltongarcia/google_pacman
JavaScript | 3200 lines | 3189 code | 2 blank | 9 comment | 738 complexity | 80cdc9b3166d0532c6e7e29ce6781049 MD5 | raw file
Large files files are truncated, but you can click here to view the full file

   1/*!
   2 * Google Pacman 
   3 *
   4 * Copyright 2010, Google
   5 *
   6 * Date: Fri May 21 2010
   7 */
   8
   9google.pacman ||
  10function () {
  11  var a = true,
  12    e = false,
  13    g = {},
  14    i = [1, 4, 2, 8],
  15    l = {
  16      0: {
  17        axis: 0,
  18        increment: 0
  19      },
  20      1: {
  21        axis: 0,
  22        increment: -1
  23      },
  24      2: {
  25        axis: 0,
  26        increment: +1
  27      },
  28      4: {
  29        axis: 1,
  30        increment: -1
  31      },
  32      8: {
  33        axis: 1,
  34        increment: +1
  35      }
  36    },
  37    m = [0, 7, 17, 32],
  38    n = [{
  39      x: 5,
  40      y: 1,
  41      w: 56
  42    },
  43    {
  44      x: 5,
  45      y: 4,
  46      w: 5
  47    },
  48    {
  49      x: 5,
  50      y: 1,
  51      h: 4
  52    },
  53    {
  54      x: 9,
  55      y: 1,
  56      h: 12
  57    },
  58    {
  59      x: 5,
  60      y: 12,
  61      h: 4
  62    },
  63    {
  64      x: 10,
  65      y: 12,
  66      h: 4
  67    },
  68    {
  69      x: 5,
  70      y: 15,
  71      w: 16
  72    },
  73    {
  74      x: 5,
  75      y: 12,
  76      w: 31
  77    },
  78    {
  79      x: 60,
  80      y: 1,
  81      h: 4
  82    },
  83    {
  84      x: 54,
  85      y: 1,
  86      h: 4
  87    },
  88    {
  89      x: 19,
  90      y: 1,
  91      h: 12
  92    },
  93    {
  94      x: 19,
  95      y: 4,
  96      w: 26
  97    },
  98    {
  99      x: 13,
 100      y: 5,
 101      w: 7
 102    },
 103    {
 104      x: 13,
 105      y: 5,
 106      h: 4
 107    },
 108    {
 109      x: 13,
 110      y: 8,
 111      w: 3
 112    },
 113    {
 114      x: 56,
 115      y: 4,
 116      h: 9
 117    },
 118    {
 119      x: 48,
 120      y: 4,
 121      w: 13
 122    },
 123    {
 124      x: 48,
 125      y: 1,
 126      h: 12
 127    },
 128    {
 129      x: 60,
 130      y: 12,
 131      h: 4
 132    },
 133    {
 134      x: 44,
 135      y: 15,
 136      w: 17
 137    },
 138    {
 139      x: 54,
 140      y: 12,
 141      h: 4
 142    },
 143    {
 144      x: 44,
 145      y: 12,
 146      w: 17
 147    },
 148    {
 149      x: 44,
 150      y: 1,
 151      h: 15
 152    },
 153    {
 154      x: 41,
 155      y: 13,
 156      w: 4
 157    },
 158    {
 159      x: 41,
 160      y: 13,
 161      h: 3
 162    },
 163    {
 164      x: 38,
 165      y: 13,
 166      h: 3
 167    },
 168    {
 169      x: 38,
 170      y: 15,
 171      w: 4
 172    },
 173    {
 174      x: 35,
 175      y: 10,
 176      w: 10
 177    },
 178    {
 179      x: 35,
 180      y: 1,
 181      h: 15
 182    },
 183    {
 184      x: 35,
 185      y: 13,
 186      w: 4
 187    },
 188    {
 189      x: 21,
 190      y: 12,
 191      h: 4
 192    },
 193    {
 194      x: 24,
 195      y: 12,
 196      h: 4
 197    },
 198    {
 199      x: 24,
 200      y: 15,
 201      w: 12
 202    },
 203    {
 204      x: 27,
 205      y: 4,
 206      h: 9
 207    },
 208    {
 209      x: 52,
 210      y: 9,
 211      w: 5
 212    },
 213    {
 214      x: 56,
 215      y: 8,
 216      w: 10,
 217      type: 1
 218    },
 219    {
 220      x: 1,
 221      y: 8,
 222      w: 9,
 223      type: 1
 224    }],
 225    o = [{
 226      x: 1,
 227      y: 8,
 228      w: 8
 229    },
 230    {
 231      x: 57,
 232      y: 8,
 233      w: 9
 234    },
 235    {
 236      x: 44,
 237      y: 2,
 238      h: 10
 239    },
 240    {
 241      x: 35,
 242      y: 5,
 243      h: 7
 244    },
 245    {
 246      x: 36,
 247      y: 4,
 248      w: 8
 249    },
 250    {
 251      x: 36,
 252      y: 10,
 253      w: 8
 254    },
 255    {
 256      x: 39,
 257      y: 15,
 258      w: 2
 259    }],
 260    p = [{
 261      x: 5,
 262      y: 15
 263    },
 264    {
 265      x: 5,
 266      y: 3
 267    },
 268    {
 269      x: 15,
 270      y: 8
 271    },
 272    {
 273      x: 60,
 274      y: 3
 275    },
 276    {
 277      x: 60,
 278      y: 15
 279    }],
 280    q = [{
 281      x: 2,
 282      y: 8
 283    },
 284    {
 285      x: 63,
 286      y: 8
 287    }],
 288    r = {
 289      1: [{
 290        x: 39.5,
 291        y: 15,
 292        dir: 4
 293      },
 294      {
 295        x: 39.5,
 296        y: 4,
 297        dir: 4,
 298        scatterX: 57,
 299        scatterY: -4
 300      },
 301      {
 302        x: 39.5,
 303        y: 7,
 304        dir: 2,
 305        scatterX: 0,
 306        scatterY: -4
 307      },
 308      {
 309        x: 37.625,
 310        y: 7,
 311        dir: 1,
 312        scatterX: 57,
 313        scatterY: 20
 314      },
 315      {
 316        x: 41.375,
 317        y: 7,
 318        dir: 1,
 319        scatterX: 0,
 320        scatterY: 20
 321      }],
 322      2: [{
 323        x: 40.25,
 324        y: 15,
 325        dir: 8
 326      },
 327      {
 328        x: 38.75,
 329        y: 15,
 330        dir: 4
 331      },
 332      {
 333        x: 39.5,
 334        y: 4,
 335        dir: 4,
 336        scatterX: 57,
 337        scatterY: -4
 338      },
 339      {
 340        x: 39.5,
 341        y: 7,
 342        dir: 2,
 343        scatterX: 0,
 344        scatterY: -4
 345      },
 346      {
 347        x: 37.625,
 348        y: 7,
 349        dir: 1,
 350        scatterX: 57,
 351        scatterY: 20
 352      },
 353      {
 354        x: 41.375,
 355        y: 7,
 356        dir: 1,
 357        scatterX: 0,
 358        scatterY: 20
 359      }]
 360    },
 361    s = [32, 312],
 362    v = [80, 312],
 363    w = {
 364      0: 0.16,
 365      1: 0.23,
 366      2: 1,
 367      3: 1,
 368      4: 2.23,
 369      5: 0.3,
 370      6: 1.9,
 371      7: 2.23,
 372      8: 1.9,
 373      9: 5,
 374      10: 1.9,
 375      11: 1.18,
 376      12: 0.3,
 377      13: 0.5,
 378      14: 1.9,
 379      15: 9,
 380      16: 10,
 381      17: 0.26
 382    },
 383    y = 0.8 * 0.4,
 384    z = [{},
 385    {
 386      ghostSpeed: 0.75,
 387      ghostTunnelSpeed: 0.4,
 388      playerSpeed: 0.8,
 389      dotEatingSpeed: 0.71,
 390      ghostFrightSpeed: 0.5,
 391      playerFrightSpeed: 0.9,
 392      dotEatingFrightSpeed: 0.79,
 393      elroyDotsLeftPart1: 20,
 394      elroySpeedPart1: 0.8,
 395      elroyDotsLeftPart2: 10,
 396      elroySpeedPart2: 0.85,
 397      frightTime: 6,
 398      frightBlinkCount: 5,
 399      fruit: 1,
 400      fruitScore: 100,
 401      ghostModeSwitchTimes: [7, 20, 7, 20, 5, 20, 5, 1],
 402      penForceTime: 4,
 403      penLeavingLimits: [0, 0, 30, 60]
 404    },
 405    {
 406      ghostSpeed: 0.85,
 407      ghostTunnelSpeed: 0.45,
 408      playerSpeed: 0.9,
 409      dotEatingSpeed: 0.79,
 410      ghostFrightSpeed: 0.55,
 411      playerFrightSpeed: 0.95,
 412      dotEatingFrightSpeed: 0.83,
 413      elroyDotsLeftPart1: 30,
 414      elroySpeedPart1: 0.9,
 415      elroyDotsLeftPart2: 15,
 416      elroySpeedPart2: 0.95,
 417      frightTime: 5,
 418      frightBlinkCount: 5,
 419      fruit: 2,
 420      fruitScore: 300,
 421      ghostModeSwitchTimes: [7, 20, 7, 20, 5, 1033, 1 / 60, 1],
 422      penForceTime: 4,
 423      penLeavingLimits: [0, 0, 0, 50],
 424      cutsceneId: 1
 425    },
 426    {
 427      ghostSpeed: 0.85,
 428      ghostTunnelSpeed: 0.45,
 429      playerSpeed: 0.9,
 430      dotEatingSpeed: 0.79,
 431      ghostFrightSpeed: 0.55,
 432      playerFrightSpeed: 0.95,
 433      dotEatingFrightSpeed: 0.83,
 434      elroyDotsLeftPart1: 40,
 435      elroySpeedPart1: 0.9,
 436      elroyDotsLeftPart2: 20,
 437      elroySpeedPart2: 0.95,
 438      frightTime: 4,
 439      frightBlinkCount: 5,
 440      fruit: 3,
 441      fruitScore: 500,
 442      ghostModeSwitchTimes: [7, 20, 7, 20, 5, 1033, 1 / 60, 1],
 443      penForceTime: 4,
 444      penLeavingLimits: [0, 0, 0, 0]
 445    },
 446    {
 447      ghostSpeed: 0.85,
 448      ghostTunnelSpeed: 0.45,
 449      playerSpeed: 0.9,
 450      dotEatingSpeed: 0.79,
 451      ghostFrightSpeed: 0.55,
 452      playerFrightSpeed: 0.95,
 453      dotEatingFrightSpeed: 0.83,
 454      elroyDotsLeftPart1: 40,
 455      elroySpeedPart1: 0.9,
 456      elroyDotsLeftPart2: 20,
 457      elroySpeedPart2: 0.95,
 458      frightTime: 3,
 459      frightBlinkCount: 5,
 460      fruit: 3,
 461      fruitScore: 500,
 462      ghostModeSwitchTimes: [7, 20, 7, 20, 5, 1033, 1 / 60, 1],
 463      penForceTime: 4,
 464      penLeavingLimits: [0, 0, 0, 0]
 465    },
 466    {
 467      ghostSpeed: 0.95,
 468      ghostTunnelSpeed: 0.5,
 469      playerSpeed: 1,
 470      dotEatingSpeed: 0.87,
 471      ghostFrightSpeed: 0.6,
 472      playerFrightSpeed: 1,
 473      dotEatingFrightSpeed: 0.87,
 474      elroyDotsLeftPart1: 40,
 475      elroySpeedPart1: 1,
 476      elroyDotsLeftPart2: 20,
 477      elroySpeedPart2: 1.05,
 478      frightTime: 2,
 479      frightBlinkCount: 5,
 480      fruit: 4,
 481      fruitScore: 700,
 482      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 483      penForceTime: 3,
 484      penLeavingLimits: [0, 0, 0, 0],
 485      cutsceneId: 2
 486    },
 487    {
 488      ghostSpeed: 0.95,
 489      ghostTunnelSpeed: 0.5,
 490      playerSpeed: 1,
 491      dotEatingSpeed: 0.87,
 492      ghostFrightSpeed: 0.6,
 493      playerFrightSpeed: 1,
 494      dotEatingFrightSpeed: 0.87,
 495      elroyDotsLeftPart1: 50,
 496      elroySpeedPart1: 1,
 497      elroyDotsLeftPart2: 25,
 498      elroySpeedPart2: 1.05,
 499      frightTime: 5,
 500      frightBlinkCount: 5,
 501      fruit: 4,
 502      fruitScore: 700,
 503      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 504      penForceTime: 3,
 505      penLeavingLimits: [0, 0, 0, 0]
 506    },
 507    {
 508      ghostSpeed: 0.95,
 509      ghostTunnelSpeed: 0.5,
 510      playerSpeed: 1,
 511      dotEatingSpeed: 0.87,
 512      ghostFrightSpeed: 0.6,
 513      playerFrightSpeed: 1,
 514      dotEatingFrightSpeed: 0.87,
 515      elroyDotsLeftPart1: 50,
 516      elroySpeedPart1: 1,
 517      elroyDotsLeftPart2: 25,
 518      elroySpeedPart2: 1.05,
 519      frightTime: 2,
 520      frightBlinkCount: 5,
 521      fruit: 5,
 522      fruitScore: 1E3,
 523      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 524      penForceTime: 3,
 525      penLeavingLimits: [0, 0, 0, 0]
 526    },
 527    {
 528      ghostSpeed: 0.95,
 529      ghostTunnelSpeed: 0.5,
 530      playerSpeed: 1,
 531      dotEatingSpeed: 0.87,
 532      ghostFrightSpeed: 0.6,
 533      playerFrightSpeed: 1,
 534      dotEatingFrightSpeed: 0.87,
 535      elroyDotsLeftPart1: 50,
 536      elroySpeedPart1: 1,
 537      elroyDotsLeftPart2: 25,
 538      elroySpeedPart2: 1.05,
 539      frightTime: 2,
 540      frightBlinkCount: 5,
 541      fruit: 5,
 542      fruitScore: 1E3,
 543      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 544      penForceTime: 3,
 545      penLeavingLimits: [0, 0, 0, 0]
 546    },
 547    {
 548      ghostSpeed: 0.95,
 549      ghostTunnelSpeed: 0.5,
 550      playerSpeed: 1,
 551      dotEatingSpeed: 0.87,
 552      ghostFrightSpeed: 0.6,
 553      playerFrightSpeed: 1,
 554      dotEatingFrightSpeed: 0.87,
 555      elroyDotsLeftPart1: 60,
 556      elroySpeedPart1: 1,
 557      elroyDotsLeftPart2: 30,
 558      elroySpeedPart2: 1.05,
 559      frightTime: 1,
 560      frightBlinkCount: 3,
 561      fruit: 6,
 562      fruitScore: 2E3,
 563      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 564      penForceTime: 3,
 565      penLeavingLimits: [0, 0, 0, 0],
 566      cutsceneId: 3
 567    },
 568    {
 569      ghostSpeed: 0.95,
 570      ghostTunnelSpeed: 0.5,
 571      playerSpeed: 1,
 572      dotEatingSpeed: 0.87,
 573      ghostFrightSpeed: 0.6,
 574      playerFrightSpeed: 1,
 575      dotEatingFrightSpeed: 0.87,
 576      elroyDotsLeftPart1: 60,
 577      elroySpeedPart1: 1,
 578      elroyDotsLeftPart2: 30,
 579      elroySpeedPart2: 1.05,
 580      frightTime: 5,
 581      frightBlinkCount: 5,
 582      fruit: 6,
 583      fruitScore: 2E3,
 584      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 585      penForceTime: 3,
 586      penLeavingLimits: [0, 0, 0, 0]
 587    },
 588    {
 589      ghostSpeed: 0.95,
 590      ghostTunnelSpeed: 0.5,
 591      playerSpeed: 1,
 592      dotEatingSpeed: 0.87,
 593      ghostFrightSpeed: 0.6,
 594      playerFrightSpeed: 1,
 595      dotEatingFrightSpeed: 0.87,
 596      elroyDotsLeftPart1: 60,
 597      elroySpeedPart1: 1,
 598      elroyDotsLeftPart2: 30,
 599      elroySpeedPart2: 1.05,
 600      frightTime: 2,
 601      frightBlinkCount: 5,
 602      fruit: 7,
 603      fruitScore: 3E3,
 604      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 605      penForceTime: 3,
 606      penLeavingLimits: [0, 0, 0, 0]
 607    },
 608    {
 609      ghostSpeed: 0.95,
 610      ghostTunnelSpeed: 0.5,
 611      playerSpeed: 1,
 612      dotEatingSpeed: 0.87,
 613      ghostFrightSpeed: 0.6,
 614      playerFrightSpeed: 1,
 615      dotEatingFrightSpeed: 0.87,
 616      elroyDotsLeftPart1: 80,
 617      elroySpeedPart1: 1,
 618      elroyDotsLeftPart2: 40,
 619      elroySpeedPart2: 1.05,
 620      frightTime: 1,
 621      frightBlinkCount: 3,
 622      fruit: 7,
 623      fruitScore: 3E3,
 624      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 625      penForceTime: 3,
 626      penLeavingLimits: [0, 0, 0, 0]
 627    },
 628    {
 629      ghostSpeed: 0.95,
 630      ghostTunnelSpeed: 0.5,
 631      playerSpeed: 1,
 632      dotEatingSpeed: 0.87,
 633      ghostFrightSpeed: 0.6,
 634      playerFrightSpeed: 1,
 635      dotEatingFrightSpeed: 0.87,
 636      elroyDotsLeftPart1: 80,
 637      elroySpeedPart1: 1,
 638      elroyDotsLeftPart2: 40,
 639      elroySpeedPart2: 1.05,
 640      frightTime: 1,
 641      frightBlinkCount: 3,
 642      fruit: 8,
 643      fruitScore: 5E3,
 644      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 645      penForceTime: 3,
 646      penLeavingLimits: [0, 0, 0, 0],
 647      cutsceneId: 3
 648    },
 649    {
 650      ghostSpeed: 0.95,
 651      ghostTunnelSpeed: 0.5,
 652      playerSpeed: 1,
 653      dotEatingSpeed: 0.87,
 654      ghostFrightSpeed: 0.6,
 655      playerFrightSpeed: 1,
 656      dotEatingFrightSpeed: 0.87,
 657      elroyDotsLeftPart1: 80,
 658      elroySpeedPart1: 1,
 659      elroyDotsLeftPart2: 40,
 660      elroySpeedPart2: 1.05,
 661      frightTime: 3,
 662      frightBlinkCount: 5,
 663      fruit: 8,
 664      fruitScore: 5E3,
 665      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 666      penForceTime: 3,
 667      penLeavingLimits: [0, 0, 0, 0]
 668    },
 669    {
 670      ghostSpeed: 0.95,
 671      ghostTunnelSpeed: 0.5,
 672      playerSpeed: 1,
 673      dotEatingSpeed: 0.87,
 674      ghostFrightSpeed: 0.6,
 675      playerFrightSpeed: 1,
 676      dotEatingFrightSpeed: 0.87,
 677      elroyDotsLeftPart1: 100,
 678      elroySpeedPart1: 1,
 679      elroyDotsLeftPart2: 50,
 680      elroySpeedPart2: 1.05,
 681      frightTime: 1,
 682      frightBlinkCount: 3,
 683      fruit: 8,
 684      fruitScore: 5E3,
 685      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 686      penForceTime: 3,
 687      penLeavingLimits: [0, 0, 0, 0]
 688    },
 689    {
 690      ghostSpeed: 0.95,
 691      ghostTunnelSpeed: 0.5,
 692      playerSpeed: 1,
 693      dotEatingSpeed: 0.87,
 694      ghostFrightSpeed: 0.6,
 695      playerFrightSpeed: 1,
 696      dotEatingFrightSpeed: 0.87,
 697      elroyDotsLeftPart1: 100,
 698      elroySpeedPart1: 1,
 699      elroyDotsLeftPart2: 50,
 700      elroySpeedPart2: 1.05,
 701      frightTime: 1,
 702      frightBlinkCount: 3,
 703      fruit: 8,
 704      fruitScore: 5E3,
 705      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 706      penForceTime: 3,
 707      penLeavingLimits: [0, 0, 0, 0]
 708    },
 709    {
 710      ghostSpeed: 0.95,
 711      ghostTunnelSpeed: 0.5,
 712      playerSpeed: 1,
 713      dotEatingSpeed: 0.87,
 714      ghostFrightSpeed: 0.6,
 715      playerFrightSpeed: 1,
 716      dotEatingFrightSpeed: 0.87,
 717      elroyDotsLeftPart1: 100,
 718      elroySpeedPart1: 1,
 719      elroyDotsLeftPart2: 50,
 720      elroySpeedPart2: 1.05,
 721      frightTime: 0,
 722      frightBlinkCount: 0,
 723      fruit: 8,
 724      fruitScore: 5E3,
 725      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 726      penForceTime: 3,
 727      penLeavingLimits: [0, 0, 0, 0],
 728      cutsceneId: 3
 729    },
 730    {
 731      ghostSpeed: 0.95,
 732      ghostTunnelSpeed: 0.5,
 733      playerSpeed: 1,
 734      dotEatingSpeed: 0.87,
 735      ghostFrightSpeed: 0.6,
 736      playerFrightSpeed: 1,
 737      dotEatingFrightSpeed: 0.87,
 738      elroyDotsLeftPart1: 100,
 739      elroySpeedPart1: 1,
 740      elroyDotsLeftPart2: 50,
 741      elroySpeedPart2: 1.05,
 742      frightTime: 1,
 743      frightBlinkCount: 3,
 744      fruit: 8,
 745      fruitScore: 5E3,
 746      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 747      penForceTime: 3,
 748      penLeavingLimits: [0, 0, 0, 0]
 749    },
 750    {
 751      ghostSpeed: 0.95,
 752      ghostTunnelSpeed: 0.5,
 753      playerSpeed: 1,
 754      dotEatingSpeed: 0.87,
 755      ghostFrightSpeed: 0.6,
 756      playerFrightSpeed: 1,
 757      dotEatingFrightSpeed: 0.87,
 758      elroyDotsLeftPart1: 120,
 759      elroySpeedPart1: 1,
 760      elroyDotsLeftPart2: 60,
 761      elroySpeedPart2: 1.05,
 762      frightTime: 0,
 763      frightBlinkCount: 0,
 764      fruit: 8,
 765      fruitScore: 5E3,
 766      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 767      penForceTime: 3,
 768      penLeavingLimits: [0, 0, 0, 0]
 769    },
 770    {
 771      ghostSpeed: 0.95,
 772      ghostTunnelSpeed: 0.5,
 773      playerSpeed: 1,
 774      dotEatingSpeed: 0.87,
 775      ghostFrightSpeed: 0.6,
 776      playerFrightSpeed: 1,
 777      dotEatingFrightSpeed: 0.87,
 778      elroyDotsLeftPart1: 120,
 779      elroySpeedPart1: 1,
 780      elroyDotsLeftPart2: 60,
 781      elroySpeedPart2: 1.05,
 782      frightTime: 0,
 783      frightBlinkCount: 0,
 784      fruit: 8,
 785      fruitScore: 5E3,
 786      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 787      penForceTime: 3,
 788      penLeavingLimits: [0, 0, 0, 0]
 789    },
 790    {
 791      ghostSpeed: 0.95,
 792      ghostTunnelSpeed: 0.5,
 793      playerSpeed: 0.9,
 794      dotEatingSpeed: 0.79,
 795      ghostFrightSpeed: 0.75,
 796      playerFrightSpeed: 0.9,
 797      dotEatingFrightSpeed: 0.79,
 798      elroyDotsLeftPart1: 120,
 799      elroySpeedPart1: 1,
 800      elroyDotsLeftPart2: 60,
 801      elroySpeedPart2: 1.05,
 802      frightTime: 0,
 803      frightBlinkCount: 0,
 804      fruit: 8,
 805      fruitScore: 5E3,
 806      ghostModeSwitchTimes: [5, 20, 5, 20, 5, 1037, 1 / 60, 1],
 807      penForceTime: 3,
 808      penLeavingLimits: [0, 0, 0, 0]
 809    }],
 810    A = {
 811      1: [{
 812        x: 37.6,
 813        y: 7,
 814        dir: 1,
 815        dest: 6.375,
 816        speed: 0.48
 817      },
 818      {
 819        x: 37.6,
 820        y: 6.375,
 821        dir: 2,
 822        dest: 7.625,
 823        speed: 0.48
 824      },
 825      {
 826        x: 37.6,
 827        y: 7.625,
 828        dir: 1,
 829        dest: 7,
 830        speed: 0.48
 831      }],
 832      2: [{
 833        x: 39.5,
 834        y: 7,
 835        dir: 2,
 836        dest: 7.625,
 837        speed: 0.48
 838      },
 839      {
 840        x: 39.5,
 841        y: 7.625,
 842        dir: 1,
 843        dest: 6.375,
 844        speed: 0.48
 845      },
 846      {
 847        x: 39.5,
 848        y: 6.375,
 849        dir: 2,
 850        dest: 7,
 851        speed: 0.48
 852      }],
 853      3: [{
 854        x: 41.4,
 855        y: 7,
 856        dir: 1,
 857        dest: 6.375,
 858        speed: 0.48
 859      },
 860      {
 861        x: 41.4,
 862        y: 6.375,
 863        dir: 2,
 864        dest: 7.625,
 865        speed: 0.48
 866      },
 867      {
 868        x: 41.4,
 869        y: 7.625,
 870        dir: 1,
 871        dest: 7,
 872        speed: 0.48
 873      }],
 874      4: [{
 875        x: 37.6,
 876        y: 7,
 877        dir: 8,
 878        dest: 39.5,
 879        speed: y
 880      },
 881      {
 882        x: 39.5,
 883        y: 7,
 884        dir: 1,
 885        dest: 4,
 886        speed: y
 887      }],
 888      5: [{
 889        x: 39.5,
 890        y: 7,
 891        dir: 1,
 892        dest: 4,
 893        speed: y
 894      }],
 895      6: [{
 896        x: 41.4,
 897        y: 7,
 898        dir: 4,
 899        dest: 39.5,
 900        speed: y
 901      },
 902      {
 903        x: 39.5,
 904        y: 7,
 905        dir: 1,
 906        dest: 4,
 907        speed: y
 908      }],
 909      7: [{
 910        x: 39.5,
 911        y: 4,
 912        dir: 2,
 913        dest: 7,
 914        speed: 1.6
 915      },
 916      {
 917        x: 39.5,
 918        y: 7,
 919        dir: 4,
 920        dest: 37.625,
 921        speed: 1.6
 922      }],
 923      8: [{
 924        x: 39.5,
 925        y: 4,
 926        dir: 2,
 927        dest: 7,
 928        speed: 1.6
 929      }],
 930      9: [{
 931        x: 39.5,
 932        y: 4,
 933        dir: 2,
 934        dest: 7,
 935        speed: 1.6
 936      },
 937      {
 938        x: 39.5,
 939        y: 7,
 940        dir: 8,
 941        dest: 41.375,
 942        speed: 1.6
 943      }],
 944      10: [{
 945        x: 37.6,
 946        y: 7,
 947        dir: 8,
 948        dest: 39.5,
 949        speed: y
 950      },
 951      {
 952        x: 39.5,
 953        y: 7,
 954        dir: 1,
 955        dest: 4,
 956        speed: y
 957      }],
 958      11: [{
 959        x: 39.5,
 960        y: 7,
 961        dir: 1,
 962        dest: 4,
 963        speed: y
 964      }],
 965      12: [{
 966        x: 41.4,
 967        y: 7,
 968        dir: 4,
 969        dest: 39.5,
 970        speed: y
 971      },
 972      {
 973        x: 39.5,
 974        y: 7,
 975        dir: 1,
 976        dest: 4,
 977        speed: y
 978      }]
 979    },
 980    B = {
 981      1: {
 982        actors: [{
 983          ghost: e,
 984          x: 64,
 985          y: 9,
 986          id: 0
 987        },
 988        {
 989          ghost: a,
 990          x: 68.2,
 991          y: 9,
 992          id: 1
 993        }],
 994        sequence: [{
 995          time: 5.5,
 996          moves: [{
 997            dir: 4,
 998            speed: 0.75 * 0.8 * 2
 999          },
1000          {
1001            dir: 4,
1002            speed: 0.78 * 0.8 * 2
1003          }]
1004        },
1005        {
1006          time: 0.1,
1007          moves: [{
1008            dir: 4,
1009            speed: 32
1010          },
1011          {
1012            dir: 4,
1013            speed: 0
1014          }]
1015        },
1016        {
1017          time: 9,
1018          moves: [{
1019            dir: 8,
1020            speed: 0.75 * 0.8 * 2,
1021            elId: "pcm-bpcm"
1022          },
1023          {
1024            dir: 8,
1025            speed: 0.8,
1026            mode: 4
1027          }]
1028        }]
1029      },
1030      2: {
1031        actors: [{
1032          ghost: e,
1033          x: 64,
1034          y: 9,
1035          id: 0
1036        },
1037        {
1038          ghost: a,
1039          x: 70.2,
1040          y: 9,
1041          id: 1
1042        },
1043        {
1044          ghost: a,
1045          x: 32,
1046          y: 9.5,
1047          id: 2
1048        }],
1049        sequence: [{
1050          time: 2.7,
1051          moves: [{
1052            dir: 4,
1053            speed: 0.75 * 0.8 * 2
1054          },
1055          {
1056            dir: 4,
1057            speed: 0.78 * 0.8 * 2
1058          },
1059          {
1060            dir: 0,
1061            speed: 0,
1062            elId: "pcm-stck"
1063          }]
1064        },
1065        {
1066          time: 1,
1067          moves: [{
1068            dir: 4,
1069            speed: 0.75 * 0.8 * 2
1070          },
1071          {
1072            dir: 4,
1073            speed: 0.1 * 0.8
1074          },
1075          {
1076            dir: 0,
1077            speed: 0,
1078            elId: "pcm-stck"
1079          }]
1080        },
1081        {
1082          time: 1.3,
1083          moves: [{
1084            dir: 4,
1085            speed: 0.75 * 0.8 * 2
1086          },
1087          {
1088            dir: 4,
1089            speed: 0
1090          },
1091          {
1092            dir: 0,
1093            speed: 0,
1094            elId: "pcm-stck"
1095          }]
1096        },
1097        {
1098          time: 1,
1099          moves: [{
1100            dir: 4,
1101            speed: 0.75 * 0.8 * 2
1102          },
1103          {
1104            dir: 4,
1105            speed: 0,
1106            elId: "pcm-ghfa"
1107          },
1108          {
1109            dir: 0,
1110            speed: 0,
1111            elId: "pcm-stck"
1112          }]
1113        },
1114        {
1115          time: 2.5,
1116          moves: [{
1117            dir: 4,
1118            speed: 0.75 * 0.8 * 2
1119          },
1120          {
1121            dir: 4,
1122            speed: 0,
1123            elId: "pcm-ghfa"
1124          },
1125          {
1126            dir: 0,
1127            speed: 0,
1128            elId: "pcm-stck"
1129          }]
1130        }]
1131      },
1132      3: {
1133        actors: [{
1134          ghost: e,
1135          x: 64,
1136          y: 9,
1137          id: 0
1138        },
1139        {
1140          ghost: a,
1141          x: 70.2,
1142          y: 9,
1143          id: 2
1144        }],
1145        sequence: [{
1146          time: 5.3,
1147          moves: [{
1148            dir: 4,
1149            speed: 0.75 * 0.8 * 2
1150          },
1151          {
1152            dir: 4,
1153            speed: 0.78 * 0.8 * 2,
1154            elId: "pcm-ghin"
1155          }]
1156        },
1157        {
1158          time: 5.3,
1159          moves: [{
1160            dir: 4,
1161            speed: 0
1162          },
1163          {
1164            dir: 8,
1165            speed: 0.78 * 0.8 * 2,
1166            elId: "pcm-gbug"
1167          }]
1168        }]
1169      }
1170    },
1171    C = [90, 45, 30],
1172    D = C[0];
1173
1174  function E(b) {
1175    this.id = b
1176  }
1177  E.prototype.A = function () {
1178    var b = r[g.playerCount][this.id];
1179    this.pos = [b.y * 8, b.x * 8];
1180    this.posDelta = [0, 0];
1181    this.tilePos = [b.y * 8, b.x * 8];
1182    this.targetPos = [b.scatterY * 8, b.scatterX * 8];
1183    this.scatterPos = [b.scatterY * 8, b.scatterX * 8];
1184    this.lastActiveDir = this.dir = b.dir;
1185    this.physicalSpeed = this.requestedDir = this.nextDir = 0;
1186    this.c(0);
1187    this.reverseDirectionsNext = this.freeToLeavePen = this.modeChangedWhileInPen = this.eatenInThisFrightMode = e;
1188    this.l()
1189  };
1190  E.prototype.createElement = function () {
1191    this.el = document.createElement("div");
1192    this.el.className = "pcm-ac";
1193    this.el.id = "actor" + this.id;
1194    g.prepareElement(this.el, 0, 0);
1195    g.playfieldEl.appendChild(this.el);
1196    this.elPos = [0, 0];
1197    this.elBackgroundPos = [0, 0]
1198  };
1199  E.prototype.a = function (b) {
1200    var c = this.mode;
1201    this.mode = b;
1202    if (this.id == g.playerCount + 3 && (b == 16 || c == 16)) g.updateCruiseElroySpeed();
1203    switch (c) {
1204    case 32:
1205      g.ghostExitingPenNow = e;
1206      break;
1207    case 8:
1208      g.ghostEyesCount > 0 && g.ghostEyesCount--;
1209      g.ghostEyesCount == 0 && g.playAmbientSound();
1210      break
1211    }
1212    switch (b) {
1213    case 4:
1214      this.fullSpeed = g.levels.ghostFrightSpeed * 0.8;
1215      this.tunnelSpeed = g.levels.ghostTunnelSpeed * 0.8;
1216      this.followingRoutine = e;
1217      break;
1218    case 1:
1219      this.fullSpeed = g.levels.ghostSpeed * 0.8;
1220      this.tunnelSpeed = g.levels.ghostTunnelSpeed * 0.8;
1221      this.followingRoutine =
1222      e;
1223      break;
1224    case 2:
1225      this.targetPos = this.scatterPos;
1226      this.fullSpeed = g.levels.ghostSpeed * 0.8;
1227      this.tunnelSpeed = g.levels.ghostTunnelSpeed * 0.8;
1228      this.followingRoutine = e;
1229      break;
1230    case 8:
1231      this.tunnelSpeed = this.fullSpeed = 1.6;
1232      this.targetPos = [s[0], s[1]];
1233      this.freeToLeavePen = this.followingRoutine = e;
1234      break;
1235    case 16:
1236      this.l();
1237      this.followingRoutine = a;
1238      this.routineMoveId = -1;
1239      switch (this.id) {
1240      case g.playerCount + 1:
1241        this.routineToFollow = 2;
1242        break;
1243      case g.playerCount + 2:
1244        this.routineToFollow = 1;
1245        break;
1246      case g.playerCount + 3:
1247        this.routineToFollow =
1248        3;
1249        break
1250      }
1251      break;
1252    case 32:
1253      this.followingRoutine = a;
1254      this.routineMoveId = -1;
1255      switch (this.id) {
1256      case g.playerCount + 1:
1257        this.routineToFollow = 5;
1258        break;
1259      case g.playerCount + 2:
1260        this.routineToFollow = 4;
1261        break;
1262      case g.playerCount + 3:
1263        this.routineToFollow = 6;
1264        break
1265      }
1266      g.ghostExitingPenNow = a;
1267      break;
1268    case 64:
1269      this.followingRoutine = a;
1270      this.routineMoveId = -1;
1271      switch (this.id) {
1272      case g.playerCount:
1273      case g.playerCount + 1:
1274        this.routineToFollow = 8;
1275        break;
1276      case g.playerCount + 2:
1277        this.routineToFollow = 7;
1278        break;
1279      case g.playerCount + 3:
1280        this.routineToFollow = 9;
1281        break
1282      }
1283      break;
1284    case 128:
1285      this.followingRoutine = a;
1286      this.routineMoveId = -1;
1287      switch (this.id) {
1288      case g.playerCount:
1289      case g.playerCount + 1:
1290        this.routineToFollow = 11;
1291        break;
1292      case g.playerCount + 2:
1293        this.routineToFollow = 10;
1294        break;
1295      case g.playerCount + 3:
1296        this.routineToFollow = 12;
1297        break
1298      }
1299      break
1300    }
1301    this.d()
1302  };
1303  E.prototype.l = function () {
1304    if (this.id >= g.playerCount) this.targetPlayerId = Math.floor(g.rand() * g.playerCount)
1305  };
1306  E.prototype.z = function (b) {
1307    if (!g.userDisabledSound) {
1308      google.pacManSound = a;
1309      g.updateSoundIcon()
1310    }
1311    if (this.dir == g.oppositeDirections[b]) {
1312      this.dir = b;
1313      this.posDelta = [0, 0];
1314      this.currentSpeed != 2 && this.c(0);
1315      if (this.dir != 0) this.lastActiveDir = this.dir;
1316      this.nextDir = 0
1317    } else if (this.dir != b) if (this.dir == 0) {
1318      if (g.playfield[this.pos[0]][this.pos[1]].allowedDir & b) this.dir = b
1319    } else {
1320      var c = g.playfield[this.tilePos[0]][this.tilePos[1]];
1321      if (c && c.allowedDir & b) {
1322        c = l[this.dir];
1323        var d = [this.pos[0], this.pos[1]];
1324        d[c.axis] -= c.increment;
1325        var f = 0;
1326        if (d[0] == this.tilePos[0] && d[1] == this.tilePos[1]) f = 1;
1327        else {
1328          d[c.axis] -= c.increment;
1329          if (d[0] == this.tilePos[0] && d[1] == this.tilePos[1]) f = 2
1330        }
1331        if (f) {
1332          this.dir = b;
1333          this.pos[0] = this.tilePos[0];
1334          this.pos[1] = this.tilePos[1];
1335          c = l[this.dir];
1336          this.pos[c.axis] += c.increment * f;
1337          return
1338        }
1339      }
1340      this.nextDir = b;
1341      this.posDelta = [0, 0]
1342    }
1343  };
1344  E.prototype.i = function (b) {
1345    var c = this.tilePos,
1346      d = l[this.dir],
1347      f = [c[0], c[1]];
1348    f[d.axis] += d.increment * 8;
1349    var h = g.playfield[f[0]][f[1]];
1350    if (b && !h.intersection) h = g.playfield[c[0]][c[1]];
1351    if (h.intersection) switch (this.mode) {
1352    case 2:
1353    case 1:
1354    case 8:
1355      if ((this.dir & h.allowedDir) == 0 && h.allowedDir == g.oppositeDirections[this.dir]) this.nextDir = g.oppositeDirections[this.dir];
1356      else {
1357        b = 99999999999;
1358        c = 0;
1359        for (var j in i) {
1360          var k = i[j];
1361          if (h.allowedDir & k && this.dir != g.oppositeDirections[k]) {
1362            d = l[k];
1363            var x = [f[0], f[1]];
1364            x[d.axis] += d.increment;
1365            d = g.getDistance(x, [this.targetPos[0], this.targetPos[1]]);
1366            if (d < b) {
1367              b = d;
1368              c = k
1369            }
1370          }
1371        }
1372        if (c) this.nextDir = c
1373      }
1374      break;
1375    case 4:
1376      if ((this.dir & h.allowedDir) == 0 && h.allowedDir == g.oppositeDirections[this.dir]) this.nextDir = g.oppositeDirections[this.dir];
1377      else {
1378        do f = i[Math.floor(g.rand() * 4)];
1379        while ((f & h.allowedDir) == 0 || f == g.oppositeDirections[this.dir]);
1380        this.nextDir = f
1381      }
1382      break
1383    }
1384  };
1385  E.prototype.p = function (b) {
1386    g.tilesChanged = a;
1387    if (this.reverseDirectionsNext) {
1388      this.dir = g.oppositeDirections[this.dir];
1389      this.nextDir = 0;
1390      this.reverseDirectionsNext = e;
1391      this.i(a)
1392    }
1393    if (!this.ghost && !g.playfield[b[0]][b[1]].path) {
1394      this.pos[0] = this.lastGoodTilePos[0];
1395      this.pos[1] = this.lastGoodTilePos[1];
1396      b[0] = this.lastGoodTilePos[0];
1397      b[1] = this.lastGoodTilePos[1];
1398      this.dir = 0
1399    } else this.lastGoodTilePos = [b[0], b[1]];
1400    g.playfield[b[0]][b[1]].type == 1 && this.mode != 8 ? this.c(2) : this.c(0);
1401    !this.ghost && g.playfield[b[0]][b[1]].dot && g.dotEaten(this.id, b);
1402    this.tilePos[0] = b[0];
1403    this.tilePos[1] = b[1]
1404  };
1405  E.prototype.t = function () {
1406    var b = this.tilePos;
1407    switch (this.dir) {
1408    case 1:
1409      var c = [b[0], b[1]],
1410        d = [b[0] + 3.6, b[1]];
1411      break;
1412    case 2:
1413      c = [b[0] - 4, b[1]];
1414      d = [b[0], b[1]];
1415      break;
1416    case 4:
1417      c = [b[0], b[1]];
1418      d = [b[0], b[1] + 3.6];
1419      break;
1420    case 8:
1421      c = [b[0], b[1] - 4];
1422      d = [b[0], b[1]];
1423      break
1424    }
1425    if (this.pos[0] >= c[0] && this.pos[0] <= d[0] && this.pos[1] >= c[1] && this.pos[1] <= d[1]) {
1426      b = l[this.nextDir];
1427      this.posDelta[b.axis] += b.increment
1428    }
1429  };
1430  E.prototype.n = function () {
1431    if (this.pos[0] == q[0].y * 8 && this.pos[1] == q[0].x * 8) {
1432      this.pos[0] = q[1].y * 8;
1433      this.pos[1] = (q[1].x - 1) * 8
1434    } else if (this.pos[0] == q[1].y * 8 && this.pos[1] == q[1].x * 8) {
1435      this.pos[0] = q[0].y * 8;
1436      this.pos[1] = (q[0].x + 1) * 8
1437    }
1438    this.mode == 8 && this.pos[0] == s[0] && this.pos[1] == s[1] && this.a(64);
1439    if (!this.ghost && this.pos[0] == v[0] && (this.pos[1] == v[1] || this.pos[1] == v[1] + 8)) g.eatFruit(this.id)
1440  };
1441  E.prototype.u = function () {
1442    this.n();
1443    this.ghost && this.i(e);
1444    var b = g.playfield[this.pos[0]][this.pos[1]];
1445    if (b.intersection) if (this.nextDir && this.nextDir & b.allowedDir) {
1446      if (this.dir != 0) this.lastActiveDir = this.dir;
1447      this.dir = this.nextDir;
1448      this.nextDir = 0;
1449      if (!this.ghost) {
1450        this.pos[0] += this.posDelta[0];
1451        this.pos[1] += this.posDelta[1];
1452        this.posDelta = [0, 0]
1453      }
1454    } else if ((this.dir & b.allowedDir) == 0) {
1455      if (this.dir != 0) this.lastActiveDir = this.dir;
1456      this.nextDir = this.dir = 0;
1457      this.c(0)
1458    }
1459  };
1460  E.prototype.o = function () {
1461    var b = this.pos[0] / 8,
1462      c = this.pos[1] / 8,
1463      d = [Math.round(b) * 8, Math.round(c) * 8];
1464    if (d[0] != this.tilePos[0] || d[1] != this.tilePos[1]) this.p(d);
1465    else {
1466      b = [Math.floor(b) * 8, Math.floor(c) * 8];
1467      this.pos[1] == b[1] && this.pos[0] == b[0] && this.u()
1468    }!this.ghost && this.nextDir && g.playfield[d[0]][d[1]].intersection && this.nextDir & g.playfield[d[0]][d[1]].allowedDir && this.t()
1469  };
1470  E.prototype.B = function () {
1471    if (this.id == g.playerCount && g.dotsRemaining < g.levels.elroyDotsLeftPart1 && this.mode == 2 && (!g.lostLifeOnThisLevel || g.actors[g.playerCount + 3].mode != 16)) {
1472      var b = g.actors[this.targetPlayerId];
1473      this.targetPos = [b.tilePos[0], b.tilePos[1]]
1474    } else if (this.ghost && this.mode == 1) {
1475      b = g.actors[this.targetPlayerId];
1476      switch (this.id) {
1477      case g.playerCount:
1478        this.targetPos = [b.tilePos[0], b.tilePos[1]];
1479        break;
1480      case g.playerCount + 1:
1481        this.targetPos = [b.tilePos[0], b.tilePos[1]];
1482        var c = l[b.dir];
1483        this.targetPos[c.axis] += 32 * c.increment;
1484        if (b.dir == 1) this.targetPos[1] -= 32;
1485        break;
1486      case g.playerCount + 2:
1487        var d = g.actors[g.playerCount],
1488          f = [b.tilePos[0], b.tilePos[1]];
1489        c = l[b.dir];
1490        f[c.axis] += 16 * c.increment;
1491        if (b.dir == 1) f[1] -= 16;
1492        this.targetPos[0] = f[0] * 2 - d.tilePos[0];
1493        this.targetPos[1] = f[1] * 2 - d.tilePos[1];
1494        break;
1495      case g.playerCount + 3:
1496        c = g.getDistance(b.tilePos, this.tilePos);
1497        this.targetPos = c > 64 ? [b.tilePos[0], b.tilePos[1]] : this.scatterPos;
1498        break
1499      }
1500    }
1501  };
1502  E.prototype.v = function () {
1503    this.routineMoveId++;
1504    if (this.routineMoveId == A[this.routineToFollow].length) if (this.mode == 16 && this.freeToLeavePen && !g.ghostExitingPenNow) {
1505      this.eatenInThisFrightMode ? this.a(128) : this.a(32);
1506      return
1507    } else if (this.mode == 32 || this.mode == 128) {
1508      this.pos = [s[0], s[1] + 4];
1509      this.dir = this.modeChangedWhileInPen ? 8 : 4;
1510      var b = g.mainGhostMode;
1511      if (this.mode == 128 && b == 4) b = g.lastMainGhostMode;
1512      this.a(b);
1513      return
1514    } else if (this.mode == 64) {
1515      if (this.id == g.playerCount || this.freeToLeavePen) this.a(128);
1516      else {
1517        this.eatenInThisFrightMode =
1518        a;
1519        this.a(16)
1520      }
1521      return
1522    } else this.routineMoveId = 0;
1523    b = A[this.routineToFollow][this.routineMoveId];
1524    this.pos[0] = b.y * 8;
1525    this.pos[1] = b.x * 8;
1526    this.dir = b.dir;
1527    this.physicalSpeed = 0;
1528    this.speedIntervals = g.getSpeedIntervals(b.speed);
1529    this.proceedToNextRoutineMove = e;
1530    this.b()
1531  };
1532  E.prototype.m = function () {
1533    var b = A[this.routineToFollow][this.routineMoveId];
1534    if (b) if (this.speedIntervals[g.intervalTime]) {
1535      var c = l[this.dir];
1536      this.pos[c.axis] += c.increment;
1537      switch (this.dir) {
1538      case 1:
1539      case 4:
1540        if (this.pos[c.axis] < b.dest * 8) {
1541          this.pos[c.axis] = b.dest * 8;
1542          this.proceedToNextRoutineMove = a
1543        }
1544        break;
1545      case 2:
1546      case 8:
1547        if (this.pos[c.axis] > b.dest * 8) {
1548          this.pos[c.axis] = b.dest * 8;
1549          this.proceedToNextRoutineMove = a
1550        }
1551        break
1552      }
1553      this.b()
1554    }
1555  };
1556  E.prototype.j = function () {
1557    if (this.routineMoveId == -1 || this.proceedToNextRoutineMove) this.v();
1558    this.m()
1559  };
1560  E.prototype.d = function () {
1561    switch (this.currentSpeed) {
1562    case 0:
1563      var b = this.id == g.playerCount && (this.mode == 2 || this.mode == 1) ? g.cruiseElroySpeed : this.fullSpeed;
1564      break;
1565    case 1:
1566      b = this.dotEatingSpeed;
1567      break;
1568    case 2:
1569      b = this.tunnelSpeed;
1570      break
1571    }
1572    if (this.physicalSpeed != b) {
1573      this.physicalSpeed = b;
1574      this.speedIntervals = g.getSpeedIntervals(this.physicalSpeed)
1575    }
1576  };
1577  E.prototype.c = function (b) {
1578    this.currentSpeed = b;
1579    this.d()
1580  };
1581  E.prototype.e = function () {
1582    if (this.dir) if (this.speedIntervals[g.intervalTime]) {
1583      var b = l[this.dir];
1584      this.pos[b.axis] += b.increment;
1585      this.o();
1586      this.b()
1587    }
1588  };
1589  E.prototype.move = function () {
1590    if (g.gameplayMode == 0 || this.ghost && g.gameplayMode == 1 && (this.mode == 8 || this.mode == 64)) {
1591      if (this.requestedDir != 0) {
1592        this.z(this.requestedDir);
1593        this.requestedDir = 0
1594      }
1595      if (this.followingRoutine) {
1596        this.j();
1597        this.mode == 64 && this.j()
1598      } else {
1599        this.e();
1600        this.mode == 8 && this.e()
1601      }
1602    }
1603  };
1604  E.prototype.k = function () {
1605    var b = g.getPlayfieldX(this.pos[1] + this.posDelta[1]),
1606      c = g.getPlayfieldY(this.pos[0] + this.posDelta[0]);
1607    if (this.elPos[0] != c || this.elPos[1] != b) {
1608      this.elPos[0] = c;
1609      this.elPos[1] = b;
1610      this.el.style.left = b + "px";
1611      this.el.style.top = c + "px"
1612    }
1613  };
1614  E.prototype.s = function () {
1615    var b = 0,
1616      c = 0,
1617      d = this.dir;
1618    if (d == 0) d = this.lastActiveDir;
1619    if (g.gameplayMode == 1 && this.id == g.playerEatingGhostId) {
1620      b = 3;
1621      c = 0
1622    } else if ((g.gameplayMode == 9 || g.gameplayMode == 10) && this.id == 0) {
1623      b = 2;
1624      c = 0
1625    } else if (g.gameplayMode == 4 || g.gameplayMode == 5 || g.gameplayMode == 7) {
1626      b = this.id == 0 ? 2 : 4;
1627      c = 0
1628    } else if (g.gameplayMode == 3) if (this.id == g.playerDyingId) {
1629      d = 20 - Math.floor(g.gameplayModeTime / g.timing[4] * 21);
1630      if (this.id == 0) {
1631        b = d - 1;
1632        switch (b) {
1633        case -1:
1634          b = 0;
1635          break;
1636        case 11:
1637          b = 10;
1638          break;
1639        case 12:
1640        case 13:
1641        case 14:
1642        case 15:
1643        case 16:
1644        case 17:
1645        case 18:
1646        case 19:
1647        case 20:
1648          b =
1649          11;
1650          break
1651        }
1652        c = 12
1653      } else switch (d) {
1654      case 0:
1655      case 1:
1656      case 2:
1657      case 6:
1658      case 10:
1659        b = 4;
1660        c = 3;
1661        break;
1662      case 3:
1663      case 7:
1664      case 11:
1665        b = 4;
1666        c = 0;
1667        break;
1668      case 4:
1669      case 8:
1670      case 12:
1671      case 13:
1672      case 14:
1673      case 15:
1674      case 16:
1675      case 17:
1676      case 18:
1677      case 19:
1678      case 20:
1679        b = 4;
1680        c = 2;
1681        break;
1682      case 5:
1683      case 9:
1684        b = 4;
1685        c = 1;
1686        break
1687      }
1688    } else {
1689      b = 3;
1690      c = 0
1691    } else if (this.el.id == "pcm-bpcm") {
1692      b = 14;
1693      c = 0;
1694      d = Math.floor(g.globalTime * 0.2) % 4;
1695      if (d == 3) d = 1;
1696      c += 2 * d
1697    } else {
1698      switch (d) {
1699      case 4:
1700        c = 0;
1701        break;
1702      case 8:
1703        c = 1;
1704        break;
1705      case 1:
1706        c = 2;
1707        break;
1708      case 2:
1709        c = 3;
1710        break
1711      }
1712      if (g.gameplayMode != 2) b = Math.floor(g.globalTime * 0.3) % 4;
1713      if (b == 3 && this.dir == 0) b = 0;
1714      if (b == 2 && this.id == 0) b = 0;
1715      if (b == 3) {
1716        b = 2;
1717        if (this.id == 0) c = 0
1718      }
1719      if (this.id == 1) b += 4
1720    }
1721    return [c, b]
1722  };
1723  E.prototype.r = function () {
1724    var b = 0,
1725      c = 0;
1726    if (g.gameplayMode == 10 || g.gameplayMode == 4 || g.gameplayMode == 3) {
1727      b = 3;
1728      c = 0
1729    } else if (g.gameplayMode == 1 && this.id == g.ghostBeingEatenId) {
1730      switch (g.modeScoreMultiplier) {
1731      case 2:
1732        b = 0;
1733        break;
1734      case 4:
1735        b = 1;
1736        break;
1737      case 8:
1738        b = 2;
1739        break;
1740      case 16:
1741        b = 3;
1742        break
1743      }
1744      c = 11;
1745      this.el.className = "pcm-ac pcm-n"
1746    } else if (this.mode == 4 || (this.mode == 16 || this.mode == 32) && g.mainGhostMode == 4 && !this.eatenInThisFrightMode) {
1747      b = 0;
1748      c = 8;
1749      if (g.frightModeTime < g.levels.frightTotalTime - g.levels.frightTime && Math.floor(g.frightModeTime / g.timing[1]) % 2 == 0) b += 2;
1750      b += Math.floor(g.globalTime / 16) % 2
1751    } else if (this.mode == 8 || this.mode == 64) {
1752      c = this.nextDir;
1753      if (!c) c = this.dir;
1754      switch (c) {
1755      case 4:
1756        b = 2;
1757        break;
1758      case 8:
1759        b = 3;
1760        break;
1761      case 1:
1762        b = 0;
1763        break;
1764      case 2:
1765        b = 1;
1766        break
1767      }
1768      c = 10
1769    } else if (this.el.id == "pcm-ghin") {
1770      b = 6;
1771      c = 8;
1772      b += Math.floor(g.globalTime / 16) % 2
1773    } else if (this.el.id == "pcm-gbug") {
1774      b = 6;
1775      c = 9;
1776      c += Math.floor(g.globalTime / 16) % 2
1777    } else if (this.el.id == "pcm-ghfa") {
1778      b = g.cutsceneSequenceId == 3 ? 6 : 7;
1779      c = 11
1780    } else if (this.el.id == "pcm-stck") {
1781      b = g.cutsceneSequenceId == 1 ? g.cutsceneTime > 60 ? 1 : g.cutsceneTime > 45 ? 2 : 3 : g.cutsceneSequenceId == 2 ? 3 : g.cutsceneSequenceId == 3 || g.cutsceneSequenceId == 4 ? 4 : 0;
1782      c = 13
1783    } else {
1784      c = this.nextDir;
1785      if (!c || g.playfield[this.tilePos[0]][this.tilePos[1]].type == 1) c = this.dir;
1786      switch (c) {
1787      case 4:
1788        b = 4;
1789        break;
1790      case 8:
1791        b = 6;
1792        break;
1793      case 1:
1794        b = 0;
1795        break;
1796      case 2:
1797        b = 2;
1798        break
1799      }
1800      c = 4 + this.id - g.playerCount;
1801      if (this.speed > 0 || g.gameplayMode != 13) b += Math.floor(g.globalTime / 16) % 2
1802    }
1803    return [c, b]
1804  };
1805  E.prototype.b = function () {
1806    this.k();
1807    var b = [0, 0];
1808    b = g.gameplayMode == 8 || g.gameplayMode == 14 ? [0, 3] : this.ghost ? this.r() : this.s();
1809    if (this.elBackgroundPos[0] != b[0] || this.elBackgroundPos[1] != b[1]) {
1810      this.elBackgroundPos[0] = b[0];
1811      this.elBackgroundPos[1] = b[1];
1812      b[0] *= 16;
1813      b[1] *= 16;
1814      g.changeElementBkPos(this.el, b[1], b[0], a)
1815    }
1816  };
1817  g.rand = function () {
1818    var b = 4294967296,
1819      c = 134775813;
1820    c = c * g.randSeed + 1;
1821    return (g.randSeed = c % b) / b
1822  };
1823  g.seed = function (b) {
1824    g.randSeed = b
1825  };
1826  g.getDistance = function (b, c) {
1827    return Math.sqrt((c[1] - b[1]) * (c[1] - b[1]) + (c[0] - b[0]) * (c[0] - b[0]))
1828  };
1829  g.getPlayfieldX = function (b) {
1830    return b + -32
1831  };
1832  g.getPlayfieldY = function (b) {
1833    return b + 0
1834  };
1835  g.getCorrectedSpritePos = function (b) {
1836    return b / 8 * 10 + 2
1837  };
1838  g.getDotElementId = function (b, c) {
1839    return "pcm-d" + b + "-" + c
1840  };
1841  g.showElementById = function (b, c) {
1842    var d = document.getElementById(b);
1843    if (d) d.style.visibility = c ? "visible" : "hidden"
1844  };
1845  g.getAbsoluteElPos = function (b) {
1846    var c = [0, 0];
1847    do {
1848      c[0] += b.offsetTop;
1849      c[1] += b.offsetLeft
1850    } while (b = b.offsetParent);
1851    return c
1852  };
1853  g.prepareElement = function (b, c, d) {
1854    c = g.getCorrectedSpritePos(parseInt(c, 10));
1855    d = g.getCorrectedSpritePos(parseInt(d, 10));
1856    if (g.useCss) {
1857      b.style.backgroundImage = "url(src/pacman10-hp-sprite-2.png)";
1858      b.style.backgroundPosition = -c + "px " + -d + "px";
1859      b.style.backgroundRepeat = "no-repeat"
1860    } else {
1861      b.style.overflow = "hidden";
1862      c = "display: block; position: relative; left: " + -c + "px; top: " + -d + "px";
1863      b.innerHTML = '<img style="' + c + '" src="src/pacman10-hp-sprite-2.png">'
1864    }
1865  };
1866  g.changeElementBkPos = function (b, c, d, f) {
1867    if (f) {
1868      c = g.getCorrectedSpritePos(c);
1869      d = g.getCorrectedSpritePos(d)
1870    }
1871    if (g.useCss) b.style.backgroundPosition = -c + "px " + -d + "px";
1872    else if (b.childNodes[0]) {
1873      b.childNodes[0].style.left = -c + "px";
1874      b.childNodes[0].style.top = -d + "px"
1875    }
1876  };
1877  g.determinePlayfieldDimensions = function () {
1878    g.playfieldWidth = 0;
1879    g.playfieldHeight = 0;
1880    for (var b in n) {
1881      var c = n[b];
1882      if (c.w) {
1883        c = c.x + c.w - 1;
1884        if (c > g.playfieldWidth) g.playfieldWidth = c
1885      } else {
1886        c = c.y + c.h - 1;
1887        if (c > g.playfieldHeight) g.playfieldHeight = c
1888      }
1889    }
1890  };
1891  g.preparePlayfield = function () {
1892    g.playfield = [];
1893    for (var b = 0; b <= g.playfieldHeight + 1; b++) {
1894      g.playfield[b * 8] = [];
1895      for (var c = -2; c <= g.playfieldWidth + 1; c++) g.playfield[b * 8][c * 8] = {
1896        path: 0,
1897        dot: 0,
1898        intersection: 0
1899      }
1900    }
1901  };
1902  g.preparePaths = function () {
1903    for (var b in n) {
1904      var c = n[b],
1905        d = c.type;
1906      if (c.w) {
1907        for (var f = c.y * 8, h = c.x * 8; h <= (c.x + c.w - 1) * 8; h += 8) {
1908          g.playfield[f][h].path = a;
1909          if (g.playfield[f][h].dot == 0) {
1910            g.playfield[f][h].dot = 1;
1911            g.dotsRemaining++
1912          }
1913          g.playfield[f][h].type = !d || h != c.x * 8 && h != (c.x + c.w - 1) * 8 ? d : 0
1914        }
1915        g.playfield[f][c.x * 8].intersection = a;
1916        g.playfield[f][(c.x + c.w - 1) * 8].intersection = a
1917      } else {
1918        h = c.x * 8;
1919        for (f = c.y * 8; f <= (c.y + c.h - 1) * 8; f += 8) {
1920          if (g.playfield[f][h].path) g.playfield[f][h].intersection = a;
1921          g.playfield[f][h].path = a;
1922          if (g.playfield[f][h].dot == 0) {
1923            g.playfield[f][h].dot = 1;
1924            g.dotsRemaining++
1925          }
1926          g.playfield[f][h].type = !d || f != c.y * 8 && f != (c.y + c.h - 1) * 8 ? d : 0
1927        }
1928        g.playfield[c.y * 8][h].intersection = a;
1929        g.playfield[(c.y + c.h - 1) * 8][h].intersection = a
1930      }
1931    }
1932    for (b in o) if (o[b].w) for (h = o[b].x * 8; h <= (o[b].x + o[b].w - 1) * 8; h += 8) {
1933      g.playfield[o[b].y * 8][h].dot = 0;
1934      g.dotsRemaining--
1935    } else for (f = o[b].y * 8; f <= (o[b].y + o[b].h - 1) * 8; f += 8) {
1936      g.playfield[f][o[b].x * 8].dot = 0;
1937      g.dotsRemaining--
1938    }
1939  };
1940  g.prepareAllowedDirections = function () {
1941    for (var b = 8; b <= g.playfieldHeight * 8; b += 8) for (var c = 8; c <= g.playfieldWidth * 8; c += 8) {
1942      g.playfield[b][c].allowedDir = 0;
1943      if (g.playfield[b - 8][c].path) g.playfield[b][c].allowedDir += 1;
1944      if (g.playfield[b + 8][c].path) g.playfield[b][c].allowedDir += 2;
1945      if (g.playfield[b][c - 8].path) g.playfield[b][c].allowedDir += 4;
1946      if (g.playfield[b][c + 8].path) g.playfield[b][c].allowedDir += 8
1947    }
1948  };
1949  g.createDotElements = function () {
1950    for (var b = 8; b <= g.playfieldHeight * 8; b += 8) for (var c = 8; c <= g.playfieldWidth * 8; c += 8) if (g.playfield[b][c].dot) {
1951      var d = document.createElement("div");
1952      d.className = "pcm-d";
1953      d.id = g.getDotElementId(b, c);
1954      d.style.left = c + -32 + "px";
1955      d.style.top = b + 0 + "px";
1956      g.playfieldEl.appendChild(d)
1957    }
1958  };
1959  g.createEnergizerElements = function () {
1960    for (var b in p) {
1961      var c = p[b],
1962        d = g.getDotElementId(c.y * 8, c.x * 8);
1963      document.getElementById(d).className = "pcm-e";
1964      g.prepareElement(document.getElementById(d), 0, 144);
1965      g.playfield[c.y * 8][c.x * 8].dot = 2
1966    }
1967  };
1968  g.createFruitElement = function () {
1969    g.fruitEl = document.createElement("div");
1970    g.fruitEl.id = "pcm-f";
1971    g.fruitEl.style.left = g.getPlayfieldX(v[1]) + "px";
1972    g.fruitEl.style.top = g.getPlayfieldY(v[0]) + "px";
1973    g.prepareElement(g.fruitEl, -32, -16);
1974    g.playfieldEl.appendChild(g.fruitEl)
1975  };
1976  g.createPlayfieldElements = function () {
1977    g.doorEl = document.createElement("div");
1978    g.doorEl.id = "pcm-do";
1979    g.doorEl.style.display = "none";
1980    g.playfieldEl.appendChild(g.doorEl);
1981    g.createDotElements();
1982    g.createEnergizerElements();
1983    g.createFruitElement()
1984  };
1985  g.createActors = function () {
1986    g.actors = [];
1987    for (var b = 0; b < g.playerCount + 4; b++) {
1988      g.actors[b] = new E(b);
1989      if (b < g.playerCount) {
1990        g.actors[b].ghost = e;
1991        g.actors[b].mode = 1
1992      } else g.actors[b].ghost = a
1993    }
1994  };
1995  g.restartActors = function () {
1996    for (var b in g.actors) g.actors[b].A()
1997  };
1998  g.createActorElements = function () {
1999    for (var b in g.actors) g.actors[b].createElement()
2000  };
2001  g.createPlayfield = function () {
2002    g.playfieldEl = document.createElement("div");
2003    g.playfieldEl.id = "pcm-p";
2004    g.canvasEl.appendChild(g.playfieldEl)
2005  };
2006  g.resetPlayfield = function () {
2007    g.dotsRemaining = 0;
2008    g.dotsEaten = 0;
2009    g.playfieldEl.innerHTML = "";
2010    g.prepareElement(g.playfieldEl, 256, 0);
2011    g.determinePlayfieldDimensions();
2012    g.preparePlayfield();
2013    g.preparePaths();
2014    g.prepareAllowedDirections();
2015    g.createPlayfieldElements();
2016    g.createActorElements()
2017  };
2018  g.keyPressed = function (b) {
2019    var c = e;
2020    switch (b) {
2021    case 37:
2022      g.actors[0].requestedDir = 4;
2023      c = a;
2024      break;
2025    case 38:
2026      g.actors[0].requestedDir = 1;
2027      c = a;
2028      break;
2029    case 39:
2030      g.actors[0].requestedDir = 8;
2031      c = a;
2032      break;
2033    case 40:
2034      g.actors[0].requestedDir = 2;
2035      c = a;
2036      break;
2037    case 65:
2038      if (g.playerCount == 2) {
2039        g.actors[1].requestedDir = 4;
2040        c = a
2041      }
2042      break;
2043    case 83:
2044      if (g.playerCount == 2) {
2045        g.actors[1].requestedDir = 2;
2046        c = a
2047      }
2048      break;
2049    case 68:
2050      if (g.playerCount == 2) {
2051        g.actors[1].requestedDir = 8;
2052        c = a
2053      }
2054      break;
2055    case 87:
2056      if (g.playerCount == 2) {
2057        g.actors[1].requestedDir = 1;
2058        c = a
2059      }
2060      break
2061    }
2062    return c
2063  };
2064  g.handleKeyDown = function (b) {
2065    if (!b) b = window.event;
2066    if (g.keyPressed(b.keyCode)) if (b.preventDefault) b.preventDefault();
2067    else b.returnValue = e
2068  };
2069  g.canvasClicked = function (b, c) {
2070    var d = g.getAbsoluteElPos(g.canvasEl);
2071    b -= d[1] - -32;
2072    c -= d[0] - 0;
2073    d = g.actors[0];
2074    var f = g.getPlayfieldX(d.pos[1] + d.posDelta[1]) + 16,
2075      h = g.getPlayfieldY(d.pos[0] + d.posDelta[0]) + 32,
2076      j = Math.abs(b - f),
2077      k = Math.abs(c - h);
2078    if (j > 8 && k < j) d.requestedDir = b > f ? 8 : 4;
2079    else if (k > 8 && j < k) d.requestedDir = c > h ? 2 : 1
2080  };
2081  g.handleClick = function (b) {
2082    if (!b) b = window.event;
2083    g.canvasClicked(b.clientX, b.clientY)
2084  };
2085  g.registerTouch = function () {
2086    document.body.addEventListener("touchstart", g.handleTouchStart, a);
2087    g.canvasEl.addEventListener("touchstart", g.handleTouchStart, a);
2088    document.f && document.f.q && document.f.q.addEventListener("touchstart", g.handleTouchStart, a)
2089  };
2090  g.handleTouchStart = function (b) {
2091    g.touchDX = 0;
2092    g.touchDY = 0;
2093    if (b.touches.length == 1) {
2094      g.touchStartX = b.touches[0].pageX;
2095      g.touchStartY = b.touches[0].pageY;
2096      document.body.addEventListener("touchmove", g.handleTouchMove, a);
2097      document.body.addEventListener("touchend", g.handleTouchEnd, a)
2098    }
2099    b.preventDefault();
2100    b.stopPropagation()
2101  };
2102  g.handleTouchMove = function (b) {
2103    if (b.touches.length > 1) g.cancelTouch();
2104    else {
2105      g.touchDX = b.touches[0].pageX - g.touchStartX;
2106      g.touchDY = b.touches[0].pageY - g.touchStartY
2107    }
2108    b.preventDefault();
2109    b.stopPropagation()
2110  };
2111  g.handleTouchEnd = function (b) {
2112    if (g.touchDX == 0 && g.touchDY == 0) g.canvasClicked(g.touchStartX, g.touchStartY);
2113    else {
2114      var c = Math.abs(g.touchDX),
2115        d = Math.abs(g.touchDY);
2116      if (c < 8 && d < 8) g.canvasClicked(g.touchStartX, g.touchStartY);
2117      else if (c > 15 && d < c * 2 / 3) g.actors[0].requestedDir = g.touchDX > 0 ? 8 : 4;
2118      else if (d > 15 && c < d * 2 / 3) g.actors[0].requestedDir = g.touchDY > 0 ? 2 : 1
2119    }
2120    b.preventDefault();
2121    b.stopPropagation();
2122   …
Large files files are truncated, but you can click here to view the full file

searchcode is proudly made in Sydney by ben boyter
