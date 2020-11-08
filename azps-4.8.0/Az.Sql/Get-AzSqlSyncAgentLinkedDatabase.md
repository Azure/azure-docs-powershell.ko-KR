---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213230"
---
# <span data-ttu-id="b135a-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="b135a-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="b135a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b135a-102">SYNOPSIS</span></span>
<span data-ttu-id="b135a-103">동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="b135a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b135a-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b135a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b135a-105">DESCRIPTION</span></span>
<span data-ttu-id="b135a-106">**AzSqlSyncAgentLinkedDatabase** cmdlet은 동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="b135a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b135a-107">EXAMPLES</span></span>

### <span data-ttu-id="b135a-108">예제 1: Azure SQL 동기화 에이전트에 대 한 연결 된 SQL Server 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b135a-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="b135a-109">다음 예에서는 Azure SQL 동기화 에이전트로 연결 된 연결 된 SQL Server 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="b135a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b135a-110">PARAMETERS</span></span>

### <span data-ttu-id="b135a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b135a-111">-DefaultProfile</span></span>
<span data-ttu-id="b135a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b135a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b135a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b135a-113">-ResourceGroupName</span></span>
<span data-ttu-id="b135a-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b135a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b135a-115">-ServerName</span></span>
<span data-ttu-id="b135a-116">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b135a-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="b135a-117">-SyncAgentName</span></span>
<span data-ttu-id="b135a-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-118">The sync agent name.</span></span>

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

### <span data-ttu-id="b135a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b135a-119">CommonParameters</span></span>
<span data-ttu-id="b135a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b135a-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b135a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b135a-122">입력</span><span class="sxs-lookup"><span data-stu-id="b135a-122">INPUTS</span></span>

### <span data-ttu-id="b135a-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b135a-123">System.String</span></span>

## <span data-ttu-id="b135a-124">출력</span><span class="sxs-lookup"><span data-stu-id="b135a-124">OUTPUTS</span></span>

### <span data-ttu-id="b135a-125">AzureSqlSyncAgentLinkedDatabaseModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="b135a-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="b135a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b135a-126">NOTES</span></span>

## <span data-ttu-id="b135a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b135a-127">RELATED LINKS</span></span>
