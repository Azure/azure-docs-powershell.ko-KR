---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530139"
---
# <span data-ttu-id="0e6ac-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e6ac-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0e6ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6ac-103">새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e6ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e6ac-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e6ac-105">DESCRIPTION</span></span>
<span data-ttu-id="0e6ac-106">New-AzureRmPowerBIEmbeddedCapacity cmdlet은 새 PowerBI 포함 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="0e6ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e6ac-107">EXAMPLES</span></span>

### <span data-ttu-id="0e6ac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e6ac-108">Example 1</span></span>
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

<span data-ttu-id="0e6ac-109">Azure 지역 서쪽 중부 US 및 리소스 그룹 testRG에서 testcapacity 라는 용량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="0e6ac-110">용량에 대 한 sku 수준은 A1입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="0e6ac-111">변수</span><span class="sxs-lookup"><span data-stu-id="0e6ac-111">PARAMETERS</span></span>

### <span data-ttu-id="0e6ac-112">-관리자</span><span class="sxs-lookup"><span data-stu-id="0e6ac-112">-Administrator</span></span>
<span data-ttu-id="0e6ac-113">용량에 관리자로 설정할 쉼표로 구분 된 용량 이름</span><span class="sxs-lookup"><span data-stu-id="0e6ac-113">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="0e6ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6ac-114">-DefaultProfile</span></span>
<span data-ttu-id="0e6ac-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6ac-116">-위치</span><span class="sxs-lookup"><span data-stu-id="0e6ac-116">-Location</span></span>
<span data-ttu-id="0e6ac-117">PowerBI 포함 용량이 호스팅되는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="0e6ac-118">-이름</span><span class="sxs-lookup"><span data-stu-id="0e6ac-118">-Name</span></span>
<span data-ttu-id="0e6ac-119">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="0e6ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e6ac-121">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="0e6ac-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="0e6ac-122">-Sku</span></span>
<span data-ttu-id="0e6ac-123">용량에 대 한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="0e6ac-124">태그</span><span class="sxs-lookup"><span data-stu-id="0e6ac-124">-Tag</span></span>
<span data-ttu-id="0e6ac-125">용량에 대 한 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="0e6ac-126">-확인</span><span class="sxs-lookup"><span data-stu-id="0e6ac-126">-Confirm</span></span>
<span data-ttu-id="0e6ac-127">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="0e6ac-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0e6ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6ac-128">-WhatIf</span></span>
<span data-ttu-id="0e6ac-129">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0e6ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6ac-130">CommonParameters</span></span>
<span data-ttu-id="0e6ac-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6ac-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6ac-133">입력</span><span class="sxs-lookup"><span data-stu-id="0e6ac-133">INPUTS</span></span>

### <span data-ttu-id="0e6ac-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e6ac-134">System.String</span></span>

### <span data-ttu-id="0e6ac-135">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="0e6ac-135">System.String[]</span></span>

### <span data-ttu-id="0e6ac-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0e6ac-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e6ac-137">출력</span><span class="sxs-lookup"><span data-stu-id="0e6ac-137">OUTPUTS</span></span>

### <span data-ttu-id="0e6ac-138">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="0e6ac-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0e6ac-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0e6ac-139">NOTES</span></span>

## <span data-ttu-id="0e6ac-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e6ac-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e6ac-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e6ac-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="0e6ac-142">제거-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e6ac-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
