---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495848"
---
# <span data-ttu-id="6b52d-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6b52d-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="6b52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b52d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b52d-103">컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="6b52d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b52d-104">SYNTAX</span></span>

### <span data-ttu-id="6b52d-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b52d-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b52d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b52d-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b52d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b52d-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b52d-108">설명</span><span class="sxs-lookup"><span data-stu-id="6b52d-108">DESCRIPTION</span></span>
<span data-ttu-id="6b52d-109">New-AzContainerRegistryReplication cmdlet은 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="6b52d-110">예제</span><span class="sxs-lookup"><span data-stu-id="6b52d-110">EXAMPLES</span></span>

### <span data-ttu-id="6b52d-111">예제 1: 새 컨테이너 레지스트리 복제 만들기</span><span class="sxs-lookup"><span data-stu-id="6b52d-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="6b52d-112">새 컨테이너 레지스트리 복제를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="6b52d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b52d-113">PARAMETERS</span></span>

### <span data-ttu-id="6b52d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b52d-114">-DefaultProfile</span></span>
<span data-ttu-id="6b52d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b52d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="6b52d-116">-Location</span></span>
<span data-ttu-id="6b52d-117">Container Registry 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-117">Container Registry Location.</span></span>
<span data-ttu-id="6b52d-118">기본적으로 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6b52d-119">-Name</span></span>
<span data-ttu-id="6b52d-120">Container Registry 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="6b52d-121">기본값은 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="6b52d-122">-Registry</span></span>
<span data-ttu-id="6b52d-123">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6b52d-124">-RegistryName</span></span>
<span data-ttu-id="6b52d-125">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b52d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b52d-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b52d-128">-ResourceId</span></span>
<span data-ttu-id="6b52d-129">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6b52d-129">The container registry resource id</span></span>

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

### <span data-ttu-id="6b52d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b52d-130">-Tag</span></span>
<span data-ttu-id="6b52d-131">Container Registry 태그.</span><span class="sxs-lookup"><span data-stu-id="6b52d-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b52d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b52d-132">-Confirm</span></span>
<span data-ttu-id="6b52d-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b52d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b52d-134">-WhatIf</span></span>
<span data-ttu-id="6b52d-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6b52d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b52d-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b52d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b52d-137">CommonParameters</span></span>
<span data-ttu-id="6b52d-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b52d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b52d-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b52d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b52d-140">입력</span><span class="sxs-lookup"><span data-stu-id="6b52d-140">INPUTS</span></span>

### <span data-ttu-id="6b52d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6b52d-141">System.String</span></span>

## <span data-ttu-id="6b52d-142">출력</span><span class="sxs-lookup"><span data-stu-id="6b52d-142">OUTPUTS</span></span>

### <span data-ttu-id="6b52d-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6b52d-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="6b52d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b52d-144">NOTES</span></span>

## <span data-ttu-id="6b52d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b52d-145">RELATED LINKS</span></span>

[<span data-ttu-id="6b52d-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6b52d-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="6b52d-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6b52d-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)