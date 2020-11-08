---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204551"
---
# <span data-ttu-id="9bd5d-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="9bd5d-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="9bd5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd5d-103">재고에 사용 가능한 네트워크 가상 어플라이언스 Sku를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="9bd5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9bd5d-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bd5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9bd5d-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd5d-106">Get-AzNetworkVirtualApplianceSku Microsoft Azure 인벤토리에서 사용할 수 있는 네트워크 가상 어플라이언스 Sku를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="9bd5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9bd5d-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd5d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9bd5d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="9bd5d-109">이름별로 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-109">Get a sku by name.</span></span>

### <span data-ttu-id="9bd5d-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="9bd5d-110">Example 2</span></span>
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

<span data-ttu-id="9bd5d-111">모든 사용 가능한 네트워크 가상 어플라이언스 Sku를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="9bd5d-112">변수</span><span class="sxs-lookup"><span data-stu-id="9bd5d-112">PARAMETERS</span></span>

### <span data-ttu-id="9bd5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd5d-113">-DefaultProfile</span></span>
<span data-ttu-id="9bd5d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd5d-115">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="9bd5d-115">-SkuName</span></span>
<span data-ttu-id="9bd5d-116">Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-116">The Sku name.</span></span>

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

### <span data-ttu-id="9bd5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd5d-117">CommonParameters</span></span>
<span data-ttu-id="9bd5d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd5d-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd5d-120">입력</span><span class="sxs-lookup"><span data-stu-id="9bd5d-120">INPUTS</span></span>

### <span data-ttu-id="9bd5d-121">않아야</span><span class="sxs-lookup"><span data-stu-id="9bd5d-121">None</span></span>

## <span data-ttu-id="9bd5d-122">출력</span><span class="sxs-lookup"><span data-stu-id="9bd5d-122">OUTPUTS</span></span>

### <span data-ttu-id="9bd5d-123">PSNetworkVirtualApplianceSku에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9bd5d-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="9bd5d-124">상속자</span><span class="sxs-lookup"><span data-stu-id="9bd5d-124">NOTES</span></span>

## <span data-ttu-id="9bd5d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bd5d-125">RELATED LINKS</span></span>
