---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 5a6828231b276fc698179d78d3ae4bda7a4c6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950928"
---
# <span data-ttu-id="11fa3-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11fa3-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="11fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="11fa3-103">디바이스에 대한 역할 업데이트</span><span class="sxs-lookup"><span data-stu-id="11fa3-103">Updates a Role for a device</span></span>

## <span data-ttu-id="11fa3-104">구문</span><span class="sxs-lookup"><span data-stu-id="11fa3-104">SYNTAX</span></span>

### <span data-ttu-id="11fa3-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="11fa3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fa3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11fa3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fa3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11fa3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11fa3-108">설명</span><span class="sxs-lookup"><span data-stu-id="11fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="11fa3-109">**Set-AzStackEdgeRole** cmdlet은 Stack Edge 디바이스에 대한 IoT 역할을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="11fa3-110">이전 탑재된 공유는 ShareName 매개 변수에서 새로 제공된 공유로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="11fa3-111">예제</span><span class="sxs-lookup"><span data-stu-id="11fa3-111">EXAMPLES</span></span>

### <span data-ttu-id="11fa3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="11fa3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="11fa3-113">공유 이름은 이전 탑재된 공유를 새로 제공된 공유로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="11fa3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="11fa3-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="11fa3-115">모든 공유를 이산화하지 않는 경우</span><span class="sxs-lookup"><span data-stu-id="11fa3-115">To unmount all shares</span></span>

## <span data-ttu-id="11fa3-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11fa3-116">PARAMETERS</span></span>

### <span data-ttu-id="11fa3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fa3-117">-DefaultProfile</span></span>
<span data-ttu-id="11fa3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11fa3-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="11fa3-119">-DeviceName</span></span>
<span data-ttu-id="11fa3-120">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="11fa3-120">Device Name</span></span>

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

### <span data-ttu-id="11fa3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11fa3-121">-InputObject</span></span>
<span data-ttu-id="11fa3-122">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="11fa3-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="11fa3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="11fa3-123">-Name</span></span>
<span data-ttu-id="11fa3-124">역할의 이름</span><span class="sxs-lookup"><span data-stu-id="11fa3-124">Name of the Role</span></span>

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

### <span data-ttu-id="11fa3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fa3-125">-ResourceGroupName</span></span>
<span data-ttu-id="11fa3-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="11fa3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="11fa3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11fa3-127">-ResourceId</span></span>
<span data-ttu-id="11fa3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="11fa3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="11fa3-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="11fa3-129">-ShareName</span></span>
<span data-ttu-id="11fa3-130">역할의 공유</span><span class="sxs-lookup"><span data-stu-id="11fa3-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="11fa3-131">-확인</span><span class="sxs-lookup"><span data-stu-id="11fa3-131">-Confirm</span></span>
<span data-ttu-id="11fa3-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11fa3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11fa3-133">-WhatIf</span></span>
<span data-ttu-id="11fa3-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11fa3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11fa3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fa3-136">CommonParameters</span></span>
<span data-ttu-id="11fa3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11fa3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fa3-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11fa3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fa3-139">입력</span><span class="sxs-lookup"><span data-stu-id="11fa3-139">INPUTS</span></span>

### <span data-ttu-id="11fa3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="11fa3-140">System.String</span></span>

### <span data-ttu-id="11fa3-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11fa3-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="11fa3-142">출력</span><span class="sxs-lookup"><span data-stu-id="11fa3-142">OUTPUTS</span></span>

### <span data-ttu-id="11fa3-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11fa3-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="11fa3-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11fa3-144">NOTES</span></span>

## <span data-ttu-id="11fa3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11fa3-145">RELATED LINKS</span></span>
