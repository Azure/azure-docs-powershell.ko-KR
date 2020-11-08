---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034088"
---
# <span data-ttu-id="c13ca-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c13ca-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c13ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c13ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c13ca-103">새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="c13ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c13ca-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c13ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c13ca-105">DESCRIPTION</span></span>
<span data-ttu-id="c13ca-106">New-AzPowerBIEmbeddedCapacity cmdlet은 새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c13ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c13ca-107">EXAMPLES</span></span>

### <span data-ttu-id="c13ca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c13ca-108">Example 1</span></span>
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

<span data-ttu-id="c13ca-109">Azure 지역 서쪽 중부 US 및 리소스 그룹 testRG에서 testcapacity 라는 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="c13ca-110">용량에 대 한 sku 수준은 A1입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="c13ca-111">변수</span><span class="sxs-lookup"><span data-stu-id="c13ca-111">PARAMETERS</span></span>

### <span data-ttu-id="c13ca-112">-관리자</span><span class="sxs-lookup"><span data-stu-id="c13ca-112">-Administrator</span></span>
<span data-ttu-id="c13ca-113">용량에 관리자로 설정할 쉼표로 구분 된 이름</span><span class="sxs-lookup"><span data-stu-id="c13ca-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="c13ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13ca-114">-DefaultProfile</span></span>
<span data-ttu-id="c13ca-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c13ca-116">-위치</span><span class="sxs-lookup"><span data-stu-id="c13ca-116">-Location</span></span>
<span data-ttu-id="c13ca-117">PowerBI 포함 용량이 호스팅되는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="c13ca-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c13ca-118">-Name</span></span>
<span data-ttu-id="c13ca-119">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="c13ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c13ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="c13ca-121">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="c13ca-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="c13ca-122">-Sku</span></span>
<span data-ttu-id="c13ca-123">용량에 대 한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="c13ca-124">태그</span><span class="sxs-lookup"><span data-stu-id="c13ca-124">-Tag</span></span>
<span data-ttu-id="c13ca-125">용량에 대 한 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="c13ca-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c13ca-126">-Confirm</span></span>
<span data-ttu-id="c13ca-127">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="c13ca-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c13ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c13ca-128">-WhatIf</span></span>
<span data-ttu-id="c13ca-129">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c13ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13ca-130">CommonParameters</span></span>
<span data-ttu-id="c13ca-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13ca-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c13ca-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13ca-133">입력</span><span class="sxs-lookup"><span data-stu-id="c13ca-133">INPUTS</span></span>

### <span data-ttu-id="c13ca-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c13ca-134">System.String</span></span>

### <span data-ttu-id="c13ca-135">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="c13ca-135">System.String[]</span></span>

### <span data-ttu-id="c13ca-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c13ca-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c13ca-137">출력</span><span class="sxs-lookup"><span data-stu-id="c13ca-137">OUTPUTS</span></span>

### <span data-ttu-id="c13ca-138">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="c13ca-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c13ca-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c13ca-139">NOTES</span></span>

## <span data-ttu-id="c13ca-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c13ca-140">RELATED LINKS</span></span>

[<span data-ttu-id="c13ca-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c13ca-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c13ca-142">제거-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c13ca-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
