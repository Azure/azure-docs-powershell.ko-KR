---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711177"
---
# <span data-ttu-id="27db3-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="27db3-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="27db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27db3-102">SYNOPSIS</span></span>
<span data-ttu-id="27db3-103">마이그레이션에 대 한 데이터베이스 원본을 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27db3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27db3-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="27db3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27db3-105">DESCRIPTION</span></span>
<span data-ttu-id="27db3-106">New-AzureRmDataMigrationDatabaseInfo cmdlet은 마이그레이션할 원본 데이터베이스 인스턴스를 지정 하는 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="27db3-107">데이터베이스 이름을 입력 매개 변수로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="27db3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="27db3-108">EXAMPLES</span></span>

### <span data-ttu-id="27db3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="27db3-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="27db3-110">앞의 예제에서는 원본 데이터베이스 **AdventureWorks2016** 에 대 한 새 databaseinfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="27db3-111">이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="27db3-112">Get-AzureSubscription cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="27db3-113">변수</span><span class="sxs-lookup"><span data-stu-id="27db3-113">PARAMETERS</span></span>

### <span data-ttu-id="27db3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27db3-114">-DefaultProfile</span></span>
<span data-ttu-id="27db3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="27db3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="27db3-116">-Confirm</span></span>
<span data-ttu-id="27db3-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27db3-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="27db3-118">-SourceDatabaseName</span></span>
<span data-ttu-id="27db3-119">원본 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="27db3-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27db3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27db3-120">-WhatIf</span></span>
<span data-ttu-id="27db3-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27db3-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27db3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="27db3-123">입력</span><span class="sxs-lookup"><span data-stu-id="27db3-123">INPUTS</span></span>

### <span data-ttu-id="27db3-124">않아야</span><span class="sxs-lookup"><span data-stu-id="27db3-124">None</span></span>


## <span data-ttu-id="27db3-125">출력</span><span class="sxs-lookup"><span data-stu-id="27db3-125">OUTPUTS</span></span>

### <span data-ttu-id="27db3-126">DataMigration Info (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27db3-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="27db3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="27db3-127">NOTES</span></span>

## <span data-ttu-id="27db3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27db3-128">RELATED LINKS</span></span>


