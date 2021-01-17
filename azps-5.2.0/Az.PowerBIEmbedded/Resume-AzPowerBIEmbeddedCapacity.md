---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371841"
---
# <span data-ttu-id="6e54b-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6e54b-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6e54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e54b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e54b-103">PowerBI Embedded Capacity의 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="6e54b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e54b-104">SYNTAX</span></span>

### <span data-ttu-id="6e54b-105">ByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="6e54b-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e54b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e54b-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e54b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e54b-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e54b-108">설명</span><span class="sxs-lookup"><span data-stu-id="6e54b-108">DESCRIPTION</span></span>
<span data-ttu-id="6e54b-109">Resume-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI Embedded Capacity의 인스턴스를 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="6e54b-110">예제</span><span class="sxs-lookup"><span data-stu-id="6e54b-110">EXAMPLES</span></span>

### <span data-ttu-id="6e54b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e54b-111">Example 1</span></span>
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

<span data-ttu-id="6e54b-112">이 명령은 resourcegroup testRG에서 testcapacity라는 일시 중지된 용량을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="6e54b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e54b-113">PARAMETERS</span></span>

### <span data-ttu-id="6e54b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e54b-114">-DefaultProfile</span></span>
<span data-ttu-id="6e54b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e54b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e54b-116">-InputObject</span></span>
<span data-ttu-id="6e54b-117">파이핑에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="6e54b-117">Input object for Piping</span></span>

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

### <span data-ttu-id="6e54b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6e54b-118">-Name</span></span>
<span data-ttu-id="6e54b-119">PowerBI 포함된 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="6e54b-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="6e54b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e54b-120">-PassThru</span></span>
<span data-ttu-id="6e54b-121">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="6e54b-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6e54b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e54b-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e54b-123">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="6e54b-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="6e54b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e54b-124">-ResourceId</span></span>
<span data-ttu-id="6e54b-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6e54b-125">Azure resource ID</span></span>

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

### <span data-ttu-id="6e54b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e54b-126">-Confirm</span></span>
<span data-ttu-id="6e54b-127">사용자에게 작업을 수행할지 여부를 확인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6e54b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e54b-128">-WhatIf</span></span>
<span data-ttu-id="6e54b-129">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6e54b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e54b-130">CommonParameters</span></span>
<span data-ttu-id="6e54b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e54b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e54b-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e54b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e54b-133">입력</span><span class="sxs-lookup"><span data-stu-id="6e54b-133">INPUTS</span></span>

### <span data-ttu-id="6e54b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6e54b-134">System.String</span></span>

### <span data-ttu-id="6e54b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6e54b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6e54b-136">출력</span><span class="sxs-lookup"><span data-stu-id="6e54b-136">OUTPUTS</span></span>

### <span data-ttu-id="6e54b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6e54b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6e54b-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e54b-138">NOTES</span></span>

## <span data-ttu-id="6e54b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e54b-139">RELATED LINKS</span></span>

[<span data-ttu-id="6e54b-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6e54b-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6e54b-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6e54b-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
