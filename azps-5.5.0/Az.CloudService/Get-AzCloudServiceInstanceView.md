---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200753"
---
# <span data-ttu-id="3af75-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="3af75-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="3af75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af75-102">SYNOPSIS</span></span>
<span data-ttu-id="3af75-103">클라우드 서비스의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="3af75-104">구문</span><span class="sxs-lookup"><span data-stu-id="3af75-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3af75-105">설명</span><span class="sxs-lookup"><span data-stu-id="3af75-105">DESCRIPTION</span></span>
<span data-ttu-id="3af75-106">클라우드 서비스의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="3af75-107">예제</span><span class="sxs-lookup"><span data-stu-id="3af75-107">EXAMPLES</span></span>

### <span data-ttu-id="3af75-108">예제 1: 클라우드 서비스 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="3af75-109">이 cmdlet은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="3af75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3af75-110">PARAMETERS</span></span>

### <span data-ttu-id="3af75-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="3af75-111">-CloudServiceName</span></span>
<span data-ttu-id="3af75-112">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="3af75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af75-113">-DefaultProfile</span></span>
<span data-ttu-id="3af75-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af75-115">-ResourceGroupName</span></span>
<span data-ttu-id="3af75-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="3af75-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3af75-117">-SubscriptionId</span></span>
<span data-ttu-id="3af75-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3af75-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af75-120">CommonParameters</span></span>
<span data-ttu-id="3af75-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3af75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af75-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3af75-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af75-123">입력</span><span class="sxs-lookup"><span data-stu-id="3af75-123">INPUTS</span></span>

## <span data-ttu-id="3af75-124">출력</span><span class="sxs-lookup"><span data-stu-id="3af75-124">OUTPUTS</span></span>

### <span data-ttu-id="3af75-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="3af75-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="3af75-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3af75-126">NOTES</span></span>

<span data-ttu-id="3af75-127">별칭</span><span class="sxs-lookup"><span data-stu-id="3af75-127">ALIASES</span></span>

## <span data-ttu-id="3af75-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3af75-128">RELATED LINKS</span></span>

