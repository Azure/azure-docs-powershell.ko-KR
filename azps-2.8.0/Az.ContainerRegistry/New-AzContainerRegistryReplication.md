---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: 2f5e310df06650b2c8f2506910c80dbf0ea440bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697124"
---
# <span data-ttu-id="b7251-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b7251-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="b7251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7251-102">SYNOPSIS</span></span>
<span data-ttu-id="b7251-103">컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="b7251-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7251-104">SYNTAX</span></span>

### <span data-ttu-id="b7251-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7251-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7251-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7251-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7251-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7251-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7251-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b7251-108">DESCRIPTION</span></span>
<span data-ttu-id="b7251-109">New-AzContainerRegistryReplication cmdlet은 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="b7251-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b7251-110">EXAMPLES</span></span>

### <span data-ttu-id="b7251-111">예제 1: 새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="b7251-112">새 컨테이너 레지스트리 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="b7251-113">변수</span><span class="sxs-lookup"><span data-stu-id="b7251-113">PARAMETERS</span></span>

### <span data-ttu-id="b7251-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7251-114">-DefaultProfile</span></span>
<span data-ttu-id="b7251-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7251-116">-위치</span><span class="sxs-lookup"><span data-stu-id="b7251-116">-Location</span></span>
<span data-ttu-id="b7251-117">컨테이너 레지스트리 위치.</span><span class="sxs-lookup"><span data-stu-id="b7251-117">Container Registry Location.</span></span>
<span data-ttu-id="b7251-118">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="b7251-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b7251-119">-Name</span></span>
<span data-ttu-id="b7251-120">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="b7251-121">위치 이름을 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-121">Default to the location name.</span></span>

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

### <span data-ttu-id="b7251-122">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="b7251-122">-Registry</span></span>
<span data-ttu-id="b7251-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="b7251-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b7251-124">-RegistryName</span></span>
<span data-ttu-id="b7251-125">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="b7251-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7251-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7251-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7251-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7251-128">-ResourceId</span></span>
<span data-ttu-id="b7251-129">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="b7251-129">The container registry resource id</span></span>

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

### <span data-ttu-id="b7251-130">태그</span><span class="sxs-lookup"><span data-stu-id="b7251-130">-Tag</span></span>
<span data-ttu-id="b7251-131">컨테이너 레지스트리 태그</span><span class="sxs-lookup"><span data-stu-id="b7251-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="b7251-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b7251-132">-Confirm</span></span>
<span data-ttu-id="b7251-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7251-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7251-134">-WhatIf</span></span>
<span data-ttu-id="b7251-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7251-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7251-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7251-137">CommonParameters</span></span>
<span data-ttu-id="b7251-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7251-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7251-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7251-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7251-140">입력</span><span class="sxs-lookup"><span data-stu-id="b7251-140">INPUTS</span></span>

### <span data-ttu-id="b7251-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b7251-141">System.String</span></span>

## <span data-ttu-id="b7251-142">출력</span><span class="sxs-lookup"><span data-stu-id="b7251-142">OUTPUTS</span></span>

### <span data-ttu-id="b7251-143">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b7251-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="b7251-144">상속자</span><span class="sxs-lookup"><span data-stu-id="b7251-144">NOTES</span></span>

## <span data-ttu-id="b7251-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7251-145">RELATED LINKS</span></span>

[<span data-ttu-id="b7251-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b7251-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="b7251-147">제거-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b7251-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)