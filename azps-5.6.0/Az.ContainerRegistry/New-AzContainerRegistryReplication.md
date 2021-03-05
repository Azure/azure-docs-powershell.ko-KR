---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995717"
---
# <span data-ttu-id="19510-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="19510-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="19510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19510-102">SYNOPSIS</span></span>
<span data-ttu-id="19510-103">컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19510-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="19510-104">구문</span><span class="sxs-lookup"><span data-stu-id="19510-104">SYNTAX</span></span>

### <span data-ttu-id="19510-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="19510-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19510-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19510-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19510-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19510-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19510-108">설명</span><span class="sxs-lookup"><span data-stu-id="19510-108">DESCRIPTION</span></span>
<span data-ttu-id="19510-109">New-AzContainerRegistryReplication cmdlet은 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19510-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="19510-110">예제</span><span class="sxs-lookup"><span data-stu-id="19510-110">EXAMPLES</span></span>

### <span data-ttu-id="19510-111">예제 1: 새 컨테이너 레지스트리 복제 만들기.</span><span class="sxs-lookup"><span data-stu-id="19510-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="19510-112">새 컨테이너 레지스트리 복제를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="19510-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="19510-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19510-113">PARAMETERS</span></span>

### <span data-ttu-id="19510-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19510-114">-DefaultProfile</span></span>
<span data-ttu-id="19510-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19510-116">-Location</span><span class="sxs-lookup"><span data-stu-id="19510-116">-Location</span></span>
<span data-ttu-id="19510-117">컨테이너 레지스트리 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-117">Container Registry Location.</span></span>
<span data-ttu-id="19510-118">기본적으로 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="19510-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19510-119">-Name</span></span>
<span data-ttu-id="19510-120">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="19510-121">기본적으로 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-121">Default to the location name.</span></span>

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

### <span data-ttu-id="19510-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="19510-122">-Registry</span></span>
<span data-ttu-id="19510-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="19510-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="19510-124">-RegistryName</span></span>
<span data-ttu-id="19510-125">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="19510-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19510-126">-ResourceGroupName</span></span>
<span data-ttu-id="19510-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="19510-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19510-128">-ResourceId</span></span>
<span data-ttu-id="19510-129">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="19510-129">The container registry resource id</span></span>

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

### <span data-ttu-id="19510-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="19510-130">-Tag</span></span>
<span data-ttu-id="19510-131">컨테이너 레지스트리 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="19510-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="19510-132">-확인</span><span class="sxs-lookup"><span data-stu-id="19510-132">-Confirm</span></span>
<span data-ttu-id="19510-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19510-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19510-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19510-134">-WhatIf</span></span>
<span data-ttu-id="19510-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="19510-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19510-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19510-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19510-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19510-137">CommonParameters</span></span>
<span data-ttu-id="19510-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19510-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19510-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19510-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19510-140">입력</span><span class="sxs-lookup"><span data-stu-id="19510-140">INPUTS</span></span>

### <span data-ttu-id="19510-141">System.String</span><span class="sxs-lookup"><span data-stu-id="19510-141">System.String</span></span>

## <span data-ttu-id="19510-142">출력</span><span class="sxs-lookup"><span data-stu-id="19510-142">OUTPUTS</span></span>

### <span data-ttu-id="19510-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="19510-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="19510-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19510-144">NOTES</span></span>

## <span data-ttu-id="19510-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19510-145">RELATED LINKS</span></span>

[<span data-ttu-id="19510-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="19510-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="19510-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="19510-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)