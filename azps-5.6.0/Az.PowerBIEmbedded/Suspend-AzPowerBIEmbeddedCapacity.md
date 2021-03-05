---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 54c546ed7bac74a13030a9ca2f18276761e2d381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993510"
---
# <span data-ttu-id="439f3-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="439f3-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="439f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="439f3-102">SYNOPSIS</span></span>
<span data-ttu-id="439f3-103">PowerBI Embedded Capacity의 인스턴스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="439f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="439f3-104">SYNTAX</span></span>

### <span data-ttu-id="439f3-105">ByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="439f3-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439f3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="439f3-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439f3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="439f3-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439f3-108">설명</span><span class="sxs-lookup"><span data-stu-id="439f3-108">DESCRIPTION</span></span>
<span data-ttu-id="439f3-109">Suspend-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI Embedded Capacity 인스턴스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="439f3-110">예제</span><span class="sxs-lookup"><span data-stu-id="439f3-110">EXAMPLES</span></span>

### <span data-ttu-id="439f3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="439f3-111">Example 1</span></span>
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

<span data-ttu-id="439f3-112">이 명령은 리소스 그룹 테스트 그룹에서 testcapacity라는 활성 용량을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="439f3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="439f3-113">PARAMETERS</span></span>

### <span data-ttu-id="439f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439f3-114">-DefaultProfile</span></span>
<span data-ttu-id="439f3-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439f3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="439f3-116">-InputObject</span></span>
<span data-ttu-id="439f3-117">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="439f3-117">Input object for Piping</span></span>

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

### <span data-ttu-id="439f3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="439f3-118">-Name</span></span>
<span data-ttu-id="439f3-119">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="439f3-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="439f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="439f3-120">-PassThru</span></span>
<span data-ttu-id="439f3-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="439f3-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="439f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="439f3-123">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="439f3-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="439f3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="439f3-124">-ResourceId</span></span>
<span data-ttu-id="439f3-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="439f3-125">Azure resource ID</span></span>

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

### <span data-ttu-id="439f3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="439f3-126">-Confirm</span></span>
<span data-ttu-id="439f3-127">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="439f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439f3-128">-WhatIf</span></span>
<span data-ttu-id="439f3-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="439f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439f3-130">CommonParameters</span></span>
<span data-ttu-id="439f3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="439f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439f3-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="439f3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439f3-133">입력</span><span class="sxs-lookup"><span data-stu-id="439f3-133">INPUTS</span></span>

### <span data-ttu-id="439f3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="439f3-134">System.String</span></span>

### <span data-ttu-id="439f3-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="439f3-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="439f3-136">출력</span><span class="sxs-lookup"><span data-stu-id="439f3-136">OUTPUTS</span></span>

### <span data-ttu-id="439f3-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="439f3-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="439f3-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="439f3-138">NOTES</span></span>

## <span data-ttu-id="439f3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="439f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="439f3-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="439f3-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="439f3-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="439f3-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

