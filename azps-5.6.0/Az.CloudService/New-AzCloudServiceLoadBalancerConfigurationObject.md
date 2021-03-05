---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986183"
---
# <span data-ttu-id="8a29f-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="8a29f-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="8a29f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a29f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a29f-103">LoadBalancerConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8a29f-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="8a29f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a29f-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a29f-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a29f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a29f-106">LoadBalancerConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8a29f-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="8a29f-107">예제</span><span class="sxs-lookup"><span data-stu-id="8a29f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a29f-108">예제 1: 부하 균형 조정기 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8a29f-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="8a29f-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 Load Balancer 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="8a29f-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="8a29f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a29f-111">PARAMETERS</span></span>

### <span data-ttu-id="8a29f-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a29f-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="8a29f-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8a29f-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="8a29f-114">생성을 위해 FRONTENDIPCONFIGURATION 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8a29f-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a29f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a29f-115">-Name</span></span>
<span data-ttu-id="8a29f-116">LoadBalancerConfiguration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="8a29f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a29f-117">CommonParameters</span></span>
<span data-ttu-id="8a29f-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a29f-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a29f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a29f-120">입력</span><span class="sxs-lookup"><span data-stu-id="8a29f-120">INPUTS</span></span>

## <span data-ttu-id="8a29f-121">출력</span><span class="sxs-lookup"><span data-stu-id="8a29f-121">OUTPUTS</span></span>

### <span data-ttu-id="8a29f-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a29f-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="8a29f-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a29f-123">NOTES</span></span>

<span data-ttu-id="8a29f-124">별칭</span><span class="sxs-lookup"><span data-stu-id="8a29f-124">ALIASES</span></span>

<span data-ttu-id="8a29f-125">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8a29f-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a29f-126">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a29f-127">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a29f-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a29f-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8a29f-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="8a29f-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8a29f-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="8a29f-130">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8a29f-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="8a29f-131">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8a29f-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="8a29f-132">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8a29f-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="8a29f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a29f-133">RELATED LINKS</span></span>

