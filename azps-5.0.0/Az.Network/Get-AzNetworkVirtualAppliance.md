---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215984"
---
# <span data-ttu-id="56fbe-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="56fbe-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="56fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="56fbe-103">네트워크 가상 기기를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="56fbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56fbe-104">SYNTAX</span></span>

### <span data-ttu-id="56fbe-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="56fbe-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fbe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56fbe-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56fbe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="56fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="56fbe-108">Get-AzNetworkVirtualAppliance 명령에서는 네트워크 가상 어플라이언스 리소스를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="56fbe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="56fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="56fbe-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="56fbe-110">Example 1</span></span>
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

<span data-ttu-id="56fbe-111">네트워크 가상 기기 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="56fbe-112">변수</span><span class="sxs-lookup"><span data-stu-id="56fbe-112">PARAMETERS</span></span>

### <span data-ttu-id="56fbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fbe-113">-DefaultProfile</span></span>
<span data-ttu-id="56fbe-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fbe-115">-이름</span><span class="sxs-lookup"><span data-stu-id="56fbe-115">-Name</span></span>
<span data-ttu-id="56fbe-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-116">The resource name.</span></span>

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

### <span data-ttu-id="56fbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56fbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="56fbe-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-118">The resource group name.</span></span>

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

### <span data-ttu-id="56fbe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56fbe-119">-ResourceId</span></span>
<span data-ttu-id="56fbe-120">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-120">The resource Id.</span></span>

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

### <span data-ttu-id="56fbe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fbe-121">CommonParameters</span></span>
<span data-ttu-id="56fbe-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fbe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fbe-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56fbe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fbe-124">입력</span><span class="sxs-lookup"><span data-stu-id="56fbe-124">INPUTS</span></span>

### <span data-ttu-id="56fbe-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56fbe-125">System.String</span></span>

## <span data-ttu-id="56fbe-126">출력</span><span class="sxs-lookup"><span data-stu-id="56fbe-126">OUTPUTS</span></span>

### <span data-ttu-id="56fbe-127">Microsoft. 네트워크 모델. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="56fbe-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="56fbe-128">상속자</span><span class="sxs-lookup"><span data-stu-id="56fbe-128">NOTES</span></span>

## <span data-ttu-id="56fbe-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56fbe-129">RELATED LINKS</span></span>
