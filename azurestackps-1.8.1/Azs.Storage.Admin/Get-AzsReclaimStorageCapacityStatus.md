---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875105"
---
# <span data-ttu-id="5c834-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="5c834-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="5c834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c834-102">SYNOPSIS</span></span>
<span data-ttu-id="5c834-103">가비지 수집 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="5c834-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c834-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c834-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c834-105">DESCRIPTION</span></span>
<span data-ttu-id="5c834-106">가비지 수집 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="5c834-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c834-107">EXAMPLES</span></span>

### <span data-ttu-id="5c834-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c834-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="5c834-109">가비지 수집 상태에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="5c834-110">변수</span><span class="sxs-lookup"><span data-stu-id="5c834-110">PARAMETERS</span></span>

### <span data-ttu-id="5c834-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5c834-111">-FarmName</span></span>
<span data-ttu-id="5c834-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c834-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="5c834-113">-JobId</span></span>
<span data-ttu-id="5c834-114">작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c834-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c834-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c834-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c834-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c834-117">CommonParameters</span></span>
<span data-ttu-id="5c834-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c834-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c834-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c834-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c834-120">입력</span><span class="sxs-lookup"><span data-stu-id="5c834-120">INPUTS</span></span>

## <span data-ttu-id="5c834-121">출력</span><span class="sxs-lookup"><span data-stu-id="5c834-121">OUTPUTS</span></span>

## <span data-ttu-id="5c834-122">상속자</span><span class="sxs-lookup"><span data-stu-id="5c834-122">NOTES</span></span>

## <span data-ttu-id="5c834-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c834-123">RELATED LINKS</span></span>
