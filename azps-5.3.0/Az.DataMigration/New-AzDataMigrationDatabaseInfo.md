---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387570"
---
# <span data-ttu-id="ed2b2-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ed2b2-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="ed2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2b2-103">마이그레이션을 위한 데이터베이스 원본을 지정하는 Azure Database Migration Service에 대한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="ed2b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed2b2-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed2b2-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2b2-106">New-AzDataMigrationDatabaseInfo cmdlet은 마이그레이션할 원본 데이터베이스 인스턴스를 지정하는 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="ed2b2-107">데이터베이스 이름은 입력 매개 변수로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="ed2b2-108">예제</span><span class="sxs-lookup"><span data-stu-id="ed2b2-108">EXAMPLES</span></span>

### <span data-ttu-id="ed2b2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed2b2-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="ed2b2-110">앞의 예제에서는 원본 데이터베이스 **AdventureWorks2016에** 대한 새 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="ed2b2-111">이 스크립트는 Azure 계정에 이미 로그인되어 있는 것으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="ed2b2-112">Get-AzSubscription cmdlet을 사용하여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="ed2b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed2b2-113">PARAMETERS</span></span>

### <span data-ttu-id="ed2b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2b2-114">-DefaultProfile</span></span>
<span data-ttu-id="ed2b2-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2b2-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed2b2-116">-SourceDatabaseName</span></span>
<span data-ttu-id="ed2b2-117">원본 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-117">Source Database Name.</span></span>

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

### <span data-ttu-id="ed2b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2b2-118">CommonParameters</span></span>
<span data-ttu-id="ed2b2-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2b2-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed2b2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2b2-121">입력</span><span class="sxs-lookup"><span data-stu-id="ed2b2-121">INPUTS</span></span>

### <span data-ttu-id="ed2b2-122">없음</span><span class="sxs-lookup"><span data-stu-id="ed2b2-122">None</span></span>

## <span data-ttu-id="ed2b2-123">출력</span><span class="sxs-lookup"><span data-stu-id="ed2b2-123">OUTPUTS</span></span>

### <span data-ttu-id="ed2b2-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ed2b2-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="ed2b2-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed2b2-125">NOTES</span></span>

## <span data-ttu-id="ed2b2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed2b2-126">RELATED LINKS</span></span>
