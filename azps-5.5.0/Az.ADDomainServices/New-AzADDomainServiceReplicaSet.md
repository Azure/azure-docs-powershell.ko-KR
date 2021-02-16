---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176593"
---
# <span data-ttu-id="0a72b-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="0a72b-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="0a72b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a72b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a72b-103">ReplicaSet에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0a72b-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="0a72b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a72b-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a72b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0a72b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a72b-106">ReplicaSet에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0a72b-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="0a72b-107">예제</span><span class="sxs-lookup"><span data-stu-id="0a72b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a72b-108">예제 1: AdDomain용 ReplicaSet 만들기</span><span class="sxs-lookup"><span data-stu-id="0a72b-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="0a72b-109">AdDomain용 ReplicaSet 만들기</span><span class="sxs-lookup"><span data-stu-id="0a72b-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="0a72b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a72b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a72b-111">-Location</span><span class="sxs-lookup"><span data-stu-id="0a72b-111">-Location</span></span>
<span data-ttu-id="0a72b-112">가상 네트워크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0a72b-112">Virtual network location.</span></span>

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

### <span data-ttu-id="0a72b-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0a72b-113">-SubnetId</span></span>
<span data-ttu-id="0a72b-114">Domain Services를 배포할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a72b-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="0a72b-115">Domain Services가 배포될 서브넷의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a72b-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="0a72b-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="0a72b-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="0a72b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a72b-117">CommonParameters</span></span>
<span data-ttu-id="0a72b-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a72b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a72b-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a72b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a72b-120">입력</span><span class="sxs-lookup"><span data-stu-id="0a72b-120">INPUTS</span></span>

## <span data-ttu-id="0a72b-121">출력</span><span class="sxs-lookup"><span data-stu-id="0a72b-121">OUTPUTS</span></span>

### <span data-ttu-id="0a72b-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="0a72b-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="0a72b-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a72b-123">NOTES</span></span>

<span data-ttu-id="0a72b-124">별칭</span><span class="sxs-lookup"><span data-stu-id="0a72b-124">ALIASES</span></span>

## <span data-ttu-id="0a72b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a72b-125">RELATED LINKS</span></span>

