---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957867"
---
# <span data-ttu-id="3cc37-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="3cc37-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="3cc37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc37-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc37-103">Sql Pool의 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="3cc37-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cc37-104">SYNTAX</span></span>

### <span data-ttu-id="3cc37-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3cc37-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cc37-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc37-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cc37-107">설명</span><span class="sxs-lookup"><span data-stu-id="3cc37-107">DESCRIPTION</span></span>
<span data-ttu-id="3cc37-108">**Get-AzSynapseSqlPoolGeoBackup** cmdlet은 지정된 작업 영역의 SQL 풀 또는 사용 가능한 모든 지역 중복 백업의 지정된 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="3cc37-109">지역 중복 백업은 별도의 지리적 위치에서 데이터 파일을 사용하여 복원 가능한 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="3cc37-110">새 지역으로 Geo-Restore 지역 정전이 발생하면 지역 중복 백업을 복원하여 Sql Pool을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="3cc37-111">예제</span><span class="sxs-lookup"><span data-stu-id="3cc37-111">EXAMPLES</span></span>

### <span data-ttu-id="3cc37-112">예제 1: 지정된 지역 중복 백업을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="3cc37-113">cmdlet은 SQL 풀에 대한 지역 백업을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="3cc37-114">예제 2: 작업 영역의 모든 지역 중복 백업 사용</span><span class="sxs-lookup"><span data-stu-id="3cc37-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="3cc37-115">이 명령은 지정된 작업 영역의 사용 가능한 모든 지역 중복 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="3cc37-116">예제 3: 필터링을 사용하여 작업 영역의 모든 지역 중복 백업 사용</span><span class="sxs-lookup"><span data-stu-id="3cc37-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="3cc37-117">이 명령은 "Contoso"로 시작하는 지정된 작업 영역의 사용 가능한 모든 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="3cc37-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3cc37-118">PARAMETERS</span></span>

### <span data-ttu-id="3cc37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc37-119">-DefaultProfile</span></span>
<span data-ttu-id="3cc37-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc37-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3cc37-121">-Name</span></span>
<span data-ttu-id="3cc37-122">Synapse Sql 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc37-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc37-123">-ResourceId</span></span>
<span data-ttu-id="3cc37-124">Sql Pool 지역 백업 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc37-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cc37-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-126">Resource group name.</span></span>

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

### <span data-ttu-id="3cc37-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cc37-127">-WorkspaceName</span></span>
<span data-ttu-id="3cc37-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cc37-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc37-129">CommonParameters</span></span>
<span data-ttu-id="3cc37-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc37-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc37-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cc37-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc37-132">입력</span><span class="sxs-lookup"><span data-stu-id="3cc37-132">INPUTS</span></span>

### <span data-ttu-id="3cc37-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cc37-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3cc37-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3cc37-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="3cc37-135">출력</span><span class="sxs-lookup"><span data-stu-id="3cc37-135">OUTPUTS</span></span>

### <span data-ttu-id="3cc37-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="3cc37-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="3cc37-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cc37-137">NOTES</span></span>

## <span data-ttu-id="3cc37-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cc37-138">RELATED LINKS</span></span>
