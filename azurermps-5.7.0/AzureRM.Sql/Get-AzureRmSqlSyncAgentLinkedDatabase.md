---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703946"
---
# <span data-ttu-id="95b78-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="95b78-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="95b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95b78-102">SYNOPSIS</span></span>
<span data-ttu-id="95b78-103">동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95b78-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95b78-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95b78-105">DESCRIPTION</span></span>
<span data-ttu-id="95b78-106">**AzureRmSqlSyncAgentLinkedDatabases** cmdlet은 동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="95b78-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95b78-107">EXAMPLES</span></span>

### <span data-ttu-id="95b78-108">예제 1: Azure SQL 동기화 에이전트에 대 한 연결 된 SQL Server 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="95b78-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="95b78-109">이 명령은 Azure SQL 동기화 에이전트로 연결 된 연결 된 SQL Server 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="95b78-110">변수</span><span class="sxs-lookup"><span data-stu-id="95b78-110">PARAMETERS</span></span>

### <span data-ttu-id="95b78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b78-111">-DefaultProfile</span></span>
<span data-ttu-id="95b78-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95b78-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b78-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95b78-113">-ResourceGroupName</span></span>
<span data-ttu-id="95b78-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b78-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="95b78-115">-ServerName</span></span>
<span data-ttu-id="95b78-116">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b78-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="95b78-117">-SyncAgentName</span></span>
<span data-ttu-id="95b78-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b78-119">CommonParameters</span></span>
<span data-ttu-id="95b78-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b78-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b78-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b78-122">입력</span><span class="sxs-lookup"><span data-stu-id="95b78-122">INPUTS</span></span>

### <span data-ttu-id="95b78-123">않아야</span><span class="sxs-lookup"><span data-stu-id="95b78-123">None</span></span>
<span data-ttu-id="95b78-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95b78-125">출력</span><span class="sxs-lookup"><span data-stu-id="95b78-125">OUTPUTS</span></span>

### <span data-ttu-id="95b78-126">AzureSqlSyncAgentLinkedDatabaseModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b78-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="95b78-127">상속자</span><span class="sxs-lookup"><span data-stu-id="95b78-127">NOTES</span></span>

## <span data-ttu-id="95b78-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95b78-128">RELATED LINKS</span></span>
