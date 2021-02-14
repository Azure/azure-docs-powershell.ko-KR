---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195124"
---
# <span data-ttu-id="52323-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="52323-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="52323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52323-102">SYNOPSIS</span></span>
<span data-ttu-id="52323-103">LoadBalancerFrontendIPConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="52323-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="52323-104">구문</span><span class="sxs-lookup"><span data-stu-id="52323-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="52323-105">설명</span><span class="sxs-lookup"><span data-stu-id="52323-105">DESCRIPTION</span></span>
<span data-ttu-id="52323-106">LoadBalancerFrontendIPConfiguration에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="52323-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="52323-107">예제</span><span class="sxs-lookup"><span data-stu-id="52323-107">EXAMPLES</span></span>

### <span data-ttu-id="52323-108">예제 1: 부하 균형 조정기 프런트 엔드 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="52323-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="52323-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 부하 균형 조정기 프런트 엔드 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="52323-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="52323-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="52323-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="52323-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52323-111">PARAMETERS</span></span>

### <span data-ttu-id="52323-112">-Name</span><span class="sxs-lookup"><span data-stu-id="52323-112">-Name</span></span>
<span data-ttu-id="52323-113">FrontendIpConfigration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52323-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="52323-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="52323-114">-PublicIPAddressId</span></span>
<span data-ttu-id="52323-115">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="52323-115">Resource Id.</span></span>

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

### <span data-ttu-id="52323-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52323-116">CommonParameters</span></span>
<span data-ttu-id="52323-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52323-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52323-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52323-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52323-119">입력</span><span class="sxs-lookup"><span data-stu-id="52323-119">INPUTS</span></span>

## <span data-ttu-id="52323-120">출력</span><span class="sxs-lookup"><span data-stu-id="52323-120">OUTPUTS</span></span>

### <span data-ttu-id="52323-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="52323-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="52323-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52323-122">NOTES</span></span>

<span data-ttu-id="52323-123">별칭</span><span class="sxs-lookup"><span data-stu-id="52323-123">ALIASES</span></span>

## <span data-ttu-id="52323-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52323-124">RELATED LINKS</span></span>

