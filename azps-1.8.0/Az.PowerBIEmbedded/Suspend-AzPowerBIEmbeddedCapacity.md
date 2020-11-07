---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699800"
---
# <span data-ttu-id="29e2c-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="29e2c-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="29e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="29e2c-103">PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="29e2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29e2c-104">SYNTAX</span></span>

### <span data-ttu-id="29e2c-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="29e2c-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29e2c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29e2c-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29e2c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29e2c-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29e2c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="29e2c-109">Suspend-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="29e2c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="29e2c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="29e2c-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="29e2c-112">이 명령은 resourcegroup testcapacity에서 testcapacity 이라는 활성 용량을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="29e2c-113">변수</span><span class="sxs-lookup"><span data-stu-id="29e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="29e2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e2c-114">-DefaultProfile</span></span>
<span data-ttu-id="29e2c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e2c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29e2c-116">-InputObject</span></span>
<span data-ttu-id="29e2c-117">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="29e2c-117">Input object for Piping</span></span>

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

### <span data-ttu-id="29e2c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="29e2c-118">-Name</span></span>
<span data-ttu-id="29e2c-119">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="29e2c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29e2c-120">-PassThru</span></span>
<span data-ttu-id="29e2c-121">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="29e2c-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29e2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="29e2c-123">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="29e2c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29e2c-124">-ResourceId</span></span>
<span data-ttu-id="29e2c-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="29e2c-125">Azure resource ID</span></span>

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

### <span data-ttu-id="29e2c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="29e2c-126">-Confirm</span></span>
<span data-ttu-id="29e2c-127">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="29e2c-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="29e2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e2c-128">-WhatIf</span></span>
<span data-ttu-id="29e2c-129">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="29e2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e2c-130">CommonParameters</span></span>
<span data-ttu-id="29e2c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e2c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e2c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e2c-133">입력</span><span class="sxs-lookup"><span data-stu-id="29e2c-133">INPUTS</span></span>

### <span data-ttu-id="29e2c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29e2c-134">System.String</span></span>

### <span data-ttu-id="29e2c-135">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="29e2c-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="29e2c-136">출력</span><span class="sxs-lookup"><span data-stu-id="29e2c-136">OUTPUTS</span></span>

### <span data-ttu-id="29e2c-137">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="29e2c-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="29e2c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="29e2c-138">NOTES</span></span>

## <span data-ttu-id="29e2c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29e2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="29e2c-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="29e2c-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="29e2c-141">이력서-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="29e2c-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

