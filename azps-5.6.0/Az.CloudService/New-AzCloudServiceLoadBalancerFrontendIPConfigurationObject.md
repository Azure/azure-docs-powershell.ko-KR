---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: 5628b7819789ba97ee56a0c69f65e371f9b35e7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986174"
---
# <span data-ttu-id="93547-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="93547-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="93547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93547-102">SYNOPSIS</span></span>
<span data-ttu-id="93547-103">LoadBalancerFrontendIPConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="93547-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="93547-104">구문</span><span class="sxs-lookup"><span data-stu-id="93547-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="93547-105">설명</span><span class="sxs-lookup"><span data-stu-id="93547-105">DESCRIPTION</span></span>
<span data-ttu-id="93547-106">LoadBalancerFrontendIPConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="93547-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="93547-107">예제</span><span class="sxs-lookup"><span data-stu-id="93547-107">EXAMPLES</span></span>

### <span data-ttu-id="93547-108">예제 1: 부하 균형 조정기 프런트 엔드 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="93547-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="93547-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 부하 균형기 프런트 엔드 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93547-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="93547-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="93547-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="93547-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93547-111">PARAMETERS</span></span>

### <span data-ttu-id="93547-112">-Name</span><span class="sxs-lookup"><span data-stu-id="93547-112">-Name</span></span>
<span data-ttu-id="93547-113">FrontendIpConfigration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93547-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="93547-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="93547-114">-PublicIPAddressId</span></span>
<span data-ttu-id="93547-115">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="93547-115">Resource Id.</span></span>

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

### <span data-ttu-id="93547-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93547-116">CommonParameters</span></span>
<span data-ttu-id="93547-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93547-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93547-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93547-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93547-119">입력</span><span class="sxs-lookup"><span data-stu-id="93547-119">INPUTS</span></span>

## <span data-ttu-id="93547-120">출력</span><span class="sxs-lookup"><span data-stu-id="93547-120">OUTPUTS</span></span>

### <span data-ttu-id="93547-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="93547-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="93547-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93547-122">NOTES</span></span>

<span data-ttu-id="93547-123">별칭</span><span class="sxs-lookup"><span data-stu-id="93547-123">ALIASES</span></span>

## <span data-ttu-id="93547-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93547-124">RELATED LINKS</span></span>

