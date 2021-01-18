---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495559"
---
# <span data-ttu-id="fb8d8-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fb8d8-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="fb8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8d8-103">네트워크 가상 어플라이언스 리소스에 연결된 사이트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="fb8d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb8d8-104">SYNTAX</span></span>

### <span data-ttu-id="fb8d8-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb8d8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb8d8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb8d8-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb8d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="fb8d8-108">이 Get-AzVirtualApplianceSite 하나 이상의 네트워크 가상 어플라이언스 리소스에 연결된 사이트를 되거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="fb8d8-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="fb8d8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb8d8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="fb8d8-111">가상 어플라이언스 사이트 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="fb8d8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fb8d8-112">Example 2</span></span>
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

<span data-ttu-id="fb8d8-113">네트워크 가상 어플라이언스에 가상 어플라이언스 사이트 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="fb8d8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb8d8-114">PARAMETERS</span></span>

### <span data-ttu-id="fb8d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8d8-115">-DefaultProfile</span></span>
<span data-ttu-id="fb8d8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb8d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb8d8-117">-Name</span></span>
<span data-ttu-id="fb8d8-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-118">The resource name.</span></span>

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

### <span data-ttu-id="fb8d8-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="fb8d8-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="fb8d8-120">사이트가 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="fb8d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb8d8-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-122">The resource group name.</span></span>

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

### <span data-ttu-id="fb8d8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb8d8-123">-ResourceId</span></span>
<span data-ttu-id="fb8d8-124">가상 어플라이언스 사이트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="fb8d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8d8-125">CommonParameters</span></span>
<span data-ttu-id="fb8d8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8d8-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb8d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8d8-128">입력</span><span class="sxs-lookup"><span data-stu-id="fb8d8-128">INPUTS</span></span>

### <span data-ttu-id="fb8d8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb8d8-129">System.String</span></span>

## <span data-ttu-id="fb8d8-130">출력</span><span class="sxs-lookup"><span data-stu-id="fb8d8-130">OUTPUTS</span></span>

### <span data-ttu-id="fb8d8-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fb8d8-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="fb8d8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb8d8-132">NOTES</span></span>

## <span data-ttu-id="fb8d8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb8d8-133">RELATED LINKS</span></span>
