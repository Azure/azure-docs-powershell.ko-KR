---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525047"
---
# <span data-ttu-id="31e68-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="31e68-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="31e68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e68-102">SYNOPSIS</span></span>
<span data-ttu-id="31e68-103">PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31e68-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="31e68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31e68-105">DESCRIPTION</span></span>
<span data-ttu-id="31e68-106">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="31e68-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31e68-107">EXAMPLES</span></span>

### <span data-ttu-id="31e68-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="31e68-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="31e68-109">이 명령은 resourcegroup testcapacity에서 testcapacity 이라는 활성 용량을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="31e68-110">변수</span><span class="sxs-lookup"><span data-stu-id="31e68-110">PARAMETERS</span></span>

### <span data-ttu-id="31e68-111">-이름</span><span class="sxs-lookup"><span data-stu-id="31e68-111">-Name</span></span>
<span data-ttu-id="31e68-112">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e68-113">-ResourceGroupName</span></span>
<span data-ttu-id="31e68-114">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31e68-115">-ResourceId</span></span>
<span data-ttu-id="31e68-116">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="31e68-116">Azure resource ID</span></span>

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

### <span data-ttu-id="31e68-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31e68-117">-InputObject</span></span>
<span data-ttu-id="31e68-118">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="31e68-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-119">-확인</span><span class="sxs-lookup"><span data-stu-id="31e68-119">-Confirm</span></span>
<span data-ttu-id="31e68-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="31e68-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e68-121">-WhatIf</span></span>
<span data-ttu-id="31e68-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e68-123">CommonParameters</span></span>
<span data-ttu-id="31e68-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e68-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e68-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e68-126">입력</span><span class="sxs-lookup"><span data-stu-id="31e68-126">INPUTS</span></span>

### <span data-ttu-id="31e68-127">않아야</span><span class="sxs-lookup"><span data-stu-id="31e68-127">None</span></span>
<span data-ttu-id="31e68-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31e68-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31e68-129">출력</span><span class="sxs-lookup"><span data-stu-id="31e68-129">OUTPUTS</span></span>

### <span data-ttu-id="31e68-130">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="31e68-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="31e68-131">상속자</span><span class="sxs-lookup"><span data-stu-id="31e68-131">NOTES</span></span>

## <span data-ttu-id="31e68-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31e68-132">RELATED LINKS</span></span>

[<span data-ttu-id="31e68-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="31e68-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="31e68-134">이력서-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="31e68-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

