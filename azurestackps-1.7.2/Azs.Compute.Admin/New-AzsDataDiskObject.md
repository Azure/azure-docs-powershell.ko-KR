---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873956"
---
# <span data-ttu-id="51f2a-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="51f2a-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="51f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="51f2a-103">새 가상 컴퓨터 플랫폼 이미지를 만드는 데 사용 되는 데이터 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="51f2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51f2a-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="51f2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="51f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="51f2a-106">데이터 디스크에 대 한 정보를 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="51f2a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="51f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="51f2a-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="51f2a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="51f2a-109">새 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-109">Create a new data disk object.</span></span>

## <span data-ttu-id="51f2a-110">변수</span><span class="sxs-lookup"><span data-stu-id="51f2a-110">PARAMETERS</span></span>

### <span data-ttu-id="51f2a-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="51f2a-111">-Lun</span></span>
<span data-ttu-id="51f2a-112">논리 단위 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f2a-113">-Uri</span><span class="sxs-lookup"><span data-stu-id="51f2a-113">-Uri</span></span>
<span data-ttu-id="51f2a-114">디스크 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f2a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f2a-115">CommonParameters</span></span>
<span data-ttu-id="51f2a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51f2a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f2a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f2a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f2a-118">입력</span><span class="sxs-lookup"><span data-stu-id="51f2a-118">INPUTS</span></span>

## <span data-ttu-id="51f2a-119">출력</span><span class="sxs-lookup"><span data-stu-id="51f2a-119">OUTPUTS</span></span>

## <span data-ttu-id="51f2a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="51f2a-120">NOTES</span></span>

## <span data-ttu-id="51f2a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51f2a-121">RELATED LINKS</span></span>

