---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204618"
---
# <span data-ttu-id="7ffb0-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7ffb0-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="7ffb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ffb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffb0-103">컨테이너 레지스트리의 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="7ffb0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ffb0-104">SYNTAX</span></span>

### <span data-ttu-id="7ffb0-105">ListReplicationByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ffb0-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ffb0-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffb0-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ffb0-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffb0-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ffb0-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffb0-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ffb0-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffb0-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ffb0-110">설명은</span><span class="sxs-lookup"><span data-stu-id="7ffb0-110">DESCRIPTION</span></span>
<span data-ttu-id="7ffb0-111">Get-AzContainerRegistryReplication cmdlet은 컨테이너 레지스트리의 지정 된 복제 또는 컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="7ffb0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7ffb0-112">EXAMPLES</span></span>

### <span data-ttu-id="7ffb0-113">예제 1: 컨테이너 레지스트리의 지정 된 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="7ffb0-114">컨테이너 레지스트리의 지정 된 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="7ffb0-115">예제 2: 컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="7ffb0-116">컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="7ffb0-117">변수</span><span class="sxs-lookup"><span data-stu-id="7ffb0-117">PARAMETERS</span></span>

### <span data-ttu-id="7ffb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffb0-118">-DefaultProfile</span></span>
<span data-ttu-id="7ffb0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ffb0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7ffb0-120">-Name</span></span>
<span data-ttu-id="7ffb0-121">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="7ffb0-122">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="7ffb0-122">-Registry</span></span>
<span data-ttu-id="7ffb0-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="7ffb0-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7ffb0-124">-RegistryName</span></span>
<span data-ttu-id="7ffb0-125">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="7ffb0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffb0-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ffb0-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ffb0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffb0-128">-ResourceId</span></span>
<span data-ttu-id="7ffb0-129">컨테이너 레지스트리 복제 리소스 id</span><span class="sxs-lookup"><span data-stu-id="7ffb0-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="7ffb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffb0-130">CommonParameters</span></span>
<span data-ttu-id="7ffb0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffb0-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ffb0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffb0-133">입력</span><span class="sxs-lookup"><span data-stu-id="7ffb0-133">INPUTS</span></span>

### <span data-ttu-id="7ffb0-134">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7ffb0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="7ffb0-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7ffb0-135">System.String</span></span>

## <span data-ttu-id="7ffb0-136">출력</span><span class="sxs-lookup"><span data-stu-id="7ffb0-136">OUTPUTS</span></span>

### <span data-ttu-id="7ffb0-137">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7ffb0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="7ffb0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7ffb0-138">NOTES</span></span>

## <span data-ttu-id="7ffb0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ffb0-139">RELATED LINKS</span></span>

[<span data-ttu-id="7ffb0-140">새로운 AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7ffb0-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="7ffb0-141">제거-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7ffb0-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)