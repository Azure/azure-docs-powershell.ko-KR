---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 93c15d2675cc0e3e5fe0b37bc5af331ce97e7d8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953451"
---
# <span data-ttu-id="9cab0-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9cab0-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9cab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cab0-102">SYNOPSIS</span></span>
<span data-ttu-id="9cab0-103">PowerBI Embedded Capacity의 인스턴스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="9cab0-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cab0-104">SYNTAX</span></span>

### <span data-ttu-id="9cab0-105">ByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="9cab0-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cab0-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9cab0-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cab0-108">설명</span><span class="sxs-lookup"><span data-stu-id="9cab0-108">DESCRIPTION</span></span>
<span data-ttu-id="9cab0-109">Remove-AzPowerBIEmbeddedCapacity cmdlet에서 PowerBI Embedded Capacity 인스턴스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="9cab0-110">예제</span><span class="sxs-lookup"><span data-stu-id="9cab0-110">EXAMPLES</span></span>

### <span data-ttu-id="9cab0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9cab0-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="9cab0-112">이 명령은 리소스 그룹 테스트RG에서 testcapacity라는 용량을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="9cab0-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9cab0-113">PARAMETERS</span></span>

### <span data-ttu-id="9cab0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cab0-114">-DefaultProfile</span></span>
<span data-ttu-id="9cab0-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cab0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cab0-116">-InputObject</span></span>
<span data-ttu-id="9cab0-117">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="9cab0-117">Input object for Piping</span></span>

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

### <span data-ttu-id="9cab0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9cab0-118">-Name</span></span>
<span data-ttu-id="9cab0-119">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="9cab0-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="9cab0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cab0-120">-PassThru</span></span>
<span data-ttu-id="9cab0-121">작업이 성공적으로 완료되면 삭제된 용량 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="9cab0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cab0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cab0-123">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9cab0-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="9cab0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cab0-124">-ResourceId</span></span>
<span data-ttu-id="9cab0-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9cab0-125">Azure resource ID</span></span>

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

### <span data-ttu-id="9cab0-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9cab0-126">-Confirm</span></span>
<span data-ttu-id="9cab0-127">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9cab0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cab0-128">-WhatIf</span></span>
<span data-ttu-id="9cab0-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9cab0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cab0-130">CommonParameters</span></span>
<span data-ttu-id="9cab0-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cab0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cab0-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9cab0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cab0-133">입력</span><span class="sxs-lookup"><span data-stu-id="9cab0-133">INPUTS</span></span>

### <span data-ttu-id="9cab0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9cab0-134">System.String</span></span>

### <span data-ttu-id="9cab0-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9cab0-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9cab0-136">출력</span><span class="sxs-lookup"><span data-stu-id="9cab0-136">OUTPUTS</span></span>

### <span data-ttu-id="9cab0-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9cab0-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9cab0-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cab0-138">NOTES</span></span>

## <span data-ttu-id="9cab0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cab0-139">RELATED LINKS</span></span>

[<span data-ttu-id="9cab0-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9cab0-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="9cab0-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9cab0-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
