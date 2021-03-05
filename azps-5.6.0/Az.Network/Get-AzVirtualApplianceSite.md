---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016208"
---
# <span data-ttu-id="786ad-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="786ad-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="786ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786ad-102">SYNOPSIS</span></span>
<span data-ttu-id="786ad-103">네트워크 가상 어플라이언스 리소스에 연결된 사이트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="786ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="786ad-104">SYNTAX</span></span>

### <span data-ttu-id="786ad-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="786ad-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="786ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="786ad-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="786ad-107">설명</span><span class="sxs-lookup"><span data-stu-id="786ad-107">DESCRIPTION</span></span>
<span data-ttu-id="786ad-108">이 Get-AzVirtualApplianceSite 네트워크 가상 어플라이언스 리소스에 연결된 사이트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="786ad-109">예제</span><span class="sxs-lookup"><span data-stu-id="786ad-109">EXAMPLES</span></span>

### <span data-ttu-id="786ad-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="786ad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="786ad-111">Virtual Appliance 사이트 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="786ad-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="786ad-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="786ad-113">네트워크 가상 어플라이언스에 Virtual Appliance 사이트 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="786ad-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="786ad-114">PARAMETERS</span></span>

### <span data-ttu-id="786ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786ad-115">-DefaultProfile</span></span>
<span data-ttu-id="786ad-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="786ad-117">-Name</span></span>
<span data-ttu-id="786ad-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-118">The resource name.</span></span>

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

### <span data-ttu-id="786ad-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="786ad-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="786ad-120">사이트가 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="786ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="786ad-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-122">The resource group name.</span></span>

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

### <span data-ttu-id="786ad-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="786ad-123">-ResourceId</span></span>
<span data-ttu-id="786ad-124">가상 어플라이언스 사이트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="786ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786ad-125">CommonParameters</span></span>
<span data-ttu-id="786ad-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="786ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786ad-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="786ad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786ad-128">입력</span><span class="sxs-lookup"><span data-stu-id="786ad-128">INPUTS</span></span>

### <span data-ttu-id="786ad-129">System.String</span><span class="sxs-lookup"><span data-stu-id="786ad-129">System.String</span></span>

## <span data-ttu-id="786ad-130">출력</span><span class="sxs-lookup"><span data-stu-id="786ad-130">OUTPUTS</span></span>

### <span data-ttu-id="786ad-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="786ad-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="786ad-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="786ad-132">NOTES</span></span>

## <span data-ttu-id="786ad-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="786ad-133">RELATED LINKS</span></span>
