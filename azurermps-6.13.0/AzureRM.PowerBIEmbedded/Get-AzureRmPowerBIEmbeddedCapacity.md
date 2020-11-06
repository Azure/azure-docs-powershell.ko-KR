---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528457"
---
# <span data-ttu-id="27529-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27529-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="27529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27529-102">SYNOPSIS</span></span>
<span data-ttu-id="27529-103">PowerBI 포함 용량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27529-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27529-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27529-104">SYNTAX</span></span>

### <span data-ttu-id="27529-105">ByCapacityOrResourceGroupOrSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="27529-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27529-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27529-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27529-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27529-107">DESCRIPTION</span></span>
<span data-ttu-id="27529-108">Get-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27529-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="27529-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27529-109">EXAMPLES</span></span>

### <span data-ttu-id="27529-110">예제 1: 리소스 그룹 용량 가져오기</span><span class="sxs-lookup"><span data-stu-id="27529-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="27529-111">이 명령은 testRG 이라는 리소스 그룹에 있는 모든 Azure PowerBI 포함 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27529-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="27529-112">예제 2: 용량 구하기</span><span class="sxs-lookup"><span data-stu-id="27529-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="27529-113">이 명령은 testRG 이라는 리소스 그룹에서 testcapacity 라는 Azure PowerBI 포함 된 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27529-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="27529-114">변수</span><span class="sxs-lookup"><span data-stu-id="27529-114">PARAMETERS</span></span>

### <span data-ttu-id="27529-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27529-115">-DefaultProfile</span></span>
<span data-ttu-id="27529-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27529-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27529-117">-이름</span><span class="sxs-lookup"><span data-stu-id="27529-117">-Name</span></span>
<span data-ttu-id="27529-118">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27529-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="27529-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27529-119">-ResourceGroupName</span></span>
<span data-ttu-id="27529-120">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27529-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="27529-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27529-121">-ResourceId</span></span>
<span data-ttu-id="27529-122">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="27529-122">Azure resource ID</span></span>

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

### <span data-ttu-id="27529-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27529-123">CommonParameters</span></span>
<span data-ttu-id="27529-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27529-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27529-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27529-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27529-126">입력</span><span class="sxs-lookup"><span data-stu-id="27529-126">INPUTS</span></span>

### <span data-ttu-id="27529-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27529-127">System.String</span></span>

## <span data-ttu-id="27529-128">출력</span><span class="sxs-lookup"><span data-stu-id="27529-128">OUTPUTS</span></span>

### <span data-ttu-id="27529-129">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="27529-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="27529-130">상속자</span><span class="sxs-lookup"><span data-stu-id="27529-130">NOTES</span></span>

## <span data-ttu-id="27529-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27529-131">RELATED LINKS</span></span>

[<span data-ttu-id="27529-132">새로운 AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="27529-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="27529-133">제거-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="27529-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
