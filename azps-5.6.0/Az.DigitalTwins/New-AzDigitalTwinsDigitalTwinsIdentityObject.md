---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: 2b038699dfa1cd959ea20b761b6c24dee69a9e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984965"
---
# <span data-ttu-id="fb56c-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="fb56c-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="fb56c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb56c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb56c-103">DigitalTwinsIdentity에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fb56c-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="fb56c-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb56c-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb56c-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb56c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb56c-106">DigitalTwinsIdentity에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fb56c-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="fb56c-107">예제</span><span class="sxs-lookup"><span data-stu-id="fb56c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb56c-108">예제 1: DigitalTwinsIdentityObject 만들기</span><span class="sxs-lookup"><span data-stu-id="fb56c-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="fb56c-109">Id 및 위치로 DigitalTwinsIdentityObject 만들기</span><span class="sxs-lookup"><span data-stu-id="fb56c-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="fb56c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb56c-110">PARAMETERS</span></span>

### <span data-ttu-id="fb56c-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fb56c-111">-EndpointName</span></span>
<span data-ttu-id="fb56c-112">엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-112">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-113">-Id</span><span class="sxs-lookup"><span data-stu-id="fb56c-113">-Id</span></span>
<span data-ttu-id="fb56c-114">리소스 ID 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-114">Resource identity path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-115">-Location</span><span class="sxs-lookup"><span data-stu-id="fb56c-115">-Location</span></span>
<span data-ttu-id="fb56c-116">DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-116">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb56c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb56c-118">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fb56c-119">-ResourceName</span></span>
<span data-ttu-id="fb56c-120">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-120">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb56c-121">-SubscriptionId</span></span>
<span data-ttu-id="fb56c-122">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-122">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb56c-123">CommonParameters</span></span>
<span data-ttu-id="fb56c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb56c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb56c-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb56c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb56c-126">입력</span><span class="sxs-lookup"><span data-stu-id="fb56c-126">INPUTS</span></span>

## <span data-ttu-id="fb56c-127">출력</span><span class="sxs-lookup"><span data-stu-id="fb56c-127">OUTPUTS</span></span>

### <span data-ttu-id="fb56c-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="fb56c-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="fb56c-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb56c-129">NOTES</span></span>

<span data-ttu-id="fb56c-130">별칭</span><span class="sxs-lookup"><span data-stu-id="fb56c-130">ALIASES</span></span>

## <span data-ttu-id="fb56c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb56c-131">RELATED LINKS</span></span>

