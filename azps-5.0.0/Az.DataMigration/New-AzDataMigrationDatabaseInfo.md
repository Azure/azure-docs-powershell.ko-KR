---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305408"
---
# <span data-ttu-id="81d62-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="81d62-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="81d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d62-102">SYNOPSIS</span></span>
<span data-ttu-id="81d62-103">마이그레이션에 대 한 데이터베이스 원본을 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="81d62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81d62-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81d62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="81d62-105">DESCRIPTION</span></span>
<span data-ttu-id="81d62-106">New-AzDataMigrationDatabaseInfo cmdlet은 마이그레이션할 원본 데이터베이스 인스턴스를 지정 하는 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="81d62-107">데이터베이스 이름을 입력 매개 변수로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="81d62-108">예제의</span><span class="sxs-lookup"><span data-stu-id="81d62-108">EXAMPLES</span></span>

### <span data-ttu-id="81d62-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="81d62-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="81d62-110">앞의 예제에서는 원본 데이터베이스 **AdventureWorks2016** 에 대 한 새 databaseinfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="81d62-111">이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="81d62-112">Get-AzSubscription cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="81d62-113">변수</span><span class="sxs-lookup"><span data-stu-id="81d62-113">PARAMETERS</span></span>

### <span data-ttu-id="81d62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d62-114">-DefaultProfile</span></span>
<span data-ttu-id="81d62-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d62-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="81d62-116">-SourceDatabaseName</span></span>
<span data-ttu-id="81d62-117">원본 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="81d62-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d62-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d62-118">CommonParameters</span></span>
<span data-ttu-id="81d62-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d62-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d62-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d62-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d62-121">입력</span><span class="sxs-lookup"><span data-stu-id="81d62-121">INPUTS</span></span>

### <span data-ttu-id="81d62-122">않아야</span><span class="sxs-lookup"><span data-stu-id="81d62-122">None</span></span>

## <span data-ttu-id="81d62-123">출력</span><span class="sxs-lookup"><span data-stu-id="81d62-123">OUTPUTS</span></span>

### <span data-ttu-id="81d62-124">DataMigration Info (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81d62-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="81d62-125">상속자</span><span class="sxs-lookup"><span data-stu-id="81d62-125">NOTES</span></span>

## <span data-ttu-id="81d62-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81d62-126">RELATED LINKS</span></span>
