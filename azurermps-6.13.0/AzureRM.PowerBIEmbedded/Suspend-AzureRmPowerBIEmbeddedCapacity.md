---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702588"
---
# <span data-ttu-id="4912f-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4912f-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4912f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4912f-102">SYNOPSIS</span></span>
<span data-ttu-id="4912f-103">PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4912f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4912f-104">SYNTAX</span></span>

### <span data-ttu-id="4912f-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="4912f-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4912f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4912f-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4912f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4912f-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4912f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4912f-108">DESCRIPTION</span></span>
<span data-ttu-id="4912f-109">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4912f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4912f-110">EXAMPLES</span></span>

### <span data-ttu-id="4912f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4912f-111">Example 1</span></span>
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

<span data-ttu-id="4912f-112">이 명령은 resourcegroup testcapacity에서 testcapacity 이라는 활성 용량을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4912f-113">변수</span><span class="sxs-lookup"><span data-stu-id="4912f-113">PARAMETERS</span></span>

### <span data-ttu-id="4912f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4912f-114">-DefaultProfile</span></span>
<span data-ttu-id="4912f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4912f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4912f-116">-InputObject</span></span>
<span data-ttu-id="4912f-117">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="4912f-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4912f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4912f-118">-Name</span></span>
<span data-ttu-id="4912f-119">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4912f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4912f-120">-PassThru</span></span>
<span data-ttu-id="4912f-121">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="4912f-121">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4912f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4912f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4912f-123">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4912f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4912f-124">-ResourceId</span></span>
<span data-ttu-id="4912f-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4912f-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4912f-126">-확인</span><span class="sxs-lookup"><span data-stu-id="4912f-126">-Confirm</span></span>
<span data-ttu-id="4912f-127">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="4912f-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4912f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4912f-128">-WhatIf</span></span>
<span data-ttu-id="4912f-129">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4912f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4912f-130">CommonParameters</span></span>
<span data-ttu-id="4912f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4912f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4912f-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4912f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4912f-133">입력</span><span class="sxs-lookup"><span data-stu-id="4912f-133">INPUTS</span></span>

### <span data-ttu-id="4912f-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4912f-134">System.String</span></span>

### <span data-ttu-id="4912f-135">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="4912f-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="4912f-136">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4912f-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4912f-137">출력</span><span class="sxs-lookup"><span data-stu-id="4912f-137">OUTPUTS</span></span>

### <span data-ttu-id="4912f-138">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="4912f-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4912f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4912f-139">NOTES</span></span>

## <span data-ttu-id="4912f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4912f-140">RELATED LINKS</span></span>

[<span data-ttu-id="4912f-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4912f-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4912f-142">이력서-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4912f-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

