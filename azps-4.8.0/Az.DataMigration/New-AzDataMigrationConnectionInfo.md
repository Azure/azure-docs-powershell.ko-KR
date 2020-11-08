---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212286"
---
# <span data-ttu-id="5b51b-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="5b51b-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="5b51b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b51b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b51b-103">연결에 대 한 서버 유형 및 이름을 지정 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="5b51b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b51b-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b51b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b51b-105">DESCRIPTION</span></span>
<span data-ttu-id="5b51b-106">New-AzDataMigrationConnectionInfo cmdlet은 연결에 대 한 서버 유형을 지정 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="5b51b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b51b-107">EXAMPLES</span></span>

### <span data-ttu-id="5b51b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b51b-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="5b51b-109">앞의 예제에서는 ServerType 매개 변수로 SQL을 제공 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="5b51b-110">변수</span><span class="sxs-lookup"><span data-stu-id="5b51b-110">PARAMETERS</span></span>

### <span data-ttu-id="5b51b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b51b-111">-DefaultProfile</span></span>
<span data-ttu-id="5b51b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b51b-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="5b51b-113">-ServerType</span></span>
<span data-ttu-id="5b51b-114">연결할 서버 유형을 설명 하는 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="5b51b-115">현재 지원 되는 값은 SQL Server, Azure SQL 관리 인스턴스, MongoDb, CosmosDb 및 Azure SQL 데이터베이스에 대 한 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="5b51b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b51b-116">CommonParameters</span></span>
<span data-ttu-id="5b51b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b51b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b51b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b51b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b51b-119">입력</span><span class="sxs-lookup"><span data-stu-id="5b51b-119">INPUTS</span></span>

### <span data-ttu-id="5b51b-120">않아야</span><span class="sxs-lookup"><span data-stu-id="5b51b-120">None</span></span>

## <span data-ttu-id="5b51b-121">출력</span><span class="sxs-lookup"><span data-stu-id="5b51b-121">OUTPUTS</span></span>

### <span data-ttu-id="5b51b-122">DataMigration. ConnectionInfo/.</span><span class="sxs-lookup"><span data-stu-id="5b51b-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="5b51b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="5b51b-123">NOTES</span></span>

## <span data-ttu-id="5b51b-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b51b-124">RELATED LINKS</span></span>
