---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 86531beb13ef70f8c35de7f4921277b0f9fa0bf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953456"
---
# <span data-ttu-id="f0ca4-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0ca4-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f0ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ca4-103">새 PowerBI Embedded 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f0ca4-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0ca4-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ca4-105">설명</span><span class="sxs-lookup"><span data-stu-id="f0ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ca4-106">New-AzPowerBIEmbeddedCapacity cmdlet에서 새 PowerBI Embedded 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f0ca4-107">예제</span><span class="sxs-lookup"><span data-stu-id="f0ca4-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ca4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0ca4-108">Example 1</span></span>
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

<span data-ttu-id="f0ca4-109">미국 중서부 Azure 지역과 리소스 그룹 testRG에서 testcapacity라는 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="f0ca4-110">용량의 sku 수준은 A1입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="f0ca4-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f0ca4-111">PARAMETERS</span></span>

### <span data-ttu-id="f0ca4-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="f0ca4-112">-Administrator</span></span>
<span data-ttu-id="f0ca4-113">용량에서 관리자로 설정할 콤마로 구분된 이름</span><span class="sxs-lookup"><span data-stu-id="f0ca4-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="f0ca4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ca4-114">-DefaultProfile</span></span>
<span data-ttu-id="f0ca4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ca4-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f0ca4-116">-Location</span></span>
<span data-ttu-id="f0ca4-117">PowerBI Embedded Capacity가 호스트되는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="f0ca4-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="f0ca4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f0ca4-118">-Name</span></span>
<span data-ttu-id="f0ca4-119">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="f0ca4-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f0ca4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ca4-120">-ResourceGroupName</span></span>
<span data-ttu-id="f0ca4-121">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f0ca4-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="f0ca4-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="f0ca4-122">-Sku</span></span>
<span data-ttu-id="f0ca4-123">용량에 대한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="f0ca4-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0ca4-124">-Tag</span></span>
<span data-ttu-id="f0ca4-125">용량에 대한 태그로 설정된 해시 테이블 집합의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="f0ca4-126">-확인</span><span class="sxs-lookup"><span data-stu-id="f0ca4-126">-Confirm</span></span>
<span data-ttu-id="f0ca4-127">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f0ca4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ca4-128">-WhatIf</span></span>
<span data-ttu-id="f0ca4-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f0ca4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ca4-130">CommonParameters</span></span>
<span data-ttu-id="f0ca4-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ca4-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0ca4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ca4-133">입력</span><span class="sxs-lookup"><span data-stu-id="f0ca4-133">INPUTS</span></span>

### <span data-ttu-id="f0ca4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f0ca4-134">System.String</span></span>

### <span data-ttu-id="f0ca4-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f0ca4-135">System.String[]</span></span>

### <span data-ttu-id="f0ca4-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0ca4-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0ca4-137">출력</span><span class="sxs-lookup"><span data-stu-id="f0ca4-137">OUTPUTS</span></span>

### <span data-ttu-id="f0ca4-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0ca4-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f0ca4-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0ca4-139">NOTES</span></span>

## <span data-ttu-id="f0ca4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0ca4-140">RELATED LINKS</span></span>

[<span data-ttu-id="f0ca4-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0ca4-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f0ca4-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0ca4-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
