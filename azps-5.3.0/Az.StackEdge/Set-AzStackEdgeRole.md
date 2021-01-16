---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374284"
---
# <span data-ttu-id="eefc8-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="eefc8-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="eefc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefc8-102">SYNOPSIS</span></span>
<span data-ttu-id="eefc8-103">디바이스에 대한 역할 업데이트</span><span class="sxs-lookup"><span data-stu-id="eefc8-103">Updates a Role for a device</span></span>

## <span data-ttu-id="eefc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="eefc8-104">SYNTAX</span></span>

### <span data-ttu-id="eefc8-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eefc8-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefc8-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefc8-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefc8-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefc8-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefc8-108">설명</span><span class="sxs-lookup"><span data-stu-id="eefc8-108">DESCRIPTION</span></span>
<span data-ttu-id="eefc8-109">**Set-AzStackEdgeRole** cmdlet은 Stack Edge 디바이스에 대한 IoT 역할을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="eefc8-110">탑재된 이전 공유는 ShareName 매개 변수에서 새로 제공된 공유로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="eefc8-111">예제</span><span class="sxs-lookup"><span data-stu-id="eefc8-111">EXAMPLES</span></span>

### <span data-ttu-id="eefc8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="eefc8-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="eefc8-113">공유 이름은 탑재된 이전 공유를 새로 제공된 공유로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="eefc8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="eefc8-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="eefc8-115">모든 공유의 마운트 언마운트</span><span class="sxs-lookup"><span data-stu-id="eefc8-115">To unmount all shares</span></span>

## <span data-ttu-id="eefc8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefc8-116">PARAMETERS</span></span>

### <span data-ttu-id="eefc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefc8-117">-DefaultProfile</span></span>
<span data-ttu-id="eefc8-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefc8-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eefc8-119">-DeviceName</span></span>
<span data-ttu-id="eefc8-120">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="eefc8-120">Device Name</span></span>

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

### <span data-ttu-id="eefc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eefc8-121">-InputObject</span></span>
<span data-ttu-id="eefc8-122">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="eefc8-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eefc8-123">-Name</span></span>
<span data-ttu-id="eefc8-124">역할의 이름</span><span class="sxs-lookup"><span data-stu-id="eefc8-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefc8-125">-ResourceGroupName</span></span>
<span data-ttu-id="eefc8-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eefc8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eefc8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eefc8-127">-ResourceId</span></span>
<span data-ttu-id="eefc8-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eefc8-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="eefc8-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eefc8-129">-ShareName</span></span>
<span data-ttu-id="eefc8-130">역할의 공유</span><span class="sxs-lookup"><span data-stu-id="eefc8-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eefc8-131">-Confirm</span></span>
<span data-ttu-id="eefc8-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefc8-133">-WhatIf</span></span>
<span data-ttu-id="eefc8-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eefc8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eefc8-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefc8-136">CommonParameters</span></span>
<span data-ttu-id="eefc8-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eefc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefc8-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eefc8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefc8-139">입력</span><span class="sxs-lookup"><span data-stu-id="eefc8-139">INPUTS</span></span>

### <span data-ttu-id="eefc8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="eefc8-140">System.String</span></span>

### <span data-ttu-id="eefc8-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="eefc8-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="eefc8-142">출력</span><span class="sxs-lookup"><span data-stu-id="eefc8-142">OUTPUTS</span></span>

### <span data-ttu-id="eefc8-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="eefc8-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="eefc8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eefc8-144">NOTES</span></span>

## <span data-ttu-id="eefc8-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eefc8-145">RELATED LINKS</span></span>
