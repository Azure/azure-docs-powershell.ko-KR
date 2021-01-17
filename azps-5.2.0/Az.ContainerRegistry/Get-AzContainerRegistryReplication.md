---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351213"
---
# <span data-ttu-id="80285-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="80285-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="80285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80285-102">SYNOPSIS</span></span>
<span data-ttu-id="80285-103">컨테이너 레지스트리의 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="80285-104">구문</span><span class="sxs-lookup"><span data-stu-id="80285-104">SYNTAX</span></span>

### <span data-ttu-id="80285-105">ListReplicationByNameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="80285-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80285-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="80285-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80285-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80285-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80285-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80285-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80285-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80285-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80285-110">설명</span><span class="sxs-lookup"><span data-stu-id="80285-110">DESCRIPTION</span></span>
<span data-ttu-id="80285-111">Get-AzContainerRegistryReplication cmdlet은 컨테이너 레지스트리의 지정된 복제 또는 컨테이너 레지스트리의 모든 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="80285-112">예제</span><span class="sxs-lookup"><span data-stu-id="80285-112">EXAMPLES</span></span>

### <span data-ttu-id="80285-113">예제 1: 컨테이너 레지스트리의 지정된 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="80285-114">컨테이너 레지스트리의 지정된 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="80285-115">예제 2: 컨테이너 레지스트리의 모든 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="80285-116">컨테이너 레지스트리의 모든 복제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80285-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="80285-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80285-117">PARAMETERS</span></span>

### <span data-ttu-id="80285-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80285-118">-DefaultProfile</span></span>
<span data-ttu-id="80285-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80285-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80285-120">-Name</span><span class="sxs-lookup"><span data-stu-id="80285-120">-Name</span></span>
<span data-ttu-id="80285-121">Container Registry 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80285-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80285-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="80285-122">-Registry</span></span>
<span data-ttu-id="80285-123">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80285-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80285-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="80285-124">-RegistryName</span></span>
<span data-ttu-id="80285-125">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80285-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80285-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80285-126">-ResourceGroupName</span></span>
<span data-ttu-id="80285-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80285-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80285-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80285-128">-ResourceId</span></span>
<span data-ttu-id="80285-129">컨테이너 레지스트리 복제 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="80285-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="80285-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80285-130">CommonParameters</span></span>
<span data-ttu-id="80285-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80285-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80285-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80285-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80285-133">입력</span><span class="sxs-lookup"><span data-stu-id="80285-133">INPUTS</span></span>

### <span data-ttu-id="80285-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80285-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="80285-135">System.String</span><span class="sxs-lookup"><span data-stu-id="80285-135">System.String</span></span>

## <span data-ttu-id="80285-136">출력</span><span class="sxs-lookup"><span data-stu-id="80285-136">OUTPUTS</span></span>

### <span data-ttu-id="80285-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="80285-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="80285-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80285-138">NOTES</span></span>

## <span data-ttu-id="80285-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80285-139">RELATED LINKS</span></span>

[<span data-ttu-id="80285-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="80285-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="80285-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="80285-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)