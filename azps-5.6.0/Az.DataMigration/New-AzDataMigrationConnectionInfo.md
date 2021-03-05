---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966635"
---
# <span data-ttu-id="e5765-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e5765-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="e5765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5765-102">SYNOPSIS</span></span>
<span data-ttu-id="e5765-103">연결에 대한 서버 유형 및 이름을 지정하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="e5765-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5765-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5765-105">설명</span><span class="sxs-lookup"><span data-stu-id="e5765-105">DESCRIPTION</span></span>
<span data-ttu-id="e5765-106">New-AzDataMigrationConnectionInfo cmdlet은 연결에 대한 서버 유형을 지정하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="e5765-107">예제</span><span class="sxs-lookup"><span data-stu-id="e5765-107">EXAMPLES</span></span>

### <span data-ttu-id="e5765-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5765-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="e5765-109">위의 예제에서는 ServerType 매개 변수로 SQL 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="e5765-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5765-110">PARAMETERS</span></span>

### <span data-ttu-id="e5765-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5765-111">-DefaultProfile</span></span>
<span data-ttu-id="e5765-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5765-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="e5765-113">-ServerType</span></span>
<span data-ttu-id="e5765-114">연결할 서버 유형을 설명하는 열의입니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="e5765-115">현재 지원되는 값은 SQL 관리 SQL Server Azure SQL MongoDb, CosmosDb 및 Azure SQL 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5765-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5765-116">CommonParameters</span></span>
<span data-ttu-id="e5765-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5765-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5765-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5765-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5765-119">입력</span><span class="sxs-lookup"><span data-stu-id="e5765-119">INPUTS</span></span>

### <span data-ttu-id="e5765-120">없음</span><span class="sxs-lookup"><span data-stu-id="e5765-120">None</span></span>

## <span data-ttu-id="e5765-121">출력</span><span class="sxs-lookup"><span data-stu-id="e5765-121">OUTPUTS</span></span>

### <span data-ttu-id="e5765-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e5765-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="e5765-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5765-123">NOTES</span></span>

## <span data-ttu-id="e5765-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5765-124">RELATED LINKS</span></span>
