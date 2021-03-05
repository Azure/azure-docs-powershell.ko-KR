---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.DigitalTwins/new-AzDigitalTwinsCheckNameRequestObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
ms.openlocfilehash: 57bfedbb95c08b572e2462536637135f7f3bfb2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984970"
---
# <span data-ttu-id="3ed48-101">New-AzDigitalTwinsCheckNameRequestObject</span><span class="sxs-lookup"><span data-stu-id="3ed48-101">New-AzDigitalTwinsCheckNameRequestObject</span></span>

## <span data-ttu-id="3ed48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed48-103">CheckNameRequest에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3ed48-103">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="3ed48-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ed48-104">SYNTAX</span></span>

```
New-AzDigitalTwinsCheckNameRequestObject -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="3ed48-105">설명</span><span class="sxs-lookup"><span data-stu-id="3ed48-105">DESCRIPTION</span></span>
<span data-ttu-id="3ed48-106">CheckNameRequest에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3ed48-106">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="3ed48-107">예제</span><span class="sxs-lookup"><span data-stu-id="3ed48-107">EXAMPLES</span></span>

### <span data-ttu-id="3ed48-108">예제 1: 이름에 따라 DigitalTwinsCheckNameRequestObject 만들기</span><span class="sxs-lookup"><span data-stu-id="3ed48-108">Example 1: Create a DigitalTwinsCheckNameRequestObject by name</span></span>
```powershell
PS C:\> New-AzDigitalTwinsCheckNameRequestObject -name youriTestName

Name          Type
----          ----
youriTestName Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="3ed48-109">이름에 따라 DigitalTwinsCheckNameRequestObject 만들기</span><span class="sxs-lookup"><span data-stu-id="3ed48-109">Create a DigitalTwinsCheckNameRequestObject by name</span></span>

## <span data-ttu-id="3ed48-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ed48-110">PARAMETERS</span></span>

### <span data-ttu-id="3ed48-111">-Name</span><span class="sxs-lookup"><span data-stu-id="3ed48-111">-Name</span></span>
<span data-ttu-id="3ed48-112">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ed48-112">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed48-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed48-113">CommonParameters</span></span>
<span data-ttu-id="3ed48-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed48-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed48-115">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ed48-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed48-116">입력</span><span class="sxs-lookup"><span data-stu-id="3ed48-116">INPUTS</span></span>

## <span data-ttu-id="3ed48-117">출력</span><span class="sxs-lookup"><span data-stu-id="3ed48-117">OUTPUTS</span></span>

### <span data-ttu-id="3ed48-118">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.CheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="3ed48-118">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.CheckNameRequest</span></span>

## <span data-ttu-id="3ed48-119">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ed48-119">NOTES</span></span>

<span data-ttu-id="3ed48-120">별칭</span><span class="sxs-lookup"><span data-stu-id="3ed48-120">ALIASES</span></span>

## <span data-ttu-id="3ed48-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ed48-121">RELATED LINKS</span></span>

