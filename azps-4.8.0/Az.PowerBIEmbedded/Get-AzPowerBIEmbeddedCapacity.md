---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212202"
---
# <span data-ttu-id="51b5e-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="51b5e-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="51b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="51b5e-103">PowerBI 포함 용량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="51b5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51b5e-104">SYNTAX</span></span>

### <span data-ttu-id="51b5e-105">ByCapacityOrResourceGroupOrSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="51b5e-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b5e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51b5e-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51b5e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51b5e-107">DESCRIPTION</span></span>
<span data-ttu-id="51b5e-108">Get-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="51b5e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51b5e-109">EXAMPLES</span></span>

### <span data-ttu-id="51b5e-110">예제 1: 리소스 그룹 용량 가져오기</span><span class="sxs-lookup"><span data-stu-id="51b5e-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="51b5e-111">이 명령은 testRG 이라는 리소스 그룹에 있는 모든 Azure PowerBI 포함 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="51b5e-112">예제 2: 용량 구하기</span><span class="sxs-lookup"><span data-stu-id="51b5e-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="51b5e-113">이 명령은 testRG 이라는 리소스 그룹에서 testcapacity 라는 Azure PowerBI 포함 된 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="51b5e-114">변수</span><span class="sxs-lookup"><span data-stu-id="51b5e-114">PARAMETERS</span></span>

### <span data-ttu-id="51b5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b5e-115">-DefaultProfile</span></span>
<span data-ttu-id="51b5e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b5e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="51b5e-117">-Name</span></span>
<span data-ttu-id="51b5e-118">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="51b5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="51b5e-120">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="51b5e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b5e-121">-ResourceId</span></span>
<span data-ttu-id="51b5e-122">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="51b5e-122">Azure resource ID</span></span>

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

### <span data-ttu-id="51b5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b5e-123">CommonParameters</span></span>
<span data-ttu-id="51b5e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b5e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b5e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b5e-126">입력</span><span class="sxs-lookup"><span data-stu-id="51b5e-126">INPUTS</span></span>

### <span data-ttu-id="51b5e-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51b5e-127">System.String</span></span>

## <span data-ttu-id="51b5e-128">출력</span><span class="sxs-lookup"><span data-stu-id="51b5e-128">OUTPUTS</span></span>

### <span data-ttu-id="51b5e-129">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="51b5e-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="51b5e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="51b5e-130">NOTES</span></span>

## <span data-ttu-id="51b5e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51b5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="51b5e-132">새로운 AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="51b5e-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="51b5e-133">제거-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="51b5e-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
