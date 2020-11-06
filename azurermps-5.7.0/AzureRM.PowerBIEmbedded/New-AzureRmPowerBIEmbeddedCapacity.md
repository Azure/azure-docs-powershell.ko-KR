---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527956"
---
# <span data-ttu-id="da475-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="da475-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="da475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da475-102">SYNOPSIS</span></span>
<span data-ttu-id="da475-103">새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da475-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da475-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da475-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="da475-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da475-105">DESCRIPTION</span></span>
<span data-ttu-id="da475-106">New-AzureRmPowerBIEmbeddedCapacity cmdlet은 새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da475-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="da475-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da475-107">EXAMPLES</span></span>

### <span data-ttu-id="da475-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="da475-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="da475-109">Azure 지역 서쪽 중부 US 및 리소스 그룹 testRG에서 testcapacity 라는 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da475-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="da475-110">용량에 대 한 sku 수준은 A1입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="da475-111">변수</span><span class="sxs-lookup"><span data-stu-id="da475-111">PARAMETERS</span></span>

### <span data-ttu-id="da475-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da475-112">-ResourceGroupName</span></span>
<span data-ttu-id="da475-113">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-114">-이름</span><span class="sxs-lookup"><span data-stu-id="da475-114">-Name</span></span>
<span data-ttu-id="da475-115">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-116">-위치</span><span class="sxs-lookup"><span data-stu-id="da475-116">-Location</span></span>
<span data-ttu-id="da475-117">PowerBI 포함 용량이 호스팅되는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-118">-Sku</span><span class="sxs-lookup"><span data-stu-id="da475-118">-Sku</span></span>
<span data-ttu-id="da475-119">용량에 대 한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-120">-관리자</span><span class="sxs-lookup"><span data-stu-id="da475-120">-Administrator</span></span>
<span data-ttu-id="da475-121">용량에 관리자로 설정할 쉼표로 구분 된 용량 이름</span><span class="sxs-lookup"><span data-stu-id="da475-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-122">태그</span><span class="sxs-lookup"><span data-stu-id="da475-122">-Tag</span></span>
<span data-ttu-id="da475-123">용량에 대 한 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="da475-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="da475-124">-확인</span><span class="sxs-lookup"><span data-stu-id="da475-124">-Confirm</span></span>
<span data-ttu-id="da475-125">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="da475-125">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="da475-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da475-126">-WhatIf</span></span>
<span data-ttu-id="da475-127">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="da475-127">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="da475-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da475-128">CommonParameters</span></span>
<span data-ttu-id="da475-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da475-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da475-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da475-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da475-131">입력</span><span class="sxs-lookup"><span data-stu-id="da475-131">INPUTS</span></span>

### <span data-ttu-id="da475-132">않아야</span><span class="sxs-lookup"><span data-stu-id="da475-132">None</span></span>
<span data-ttu-id="da475-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da475-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da475-134">출력</span><span class="sxs-lookup"><span data-stu-id="da475-134">OUTPUTS</span></span>

### <span data-ttu-id="da475-135">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="da475-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="da475-136">상속자</span><span class="sxs-lookup"><span data-stu-id="da475-136">NOTES</span></span>

## <span data-ttu-id="da475-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da475-137">RELATED LINKS</span></span>

[<span data-ttu-id="da475-138">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="da475-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="da475-139">제거-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="da475-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
