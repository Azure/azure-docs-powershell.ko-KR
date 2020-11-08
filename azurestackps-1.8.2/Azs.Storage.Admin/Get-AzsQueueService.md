---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046898"
---
# <span data-ttu-id="500de-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="500de-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="500de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500de-102">SYNOPSIS</span></span>
<span data-ttu-id="500de-103">대기열 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="500de-103">Returns the queue service.</span></span>

## <span data-ttu-id="500de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="500de-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="500de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="500de-105">DESCRIPTION</span></span>
<span data-ttu-id="500de-106">대기열 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="500de-106">Returns the queue service.</span></span>

## <span data-ttu-id="500de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="500de-107">EXAMPLES</span></span>

### <span data-ttu-id="500de-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="500de-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="500de-109">큐 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="500de-109">Get the queue service.</span></span>

## <span data-ttu-id="500de-110">변수</span><span class="sxs-lookup"><span data-stu-id="500de-110">PARAMETERS</span></span>

### <span data-ttu-id="500de-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="500de-111">-FarmName</span></span>
<span data-ttu-id="500de-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="500de-112">Farm Id.</span></span>

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

### <span data-ttu-id="500de-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500de-113">-ResourceGroupName</span></span>
<span data-ttu-id="500de-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="500de-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500de-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500de-115">CommonParameters</span></span>
<span data-ttu-id="500de-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="500de-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500de-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500de-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500de-118">입력</span><span class="sxs-lookup"><span data-stu-id="500de-118">INPUTS</span></span>

## <span data-ttu-id="500de-119">출력</span><span class="sxs-lookup"><span data-stu-id="500de-119">OUTPUTS</span></span>

### <span data-ttu-id="500de-120">QueueService. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="500de-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="500de-121">상속자</span><span class="sxs-lookup"><span data-stu-id="500de-121">NOTES</span></span>

## <span data-ttu-id="500de-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="500de-122">RELATED LINKS</span></span>
