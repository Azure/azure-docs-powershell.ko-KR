---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b27aee4c665dd2725bfd8643cb12ca005a5c4e1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014496"
---
# <span data-ttu-id="9e2ed-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="9e2ed-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="9e2ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2ed-103">동기화 에이전트에 SQL Server 데이터베이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="9e2ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e2ed-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2ed-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e2ed-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2ed-106">**Get-AzSqlSyncAgentLinkedDatabase** cmdlet은 동기화 에이전트에 SQL Server 데이터베이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="9e2ed-107">예제</span><span class="sxs-lookup"><span data-stu-id="9e2ed-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2ed-108">예제 1: Azure SQL Server 동기화 에이전트에 대한 연결된 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="9e2ed-109">다음 예제에서는 Azure SQL Server 동기화 에이전트에 의해 연결된 연결된 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="9e2ed-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e2ed-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2ed-111">-DefaultProfile</span></span>
<span data-ttu-id="9e2ed-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e2ed-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e2ed-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2ed-113">-ResourceGroupName</span></span>
<span data-ttu-id="9e2ed-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ed-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e2ed-115">-ServerName</span></span>
<span data-ttu-id="9e2ed-116">동기화 에이전트가 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ed-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="9e2ed-117">-SyncAgentName</span></span>
<span data-ttu-id="9e2ed-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2ed-119">CommonParameters</span></span>
<span data-ttu-id="9e2ed-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2ed-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e2ed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2ed-122">입력</span><span class="sxs-lookup"><span data-stu-id="9e2ed-122">INPUTS</span></span>

### <span data-ttu-id="9e2ed-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9e2ed-123">System.String</span></span>

## <span data-ttu-id="9e2ed-124">출력</span><span class="sxs-lookup"><span data-stu-id="9e2ed-124">OUTPUTS</span></span>

### <span data-ttu-id="9e2ed-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9e2ed-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="9e2ed-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e2ed-126">NOTES</span></span>

## <span data-ttu-id="9e2ed-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e2ed-127">RELATED LINKS</span></span>
