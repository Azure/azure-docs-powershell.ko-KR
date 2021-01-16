---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379940"
---
# <span data-ttu-id="3d054-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3d054-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3d054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d054-102">SYNOPSIS</span></span>
<span data-ttu-id="3d054-103">네트워크 가상 어플라이언스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="3d054-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d054-104">SYNTAX</span></span>

### <span data-ttu-id="3d054-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d054-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d054-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d054-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d054-107">설명</span><span class="sxs-lookup"><span data-stu-id="3d054-107">DESCRIPTION</span></span>
<span data-ttu-id="3d054-108">이 Get-AzNetworkVirtualAppliance 네트워크 가상 어플라이언스 리소스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="3d054-109">예제</span><span class="sxs-lookup"><span data-stu-id="3d054-109">EXAMPLES</span></span>

### <span data-ttu-id="3d054-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d054-110">Example 1</span></span>
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

<span data-ttu-id="3d054-111">네트워크 가상 어플라이언스 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3d054-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d054-112">PARAMETERS</span></span>

### <span data-ttu-id="3d054-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d054-113">-DefaultProfile</span></span>
<span data-ttu-id="3d054-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d054-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d054-115">-Name</span></span>
<span data-ttu-id="3d054-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-116">The resource name.</span></span>

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

### <span data-ttu-id="3d054-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d054-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d054-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-118">The resource group name.</span></span>

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

### <span data-ttu-id="3d054-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d054-119">-ResourceId</span></span>
<span data-ttu-id="3d054-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-120">The resource Id.</span></span>

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

### <span data-ttu-id="3d054-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d054-121">CommonParameters</span></span>
<span data-ttu-id="3d054-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d054-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d054-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d054-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d054-124">입력</span><span class="sxs-lookup"><span data-stu-id="3d054-124">INPUTS</span></span>

### <span data-ttu-id="3d054-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3d054-125">System.String</span></span>

## <span data-ttu-id="3d054-126">출력</span><span class="sxs-lookup"><span data-stu-id="3d054-126">OUTPUTS</span></span>

### <span data-ttu-id="3d054-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3d054-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3d054-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d054-128">NOTES</span></span>

## <span data-ttu-id="3d054-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d054-129">RELATED LINKS</span></span>
