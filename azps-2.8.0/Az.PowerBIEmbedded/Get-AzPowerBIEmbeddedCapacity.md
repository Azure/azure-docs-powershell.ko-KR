---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872289"
---
# <span data-ttu-id="d2e96-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2e96-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d2e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e96-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e96-103">PowerBI 포함 용량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d2e96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2e96-104">SYNTAX</span></span>

### <span data-ttu-id="d2e96-105">ByCapacityOrResourceGroupOrSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2e96-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e96-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e96-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2e96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2e96-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e96-108">Get-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d2e96-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2e96-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e96-110">예제 1: 리소스 그룹 용량 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2e96-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="d2e96-111">이 명령은 testRG 이라는 리소스 그룹에 있는 모든 Azure PowerBI 포함 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="d2e96-112">예제 2: 용량 구하기</span><span class="sxs-lookup"><span data-stu-id="d2e96-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="d2e96-113">이 명령은 testRG 이라는 리소스 그룹에서 testcapacity 라는 Azure PowerBI 포함 된 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="d2e96-114">변수</span><span class="sxs-lookup"><span data-stu-id="d2e96-114">PARAMETERS</span></span>

### <span data-ttu-id="d2e96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e96-115">-DefaultProfile</span></span>
<span data-ttu-id="d2e96-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e96-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d2e96-117">-Name</span></span>
<span data-ttu-id="d2e96-118">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d2e96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e96-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2e96-120">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="d2e96-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e96-121">-ResourceId</span></span>
<span data-ttu-id="d2e96-122">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d2e96-122">Azure resource ID</span></span>

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

### <span data-ttu-id="d2e96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e96-123">CommonParameters</span></span>
<span data-ttu-id="d2e96-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e96-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e96-126">입력</span><span class="sxs-lookup"><span data-stu-id="d2e96-126">INPUTS</span></span>

### <span data-ttu-id="d2e96-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2e96-127">System.String</span></span>

## <span data-ttu-id="d2e96-128">출력</span><span class="sxs-lookup"><span data-stu-id="d2e96-128">OUTPUTS</span></span>

### <span data-ttu-id="d2e96-129">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="d2e96-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d2e96-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d2e96-130">NOTES</span></span>

## <span data-ttu-id="d2e96-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e96-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2e96-132">새로운 AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d2e96-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d2e96-133">제거-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d2e96-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
