---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379919"
---
# <span data-ttu-id="c876d-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="c876d-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="c876d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c876d-102">SYNOPSIS</span></span>
<span data-ttu-id="c876d-103">인벤토리에서 사용 가능한 네트워크 가상 어플라이언스 SKU를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="c876d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c876d-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c876d-105">설명</span><span class="sxs-lookup"><span data-stu-id="c876d-105">DESCRIPTION</span></span>
<span data-ttu-id="c876d-106">이 Get-AzNetworkVirtualApplianceSku Microsoft Azure 인벤토리에서 사용 가능한 네트워크 가상 어플라이언스 SKU를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="c876d-107">예제</span><span class="sxs-lookup"><span data-stu-id="c876d-107">EXAMPLES</span></span>

### <span data-ttu-id="c876d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c876d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="c876d-109">이름으로 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-109">Get a sku by name.</span></span>

### <span data-ttu-id="c876d-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="c876d-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="c876d-111">네트워크 가상 어플라이언스의 사용 가능한 모든 SKU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="c876d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c876d-112">PARAMETERS</span></span>

### <span data-ttu-id="c876d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c876d-113">-DefaultProfile</span></span>
<span data-ttu-id="c876d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c876d-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c876d-115">-SkuName</span></span>
<span data-ttu-id="c876d-116">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-116">The Sku name.</span></span>

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

### <span data-ttu-id="c876d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c876d-117">CommonParameters</span></span>
<span data-ttu-id="c876d-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c876d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c876d-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c876d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c876d-120">입력</span><span class="sxs-lookup"><span data-stu-id="c876d-120">INPUTS</span></span>

### <span data-ttu-id="c876d-121">없음</span><span class="sxs-lookup"><span data-stu-id="c876d-121">None</span></span>

## <span data-ttu-id="c876d-122">출력</span><span class="sxs-lookup"><span data-stu-id="c876d-122">OUTPUTS</span></span>

### <span data-ttu-id="c876d-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="c876d-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="c876d-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c876d-124">NOTES</span></span>

## <span data-ttu-id="c876d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c876d-125">RELATED LINKS</span></span>
