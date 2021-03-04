---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954160"
---
# <span data-ttu-id="da1e1-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="da1e1-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="da1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="da1e1-103">개인 링크 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-103">Gets private link service</span></span>

## <span data-ttu-id="da1e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="da1e1-104">SYNTAX</span></span>

### <span data-ttu-id="da1e1-105">NoExpand(기본값)</span><span class="sxs-lookup"><span data-stu-id="da1e1-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da1e1-106">확장</span><span class="sxs-lookup"><span data-stu-id="da1e1-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da1e1-107">설명</span><span class="sxs-lookup"><span data-stu-id="da1e1-107">DESCRIPTION</span></span>
<span data-ttu-id="da1e1-108">**Get-AzPrivateLinkService** cmdlet은 하나 이상의 개인 링크 서비스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="da1e1-109">예제</span><span class="sxs-lookup"><span data-stu-id="da1e1-109">EXAMPLES</span></span>

### <span data-ttu-id="da1e1-110">예제</span><span class="sxs-lookup"><span data-stu-id="da1e1-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="da1e1-111">이 명령줄은 리소스 그룹에서 개인 링크 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="da1e1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="da1e1-112">PARAMETERS</span></span>

### <span data-ttu-id="da1e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1e1-113">-DefaultProfile</span></span>
<span data-ttu-id="da1e1-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1e1-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="da1e1-115">-ExpandResource</span></span>
<span data-ttu-id="da1e1-116">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da1e1-117">-Name</span></span>
<span data-ttu-id="da1e1-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da1e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="da1e1-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1e1-121">CommonParameters</span></span>
<span data-ttu-id="da1e1-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da1e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1e1-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da1e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1e1-124">입력</span><span class="sxs-lookup"><span data-stu-id="da1e1-124">INPUTS</span></span>

### <span data-ttu-id="da1e1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="da1e1-125">System.String</span></span>

## <span data-ttu-id="da1e1-126">출력</span><span class="sxs-lookup"><span data-stu-id="da1e1-126">OUTPUTS</span></span>

### <span data-ttu-id="da1e1-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="da1e1-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="da1e1-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da1e1-128">NOTES</span></span>

## <span data-ttu-id="da1e1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da1e1-129">RELATED LINKS</span></span>
