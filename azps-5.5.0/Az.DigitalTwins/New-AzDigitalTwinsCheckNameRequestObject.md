---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsCheckNameRequestObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
ms.openlocfilehash: 1e4f376099b0fc2c2bb5ef673438497bc9661153
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209664"
---
# <span data-ttu-id="58cd5-101">New-AzDigitalTwinsCheckNameRequestObject</span><span class="sxs-lookup"><span data-stu-id="58cd5-101">New-AzDigitalTwinsCheckNameRequestObject</span></span>

## <span data-ttu-id="58cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="58cd5-103">CheckNameRequest에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="58cd5-103">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="58cd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="58cd5-104">SYNTAX</span></span>

```
New-AzDigitalTwinsCheckNameRequestObject -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="58cd5-105">설명</span><span class="sxs-lookup"><span data-stu-id="58cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="58cd5-106">CheckNameRequest에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="58cd5-106">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="58cd5-107">예제</span><span class="sxs-lookup"><span data-stu-id="58cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="58cd5-108">예제 1: 이름으로 DigitalTwinsCheckNameRequestObject 만들기</span><span class="sxs-lookup"><span data-stu-id="58cd5-108">Example 1: Create a DigitalTwinsCheckNameRequestObject by name</span></span>
```powershell
PS C:\> New-AzDigitalTwinsCheckNameRequestObject -name youriTestName

Name          Type
----          ----
youriTestName Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="58cd5-109">이름으로 DigitalTwinsCheckNameRequestObject 만들기</span><span class="sxs-lookup"><span data-stu-id="58cd5-109">Create a DigitalTwinsCheckNameRequestObject by name</span></span>

## <span data-ttu-id="58cd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58cd5-110">PARAMETERS</span></span>

### <span data-ttu-id="58cd5-111">-Name</span><span class="sxs-lookup"><span data-stu-id="58cd5-111">-Name</span></span>
<span data-ttu-id="58cd5-112">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58cd5-112">Resource name.</span></span>

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

### <span data-ttu-id="58cd5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cd5-113">CommonParameters</span></span>
<span data-ttu-id="58cd5-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cd5-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58cd5-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cd5-116">입력</span><span class="sxs-lookup"><span data-stu-id="58cd5-116">INPUTS</span></span>

## <span data-ttu-id="58cd5-117">출력</span><span class="sxs-lookup"><span data-stu-id="58cd5-117">OUTPUTS</span></span>

### <span data-ttu-id="58cd5-118">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.CheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="58cd5-118">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.CheckNameRequest</span></span>

## <span data-ttu-id="58cd5-119">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58cd5-119">NOTES</span></span>

<span data-ttu-id="58cd5-120">별칭</span><span class="sxs-lookup"><span data-stu-id="58cd5-120">ALIASES</span></span>

## <span data-ttu-id="58cd5-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58cd5-121">RELATED LINKS</span></span>

