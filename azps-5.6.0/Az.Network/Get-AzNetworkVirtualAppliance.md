---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3ca8c522e3aa4d31e5718d09fffe0ff22fd4cab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006299"
---
# <span data-ttu-id="c4dd1-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="c4dd1-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="c4dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dd1-103">네트워크 가상 어플라이언스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="c4dd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4dd1-104">SYNTAX</span></span>

### <span data-ttu-id="c4dd1-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4dd1-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4dd1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4dd1-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4dd1-107">설명</span><span class="sxs-lookup"><span data-stu-id="c4dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="c4dd1-108">Get-AzNetworkVirtualAppliance 네트워크 가상 어플라이언스 리소스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="c4dd1-109">예제</span><span class="sxs-lookup"><span data-stu-id="c4dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="c4dd1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4dd1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="c4dd1-111">네트워크 가상 어플라이언스 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="c4dd1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c4dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="c4dd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dd1-113">-DefaultProfile</span></span>
<span data-ttu-id="c4dd1-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4dd1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c4dd1-115">-Name</span></span>
<span data-ttu-id="c4dd1-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dd1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4dd1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4dd1-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dd1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4dd1-119">-ResourceId</span></span>
<span data-ttu-id="c4dd1-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dd1-121">CommonParameters</span></span>
<span data-ttu-id="c4dd1-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dd1-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4dd1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dd1-124">입력</span><span class="sxs-lookup"><span data-stu-id="c4dd1-124">INPUTS</span></span>

### <span data-ttu-id="c4dd1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c4dd1-125">System.String</span></span>

## <span data-ttu-id="c4dd1-126">출력</span><span class="sxs-lookup"><span data-stu-id="c4dd1-126">OUTPUTS</span></span>

### <span data-ttu-id="c4dd1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="c4dd1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="c4dd1-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4dd1-128">NOTES</span></span>

## <span data-ttu-id="c4dd1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4dd1-129">RELATED LINKS</span></span>
