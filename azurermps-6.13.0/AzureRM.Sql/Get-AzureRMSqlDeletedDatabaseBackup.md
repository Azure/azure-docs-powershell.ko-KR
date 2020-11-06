---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2373a076e6edd97314e08c9170f9584a904ad902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529356"
---
# <span data-ttu-id="26852-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="26852-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="26852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26852-102">SYNOPSIS</span></span>
<span data-ttu-id="26852-103">복원할 수 있는 삭제 된 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26852-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26852-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26852-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26852-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26852-105">DESCRIPTION</span></span>
<span data-ttu-id="26852-106">**AzureRMSqlDeletedDatabaseBackup** cmdlet은 복원할 수 있는 지정한 삭제 된 SQL 데이터베이스 백업을 만들거나, 모든 삭제 된 백업을 복원할 수 있도록 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26852-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="26852-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26852-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="26852-108">예제의</span><span class="sxs-lookup"><span data-stu-id="26852-108">EXAMPLES</span></span>

### <span data-ttu-id="26852-109">예제 1: 서버에서 삭제 된 모든 데이터베이스 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="26852-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="26852-110">이 명령은 서버에서 삭제 된 모든 데이터베이스 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26852-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="26852-111">예제 2: 지정한 삭제 된 데이터베이스 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="26852-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="26852-112">이 명령은 ContosoDatabase에 대 한 삭제 된 데이터베이스 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26852-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="26852-113">변수</span><span class="sxs-lookup"><span data-stu-id="26852-113">PARAMETERS</span></span>

### <span data-ttu-id="26852-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26852-114">-DatabaseName</span></span>
<span data-ttu-id="26852-115">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26852-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26852-116">-DefaultProfile</span></span>
<span data-ttu-id="26852-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26852-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26852-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="26852-118">-DeletionDate</span></span>
<span data-ttu-id="26852-119">데이터베이스가 삭제 된 날짜를 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="26852-120">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26852-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26852-121">-ResourceGroupName</span></span>
<span data-ttu-id="26852-122">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="26852-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26852-123">-ServerName</span></span>
<span data-ttu-id="26852-124">데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="26852-125">-확인</span><span class="sxs-lookup"><span data-stu-id="26852-125">-Confirm</span></span>
<span data-ttu-id="26852-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26852-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26852-127">-WhatIf</span></span>
<span data-ttu-id="26852-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26852-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26852-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26852-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26852-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26852-130">CommonParameters</span></span>
<span data-ttu-id="26852-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26852-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26852-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26852-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26852-133">입력</span><span class="sxs-lookup"><span data-stu-id="26852-133">INPUTS</span></span>

### <span data-ttu-id="26852-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26852-134">System.String</span></span>

### <span data-ttu-id="26852-135">시스템 Null 허용 ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26852-135">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="26852-136">출력</span><span class="sxs-lookup"><span data-stu-id="26852-136">OUTPUTS</span></span>

### <span data-ttu-id="26852-137">AzureSqlDeletedDatabaseBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="26852-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="26852-138">상속자</span><span class="sxs-lookup"><span data-stu-id="26852-138">NOTES</span></span>

## <span data-ttu-id="26852-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26852-139">RELATED LINKS</span></span>

[<span data-ttu-id="26852-140">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26852-140">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="26852-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="26852-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
