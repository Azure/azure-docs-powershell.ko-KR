---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366017"
---
# <span data-ttu-id="a6dc5-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a6dc5-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="a6dc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dc5-103">디바이스에 대한 역할 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6dc5-103">Updates a Role for a device</span></span>

## <span data-ttu-id="a6dc5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6dc5-104">SYNTAX</span></span>

### <span data-ttu-id="a6dc5-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6dc5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6dc5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6dc5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6dc5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6dc5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6dc5-108">설명</span><span class="sxs-lookup"><span data-stu-id="a6dc5-108">DESCRIPTION</span></span>
<span data-ttu-id="a6dc5-109">**Set-AzDataBoxEdgeRole** cmdlet은 Data Box Edge 디바이스에 대한 IoT 역할을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="a6dc5-110">탑재된 이전 공유는 ShareName 매개 변수에서 새로 제공된 공유로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="a6dc5-111">예제</span><span class="sxs-lookup"><span data-stu-id="a6dc5-111">EXAMPLES</span></span>

### <span data-ttu-id="a6dc5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6dc5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="a6dc5-113">공유 이름은 탑재된 이전 공유를 새로 제공된 공유로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="a6dc5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a6dc5-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="a6dc5-115">모든 공유의 마운트 언마운트</span><span class="sxs-lookup"><span data-stu-id="a6dc5-115">To unmount all shares</span></span>

## <span data-ttu-id="a6dc5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6dc5-116">PARAMETERS</span></span>

### <span data-ttu-id="a6dc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dc5-117">-DefaultProfile</span></span>
<span data-ttu-id="a6dc5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6dc5-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a6dc5-119">-DeviceName</span></span>
<span data-ttu-id="a6dc5-120">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="a6dc5-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6dc5-121">-InputObject</span></span>
<span data-ttu-id="a6dc5-122">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a6dc5-123">-Name</span></span>
<span data-ttu-id="a6dc5-124">역할의 이름</span><span class="sxs-lookup"><span data-stu-id="a6dc5-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6dc5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6dc5-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a6dc5-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6dc5-127">-ResourceId</span></span>
<span data-ttu-id="a6dc5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6dc5-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a6dc5-129">-ShareName</span></span>
<span data-ttu-id="a6dc5-130">역할의 공유</span><span class="sxs-lookup"><span data-stu-id="a6dc5-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6dc5-131">-Confirm</span></span>
<span data-ttu-id="a6dc5-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6dc5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6dc5-133">-WhatIf</span></span>
<span data-ttu-id="a6dc5-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6dc5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6dc5-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6dc5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dc5-136">CommonParameters</span></span>
<span data-ttu-id="a6dc5-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6dc5-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6dc5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dc5-139">입력</span><span class="sxs-lookup"><span data-stu-id="a6dc5-139">INPUTS</span></span>

### <span data-ttu-id="a6dc5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a6dc5-140">System.String</span></span>

### <span data-ttu-id="a6dc5-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a6dc5-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="a6dc5-142">출력</span><span class="sxs-lookup"><span data-stu-id="a6dc5-142">OUTPUTS</span></span>

### <span data-ttu-id="a6dc5-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a6dc5-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="a6dc5-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6dc5-144">NOTES</span></span>

## <span data-ttu-id="a6dc5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6dc5-145">RELATED LINKS</span></span>