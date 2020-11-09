---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304118"
---
# <span data-ttu-id="51058-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="51058-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="51058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51058-102">SYNOPSIS</span></span>
<span data-ttu-id="51058-103">컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51058-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="51058-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51058-104">SYNTAX</span></span>

### <span data-ttu-id="51058-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="51058-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51058-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51058-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51058-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51058-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51058-108">설명은</span><span class="sxs-lookup"><span data-stu-id="51058-108">DESCRIPTION</span></span>
<span data-ttu-id="51058-109">New-AzContainerRegistryReplication cmdlet은 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51058-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="51058-110">예제의</span><span class="sxs-lookup"><span data-stu-id="51058-110">EXAMPLES</span></span>

### <span data-ttu-id="51058-111">예제 1: 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51058-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="51058-112">새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51058-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="51058-113">변수</span><span class="sxs-lookup"><span data-stu-id="51058-113">PARAMETERS</span></span>

### <span data-ttu-id="51058-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51058-114">-DefaultProfile</span></span>
<span data-ttu-id="51058-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51058-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51058-116">-위치</span><span class="sxs-lookup"><span data-stu-id="51058-116">-Location</span></span>
<span data-ttu-id="51058-117">컨테이너 레지스트리 위치.</span><span class="sxs-lookup"><span data-stu-id="51058-117">Container Registry Location.</span></span>
<span data-ttu-id="51058-118">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="51058-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="51058-119">-이름</span><span class="sxs-lookup"><span data-stu-id="51058-119">-Name</span></span>
<span data-ttu-id="51058-120">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51058-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="51058-121">위치 이름을 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="51058-121">Default to the location name.</span></span>

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

### <span data-ttu-id="51058-122">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="51058-122">-Registry</span></span>
<span data-ttu-id="51058-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="51058-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="51058-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="51058-124">-RegistryName</span></span>
<span data-ttu-id="51058-125">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51058-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="51058-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51058-126">-ResourceGroupName</span></span>
<span data-ttu-id="51058-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51058-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="51058-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51058-128">-ResourceId</span></span>
<span data-ttu-id="51058-129">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="51058-129">The container registry resource id</span></span>

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

### <span data-ttu-id="51058-130">태그</span><span class="sxs-lookup"><span data-stu-id="51058-130">-Tag</span></span>
<span data-ttu-id="51058-131">컨테이너 레지스트리 태그</span><span class="sxs-lookup"><span data-stu-id="51058-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="51058-132">-확인</span><span class="sxs-lookup"><span data-stu-id="51058-132">-Confirm</span></span>
<span data-ttu-id="51058-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51058-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51058-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51058-134">-WhatIf</span></span>
<span data-ttu-id="51058-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51058-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51058-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51058-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51058-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51058-137">CommonParameters</span></span>
<span data-ttu-id="51058-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51058-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51058-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51058-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51058-140">입력</span><span class="sxs-lookup"><span data-stu-id="51058-140">INPUTS</span></span>

### <span data-ttu-id="51058-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51058-141">System.String</span></span>

## <span data-ttu-id="51058-142">출력</span><span class="sxs-lookup"><span data-stu-id="51058-142">OUTPUTS</span></span>

### <span data-ttu-id="51058-143">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="51058-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="51058-144">상속자</span><span class="sxs-lookup"><span data-stu-id="51058-144">NOTES</span></span>

## <span data-ttu-id="51058-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51058-145">RELATED LINKS</span></span>

[<span data-ttu-id="51058-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="51058-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="51058-147">제거-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="51058-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)