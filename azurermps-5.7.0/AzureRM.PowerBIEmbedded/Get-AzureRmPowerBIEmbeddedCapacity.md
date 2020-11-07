---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702251"
---
# <span data-ttu-id="a5a85-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a85-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a5a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a85-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a85-103">PowerBI 포함 용량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5a85-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="a5a85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5a85-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a85-106">Get-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="a5a85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5a85-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a85-108">예제 1: 리소스 그룹 용량 가져오기</span><span class="sxs-lookup"><span data-stu-id="a5a85-108">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="a5a85-109">이 명령은 testRG 이라는 리소스 그룹에 있는 모든 Azure PowerBI 포함 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="a5a85-110">예제 2: 용량 구하기</span><span class="sxs-lookup"><span data-stu-id="a5a85-110">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="a5a85-111">이 명령은 testRG 이라는 리소스 그룹에서 testcapacity 라는 Azure PowerBI 포함 된 용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="a5a85-112">변수</span><span class="sxs-lookup"><span data-stu-id="a5a85-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a85-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a85-113">-ResourceGroupName</span></span>
<span data-ttu-id="a5a85-114">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a5a85-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a5a85-115">-Name</span></span>
<span data-ttu-id="a5a85-116">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a5a85-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a85-117">-ResourceId</span></span>
<span data-ttu-id="a5a85-118">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a5a85-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a85-119">CommonParameters</span></span>
<span data-ttu-id="a5a85-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a85-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a85-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a85-122">입력</span><span class="sxs-lookup"><span data-stu-id="a5a85-122">INPUTS</span></span>

### <span data-ttu-id="a5a85-123">않아야</span><span class="sxs-lookup"><span data-stu-id="a5a85-123">None</span></span>
<span data-ttu-id="a5a85-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5a85-125">출력</span><span class="sxs-lookup"><span data-stu-id="a5a85-125">OUTPUTS</span></span>

### <span data-ttu-id="a5a85-126">PSPowerBIEmbeddedCapacity><목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a85-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="a5a85-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a5a85-127">NOTES</span></span>

## <span data-ttu-id="a5a85-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5a85-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5a85-129">새로운 AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="a5a85-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a5a85-130">제거-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="a5a85-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
