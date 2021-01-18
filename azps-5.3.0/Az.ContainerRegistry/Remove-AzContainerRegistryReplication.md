---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493751"
---
# <span data-ttu-id="57613-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="57613-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="57613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57613-102">SYNOPSIS</span></span>
<span data-ttu-id="57613-103">컨테이너 레지스트리 복제를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57613-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="57613-104">구문</span><span class="sxs-lookup"><span data-stu-id="57613-104">SYNTAX</span></span>

### <span data-ttu-id="57613-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="57613-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57613-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57613-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57613-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57613-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57613-108">설명</span><span class="sxs-lookup"><span data-stu-id="57613-108">DESCRIPTION</span></span>
<span data-ttu-id="57613-109">Remove-AzContainerRegistryReplication cmdlet은 컨테이너 레지스트리 복제를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57613-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="57613-110">예제</span><span class="sxs-lookup"><span data-stu-id="57613-110">EXAMPLES</span></span>

### <span data-ttu-id="57613-111">예제 1: 컨테이너 레지스트리 복제를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57613-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="57613-112">컨테이너 레지스트리 복제를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57613-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="57613-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57613-113">PARAMETERS</span></span>

### <span data-ttu-id="57613-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57613-114">-DefaultProfile</span></span>
<span data-ttu-id="57613-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57613-116">-Name</span><span class="sxs-lookup"><span data-stu-id="57613-116">-Name</span></span>
<span data-ttu-id="57613-117">Container Registry 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="57613-118">기본값은 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57613-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57613-119">-PassThru</span></span>
<span data-ttu-id="57613-120">제거에 성공하면 이 cmdlet이 true를 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="57613-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="57613-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="57613-121">-RegistryName</span></span>
<span data-ttu-id="57613-122">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57613-123">-Replication</span><span class="sxs-lookup"><span data-stu-id="57613-123">-Replication</span></span>
<span data-ttu-id="57613-124">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57613-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57613-125">-ResourceGroupName</span></span>
<span data-ttu-id="57613-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57613-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57613-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57613-127">-ResourceId</span></span>
<span data-ttu-id="57613-128">컨테이너 레지스트리 복제 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="57613-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57613-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57613-129">-Confirm</span></span>
<span data-ttu-id="57613-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57613-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57613-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57613-131">-WhatIf</span></span>
<span data-ttu-id="57613-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57613-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57613-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57613-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57613-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57613-134">CommonParameters</span></span>
<span data-ttu-id="57613-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57613-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57613-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57613-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57613-137">입력</span><span class="sxs-lookup"><span data-stu-id="57613-137">INPUTS</span></span>

### <span data-ttu-id="57613-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="57613-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="57613-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57613-139">System.String</span></span>

## <span data-ttu-id="57613-140">출력</span><span class="sxs-lookup"><span data-stu-id="57613-140">OUTPUTS</span></span>

### <span data-ttu-id="57613-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57613-141">System.Boolean</span></span>

## <span data-ttu-id="57613-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57613-142">NOTES</span></span>

## <span data-ttu-id="57613-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57613-143">RELATED LINKS</span></span>

[<span data-ttu-id="57613-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="57613-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="57613-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="57613-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

