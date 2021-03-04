---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953472"
---
# <span data-ttu-id="bb198-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bb198-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bb198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb198-102">SYNOPSIS</span></span>
<span data-ttu-id="bb198-103">PowerBI Embedded 용량의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bb198-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb198-104">SYNTAX</span></span>

### <span data-ttu-id="bb198-105">ByCapacityOrResourceGroupOrSubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb198-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb198-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb198-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb198-107">설명</span><span class="sxs-lookup"><span data-stu-id="bb198-107">DESCRIPTION</span></span>
<span data-ttu-id="bb198-108">Get-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI Embedded 용량의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bb198-109">예제</span><span class="sxs-lookup"><span data-stu-id="bb198-109">EXAMPLES</span></span>

### <span data-ttu-id="bb198-110">예제 1: 리소스 그룹 용량 얻기</span><span class="sxs-lookup"><span data-stu-id="bb198-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="bb198-111">이 명령은 testRG라는 리소스 그룹의 모든 Azure PowerBI Embedded Capacity를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="bb198-112">예제 2: 용량을 얻다</span><span class="sxs-lookup"><span data-stu-id="bb198-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="bb198-113">이 명령은 testRG라는 리소스 그룹에서 testcapacity라는 Azure PowerBI Embedded Capacity를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="bb198-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bb198-114">PARAMETERS</span></span>

### <span data-ttu-id="bb198-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb198-115">-DefaultProfile</span></span>
<span data-ttu-id="bb198-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb198-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bb198-117">-Name</span></span>
<span data-ttu-id="bb198-118">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="bb198-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb198-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb198-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb198-120">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="bb198-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb198-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb198-121">-ResourceId</span></span>
<span data-ttu-id="bb198-122">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bb198-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb198-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb198-123">CommonParameters</span></span>
<span data-ttu-id="bb198-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb198-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb198-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bb198-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb198-126">입력</span><span class="sxs-lookup"><span data-stu-id="bb198-126">INPUTS</span></span>

### <span data-ttu-id="bb198-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bb198-127">System.String</span></span>

## <span data-ttu-id="bb198-128">출력</span><span class="sxs-lookup"><span data-stu-id="bb198-128">OUTPUTS</span></span>

### <span data-ttu-id="bb198-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bb198-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bb198-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb198-130">NOTES</span></span>

## <span data-ttu-id="bb198-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb198-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb198-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="bb198-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bb198-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="bb198-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
