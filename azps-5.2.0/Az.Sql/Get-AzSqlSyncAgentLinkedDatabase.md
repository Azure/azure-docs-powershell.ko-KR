---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352305"
---
# <span data-ttu-id="f2699-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="f2699-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="f2699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2699-102">SYNOPSIS</span></span>
<span data-ttu-id="f2699-103">동기화 에이전트에서 SQL Server 데이터베이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="f2699-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2699-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2699-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2699-105">DESCRIPTION</span></span>
<span data-ttu-id="f2699-106">**Get-AzSqlSyncAgentLinkedDatabase** cmdlet은 동기화 에이전트에서 연결된 SQL Server 데이터베이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="f2699-107">예제</span><span class="sxs-lookup"><span data-stu-id="f2699-107">EXAMPLES</span></span>

### <span data-ttu-id="f2699-108">예제 1: Azure SQL Server 동기화 에이전트에 대한 연결된 SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="f2699-109">다음 예제에서는 Azure SQL Server 동기화 에이전트에서 연결된 연결된 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="f2699-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2699-110">PARAMETERS</span></span>

### <span data-ttu-id="f2699-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2699-111">-DefaultProfile</span></span>
<span data-ttu-id="f2699-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2699-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2699-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2699-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2699-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2699-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2699-115">-ServerName</span></span>
<span data-ttu-id="f2699-116">동기화 에이전트가 SQL Server Azure 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f2699-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f2699-117">-SyncAgentName</span></span>
<span data-ttu-id="f2699-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-118">The sync agent name.</span></span>

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

### <span data-ttu-id="f2699-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2699-119">CommonParameters</span></span>
<span data-ttu-id="f2699-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2699-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2699-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2699-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2699-122">입력</span><span class="sxs-lookup"><span data-stu-id="f2699-122">INPUTS</span></span>

### <span data-ttu-id="f2699-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f2699-123">System.String</span></span>

## <span data-ttu-id="f2699-124">출력</span><span class="sxs-lookup"><span data-stu-id="f2699-124">OUTPUTS</span></span>

### <span data-ttu-id="f2699-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f2699-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="f2699-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2699-126">NOTES</span></span>

## <span data-ttu-id="f2699-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2699-127">RELATED LINKS</span></span>
