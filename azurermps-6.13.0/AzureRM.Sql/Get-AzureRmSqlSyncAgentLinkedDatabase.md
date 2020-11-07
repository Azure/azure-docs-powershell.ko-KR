---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 11c444e92c6377e0a0df5aaa324ee162647784a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704107"
---
# <span data-ttu-id="892a3-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="892a3-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="892a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="892a3-102">SYNOPSIS</span></span>
<span data-ttu-id="892a3-103">동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="892a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="892a3-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="892a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="892a3-105">DESCRIPTION</span></span>
<span data-ttu-id="892a3-106">**AzureRmSqlSyncAgentLinkedDatabases** cmdlet은 동기화 에이전트로 연결 된 SQL Server 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="892a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="892a3-107">EXAMPLES</span></span>

### <span data-ttu-id="892a3-108">예제 1: Azure SQL 동기화 에이전트에 대 한 연결 된 SQL Server 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="892a3-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="892a3-109">이 명령은 Azure SQL 동기화 에이전트로 연결 된 연결 된 SQL Server 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="892a3-110">변수</span><span class="sxs-lookup"><span data-stu-id="892a3-110">PARAMETERS</span></span>

### <span data-ttu-id="892a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892a3-111">-DefaultProfile</span></span>
<span data-ttu-id="892a3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="892a3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="892a3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892a3-113">-ResourceGroupName</span></span>
<span data-ttu-id="892a3-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="892a3-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="892a3-115">-ServerName</span></span>
<span data-ttu-id="892a3-116">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="892a3-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="892a3-117">-SyncAgentName</span></span>
<span data-ttu-id="892a3-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-118">The sync agent name.</span></span>

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

### <span data-ttu-id="892a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892a3-119">CommonParameters</span></span>
<span data-ttu-id="892a3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892a3-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892a3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892a3-122">입력</span><span class="sxs-lookup"><span data-stu-id="892a3-122">INPUTS</span></span>

### <span data-ttu-id="892a3-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="892a3-123">System.String</span></span>

## <span data-ttu-id="892a3-124">출력</span><span class="sxs-lookup"><span data-stu-id="892a3-124">OUTPUTS</span></span>

### <span data-ttu-id="892a3-125">AzureSqlSyncAgentLinkedDatabaseModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="892a3-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="892a3-126">상속자</span><span class="sxs-lookup"><span data-stu-id="892a3-126">NOTES</span></span>

## <span data-ttu-id="892a3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="892a3-127">RELATED LINKS</span></span>
