---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: cd0eab8d5670f8c37d45c8e0e211100749aa7a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016160"
---
# <span data-ttu-id="0e007-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e007-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0e007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e007-102">SYNOPSIS</span></span>
<span data-ttu-id="0e007-103">PowerBI Embedded Capacity 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="0e007-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e007-104">SYNTAX</span></span>

### <span data-ttu-id="0e007-105">ByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e007-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e007-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e007-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e007-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e007-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e007-108">설명</span><span class="sxs-lookup"><span data-stu-id="0e007-108">DESCRIPTION</span></span>
<span data-ttu-id="0e007-109">Resume-AzPowerBIEmbeddedCapacity cmdlet이 PowerBI Embedded Capacity 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="0e007-110">예제</span><span class="sxs-lookup"><span data-stu-id="0e007-110">EXAMPLES</span></span>

### <span data-ttu-id="0e007-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e007-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="0e007-112">이 명령은 리소스 그룹 테스트RG에서 testcapacity라는 일시 중지된 용량을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="0e007-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e007-113">PARAMETERS</span></span>

### <span data-ttu-id="0e007-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e007-114">-DefaultProfile</span></span>
<span data-ttu-id="0e007-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e007-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e007-116">-InputObject</span></span>
<span data-ttu-id="0e007-117">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="0e007-117">Input object for Piping</span></span>

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

### <span data-ttu-id="0e007-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0e007-118">-Name</span></span>
<span data-ttu-id="0e007-119">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="0e007-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="0e007-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e007-120">-PassThru</span></span>
<span data-ttu-id="0e007-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0e007-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0e007-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e007-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e007-123">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0e007-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="0e007-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e007-124">-ResourceId</span></span>
<span data-ttu-id="0e007-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0e007-125">Azure resource ID</span></span>

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

### <span data-ttu-id="0e007-126">-확인</span><span class="sxs-lookup"><span data-stu-id="0e007-126">-Confirm</span></span>
<span data-ttu-id="0e007-127">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0e007-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e007-128">-WhatIf</span></span>
<span data-ttu-id="0e007-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0e007-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e007-130">CommonParameters</span></span>
<span data-ttu-id="0e007-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e007-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e007-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e007-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e007-133">입력</span><span class="sxs-lookup"><span data-stu-id="0e007-133">INPUTS</span></span>

### <span data-ttu-id="0e007-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0e007-134">System.String</span></span>

### <span data-ttu-id="0e007-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e007-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0e007-136">출력</span><span class="sxs-lookup"><span data-stu-id="0e007-136">OUTPUTS</span></span>

### <span data-ttu-id="0e007-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e007-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0e007-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e007-138">NOTES</span></span>

## <span data-ttu-id="0e007-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e007-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e007-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e007-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="0e007-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0e007-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
