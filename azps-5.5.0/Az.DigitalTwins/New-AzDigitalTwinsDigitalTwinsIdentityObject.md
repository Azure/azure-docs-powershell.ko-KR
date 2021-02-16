---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209645"
---
# <span data-ttu-id="e442d-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="e442d-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="e442d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e442d-102">SYNOPSIS</span></span>
<span data-ttu-id="e442d-103">DigitalTwinsIdentity에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e442d-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="e442d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e442d-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e442d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e442d-105">DESCRIPTION</span></span>
<span data-ttu-id="e442d-106">DigitalTwinsIdentity에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e442d-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="e442d-107">예제</span><span class="sxs-lookup"><span data-stu-id="e442d-107">EXAMPLES</span></span>

### <span data-ttu-id="e442d-108">예제 1: DigitalTwinsIdentityObject 만들기</span><span class="sxs-lookup"><span data-stu-id="e442d-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="e442d-109">ID 및 위치로 DigitalTwinsIdentityObject 만들기</span><span class="sxs-lookup"><span data-stu-id="e442d-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="e442d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e442d-110">PARAMETERS</span></span>

### <span data-ttu-id="e442d-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e442d-111">-EndpointName</span></span>
<span data-ttu-id="e442d-112">엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="e442d-113">-Id</span><span class="sxs-lookup"><span data-stu-id="e442d-113">-Id</span></span>
<span data-ttu-id="e442d-114">리소스 ID 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-114">Resource identity path.</span></span>

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

### <span data-ttu-id="e442d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e442d-115">-Location</span></span>
<span data-ttu-id="e442d-116">DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e442d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e442d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e442d-118">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e442d-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e442d-119">-ResourceName</span></span>
<span data-ttu-id="e442d-120">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e442d-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e442d-121">-SubscriptionId</span></span>
<span data-ttu-id="e442d-122">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="e442d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e442d-123">CommonParameters</span></span>
<span data-ttu-id="e442d-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e442d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e442d-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e442d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e442d-126">입력</span><span class="sxs-lookup"><span data-stu-id="e442d-126">INPUTS</span></span>

## <span data-ttu-id="e442d-127">출력</span><span class="sxs-lookup"><span data-stu-id="e442d-127">OUTPUTS</span></span>

### <span data-ttu-id="e442d-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e442d-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="e442d-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e442d-129">NOTES</span></span>

<span data-ttu-id="e442d-130">별칭</span><span class="sxs-lookup"><span data-stu-id="e442d-130">ALIASES</span></span>

## <span data-ttu-id="e442d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e442d-131">RELATED LINKS</span></span>

