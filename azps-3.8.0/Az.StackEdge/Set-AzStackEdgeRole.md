---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043897"
---
# <span data-ttu-id="8942b-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8942b-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="8942b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8942b-102">SYNOPSIS</span></span>
<span data-ttu-id="8942b-103">장치에 대 한 역할 업데이트</span><span class="sxs-lookup"><span data-stu-id="8942b-103">Updates a Role for a device</span></span>

## <span data-ttu-id="8942b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8942b-104">SYNTAX</span></span>

### <span data-ttu-id="8942b-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8942b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8942b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8942b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8942b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8942b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8942b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8942b-108">DESCRIPTION</span></span>
<span data-ttu-id="8942b-109">**AzStackEdgeRole** Cmdlet은 스택 경계 장치에 대 한 IoT 역할을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="8942b-110">이전에 탑재 된 공유가 ShareName 매개 변수에서 새로 제공 된 공유로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="8942b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8942b-111">EXAMPLES</span></span>

### <span data-ttu-id="8942b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8942b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="8942b-113">공유 이름으로 이전에 탑재 된 공유를 새로 제공 된 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="8942b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8942b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="8942b-115">모든 공유를 탑재 해제 하려면</span><span class="sxs-lookup"><span data-stu-id="8942b-115">To unmount all shares</span></span>

## <span data-ttu-id="8942b-116">변수</span><span class="sxs-lookup"><span data-stu-id="8942b-116">PARAMETERS</span></span>

### <span data-ttu-id="8942b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8942b-117">-DefaultProfile</span></span>
<span data-ttu-id="8942b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8942b-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="8942b-119">-DeviceName</span></span>
<span data-ttu-id="8942b-120">장치 이름</span><span class="sxs-lookup"><span data-stu-id="8942b-120">Device Name</span></span>

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

### <span data-ttu-id="8942b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8942b-121">-InputObject</span></span>
<span data-ttu-id="8942b-122">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8942b-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8942b-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8942b-123">-Name</span></span>
<span data-ttu-id="8942b-124">역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-124">Name of the Role</span></span>

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

### <span data-ttu-id="8942b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8942b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8942b-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8942b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8942b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8942b-127">-ResourceId</span></span>
<span data-ttu-id="8942b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8942b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8942b-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8942b-129">-ShareName</span></span>
<span data-ttu-id="8942b-130">역할의 공유</span><span class="sxs-lookup"><span data-stu-id="8942b-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="8942b-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8942b-131">-Confirm</span></span>
<span data-ttu-id="8942b-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8942b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8942b-133">-WhatIf</span></span>
<span data-ttu-id="8942b-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8942b-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8942b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8942b-136">CommonParameters</span></span>
<span data-ttu-id="8942b-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8942b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8942b-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8942b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8942b-139">입력</span><span class="sxs-lookup"><span data-stu-id="8942b-139">INPUTS</span></span>

### <span data-ttu-id="8942b-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8942b-140">System.String</span></span>

### <span data-ttu-id="8942b-141">StackEdge. PSStackEdgeRole에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8942b-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="8942b-142">출력</span><span class="sxs-lookup"><span data-stu-id="8942b-142">OUTPUTS</span></span>

### <span data-ttu-id="8942b-143">StackEdge. PSStackEdgeRole에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8942b-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="8942b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8942b-144">NOTES</span></span>

## <span data-ttu-id="8942b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8942b-145">RELATED LINKS</span></span>
