---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b30ae24d384667aa8d399f03c76ab886b2faa1c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523283"
---
# <span data-ttu-id="b5124-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="b5124-101">New-DataDiskObject</span></span>

## <span data-ttu-id="b5124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5124-102">SYNOPSIS</span></span>
<span data-ttu-id="b5124-103">새 가상 컴퓨터 플랫폼 이미지를 만드는 데 사용 되는 데이터 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="b5124-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5124-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5124-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5124-105">DESCRIPTION</span></span>
<span data-ttu-id="b5124-106">데이터 디스크에 대 한 정보를 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="b5124-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5124-107">EXAMPLES</span></span>

### <span data-ttu-id="b5124-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5124-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="b5124-109">새 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-109">Create a new data disk object.</span></span>

## <span data-ttu-id="b5124-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5124-110">PARAMETERS</span></span>

### <span data-ttu-id="b5124-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="b5124-111">-Lun</span></span>
<span data-ttu-id="b5124-112">논리 단위 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-112">Logical unit number.</span></span>

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

### <span data-ttu-id="b5124-113">-Uri</span><span class="sxs-lookup"><span data-stu-id="b5124-113">-Uri</span></span>
<span data-ttu-id="b5124-114">디스크 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="b5124-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5124-115">CommonParameters</span></span>
<span data-ttu-id="b5124-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5124-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5124-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5124-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5124-118">입력</span><span class="sxs-lookup"><span data-stu-id="b5124-118">INPUTS</span></span>

## <span data-ttu-id="b5124-119">출력</span><span class="sxs-lookup"><span data-stu-id="b5124-119">OUTPUTS</span></span>

## <span data-ttu-id="b5124-120">상속자</span><span class="sxs-lookup"><span data-stu-id="b5124-120">NOTES</span></span>

## <span data-ttu-id="b5124-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5124-121">RELATED LINKS</span></span>

