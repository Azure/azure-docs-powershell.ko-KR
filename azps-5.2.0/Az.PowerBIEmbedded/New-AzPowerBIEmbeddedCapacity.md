---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355766"
---
# <span data-ttu-id="1b5a7-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1b5a7-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1b5a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5a7-103">새 PowerBI Embedded 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="1b5a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b5a7-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b5a7-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5a7-106">이 New-AzPowerBIEmbeddedCapacity 새 PowerBI Embedded Capacity를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1b5a7-107">예제</span><span class="sxs-lookup"><span data-stu-id="1b5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="1b5a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b5a7-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="1b5a7-109">미국 중서부 Azure 지역 및 리소스 그룹 testRG에서 testcapacity라는 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="1b5a7-110">용량에 대한 SKU 수준은 A1입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="1b5a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b5a7-111">PARAMETERS</span></span>

### <span data-ttu-id="1b5a7-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="1b5a7-112">-Administrator</span></span>
<span data-ttu-id="1b5a7-113">용량에 관리자로 설정할 콤마로 구분된 이름</span><span class="sxs-lookup"><span data-stu-id="1b5a7-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5a7-114">-DefaultProfile</span></span>
<span data-ttu-id="1b5a7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b5a7-116">-Location</span><span class="sxs-lookup"><span data-stu-id="1b5a7-116">-Location</span></span>
<span data-ttu-id="1b5a7-117">PowerBI Embedded Capacity가 호스트되는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="1b5a7-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1b5a7-118">-Name</span></span>
<span data-ttu-id="1b5a7-119">PowerBI 포함된 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="1b5a7-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b5a7-121">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1b5a7-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="1b5a7-122">-Sku</span></span>
<span data-ttu-id="1b5a7-123">용량에 대한 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b5a7-124">-Tag</span></span>
<span data-ttu-id="1b5a7-125">용량에 대한 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b5a7-126">-Confirm</span></span>
<span data-ttu-id="1b5a7-127">사용자에게 작업을 수행할지 여부를 확인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b5a7-128">-WhatIf</span></span>
<span data-ttu-id="1b5a7-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5a7-130">CommonParameters</span></span>
<span data-ttu-id="1b5a7-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5a7-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5a7-133">입력</span><span class="sxs-lookup"><span data-stu-id="1b5a7-133">INPUTS</span></span>

### <span data-ttu-id="1b5a7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1b5a7-134">System.String</span></span>

### <span data-ttu-id="1b5a7-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1b5a7-135">System.String[]</span></span>

### <span data-ttu-id="1b5a7-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b5a7-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b5a7-137">출력</span><span class="sxs-lookup"><span data-stu-id="1b5a7-137">OUTPUTS</span></span>

### <span data-ttu-id="1b5a7-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1b5a7-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1b5a7-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b5a7-139">NOTES</span></span>

## <span data-ttu-id="1b5a7-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b5a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="1b5a7-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1b5a7-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1b5a7-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1b5a7-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
