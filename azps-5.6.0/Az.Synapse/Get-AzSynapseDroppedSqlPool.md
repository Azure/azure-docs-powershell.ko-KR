---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981835"
---
# <span data-ttu-id="2526b-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="2526b-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="2526b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2526b-102">SYNOPSIS</span></span>
<span data-ttu-id="2526b-103">Synapse Sql Pool의 삭제된 Sql Pool 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="2526b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2526b-104">SYNTAX</span></span>

### <span data-ttu-id="2526b-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2526b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2526b-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="2526b-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2526b-107">설명</span><span class="sxs-lookup"><span data-stu-id="2526b-107">DESCRIPTION</span></span>
<span data-ttu-id="2526b-108">**Get-AzSynapseDroppedSqlPool** cmdlet은 복원할 수 SQL 지정된 삭제된 풀 백업 또는 작업 영역에서 복원할 수 있는 모든 삭제된 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="2526b-109">예제</span><span class="sxs-lookup"><span data-stu-id="2526b-109">EXAMPLES</span></span>

### <span data-ttu-id="2526b-110">예제 1: SQL 풀에서 지정된 삭제된 sqlpools를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="2526b-111">cmdlet은 SQL 풀에 대해 삭제된 sqlpool을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="2526b-112">예제 2: 작업 영역의 모든 삭제된 sqlpool 사용</span><span class="sxs-lookup"><span data-stu-id="2526b-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="2526b-113">이 명령은 지정된 작업 영역에서 사용 가능한 모든 삭제된 sqlpool을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="2526b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2526b-114">PARAMETERS</span></span>

### <span data-ttu-id="2526b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2526b-115">-DefaultProfile</span></span>
<span data-ttu-id="2526b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2526b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2526b-117">-Name</span></span>
<span data-ttu-id="2526b-118">Synapse Sql 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2526b-119">-ResourceId</span></span>
<span data-ttu-id="2526b-120">삭제된 Sql Pool 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2526b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2526b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2526b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2526b-123">-WorkspaceName</span></span>
<span data-ttu-id="2526b-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2526b-125">CommonParameters</span></span>
<span data-ttu-id="2526b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2526b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2526b-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2526b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2526b-128">입력</span><span class="sxs-lookup"><span data-stu-id="2526b-128">INPUTS</span></span>

### <span data-ttu-id="2526b-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2526b-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2526b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2526b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="2526b-131">출력</span><span class="sxs-lookup"><span data-stu-id="2526b-131">OUTPUTS</span></span>

### <span data-ttu-id="2526b-132">Microsoft.Azure.Commands.Synapse.Models.PSDRoppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="2526b-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="2526b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2526b-133">NOTES</span></span>

## <span data-ttu-id="2526b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2526b-134">RELATED LINKS</span></span>
