---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701977"
---
# <span data-ttu-id="2ac3b-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2ac3b-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="2ac3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac3b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac3b-103">컨테이너 레지스트리의 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ac3b-104">SYNTAX</span></span>

### <span data-ttu-id="2ac3b-105">ListReplicationByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2ac3b-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ac3b-110">설명은</span><span class="sxs-lookup"><span data-stu-id="2ac3b-110">DESCRIPTION</span></span>
<span data-ttu-id="2ac3b-111">Get-AzureRmContainerRegistryReplication cmdlet은 컨테이너 레지스트리의 지정 된 복제 또는 컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="2ac3b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2ac3b-112">EXAMPLES</span></span>

### <span data-ttu-id="2ac3b-113">예제 1: 컨테이너 레지스트리의 지정 된 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2ac3b-114">컨테이너 레지스트리의 지정 된 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="2ac3b-115">예제 2: 컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2ac3b-116">컨테이너 레지스트리의 모든 복제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="2ac3b-117">변수</span><span class="sxs-lookup"><span data-stu-id="2ac3b-117">PARAMETERS</span></span>

### <span data-ttu-id="2ac3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac3b-118">-DefaultProfile</span></span>
<span data-ttu-id="2ac3b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac3b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2ac3b-120">-Name</span></span>
<span data-ttu-id="2ac3b-121">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="2ac3b-122">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="2ac3b-122">-Registry</span></span>
<span data-ttu-id="2ac3b-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="2ac3b-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2ac3b-124">-RegistryName</span></span>
<span data-ttu-id="2ac3b-125">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="2ac3b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac3b-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ac3b-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ac3b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac3b-128">-ResourceId</span></span>
<span data-ttu-id="2ac3b-129">컨테이너 레지스트리 복제 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2ac3b-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="2ac3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac3b-130">CommonParameters</span></span>
<span data-ttu-id="2ac3b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac3b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac3b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac3b-133">입력</span><span class="sxs-lookup"><span data-stu-id="2ac3b-133">INPUTS</span></span>

### <span data-ttu-id="2ac3b-134">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2ac3b-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="2ac3b-135">매개 변수: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ac3b-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="2ac3b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ac3b-136">System.String</span></span>

## <span data-ttu-id="2ac3b-137">출력</span><span class="sxs-lookup"><span data-stu-id="2ac3b-137">OUTPUTS</span></span>

### <span data-ttu-id="2ac3b-138">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2ac3b-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="2ac3b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2ac3b-139">NOTES</span></span>

## <span data-ttu-id="2ac3b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ac3b-140">RELATED LINKS</span></span>

[<span data-ttu-id="2ac3b-141">새로운 AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2ac3b-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="2ac3b-142">제거-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2ac3b-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
