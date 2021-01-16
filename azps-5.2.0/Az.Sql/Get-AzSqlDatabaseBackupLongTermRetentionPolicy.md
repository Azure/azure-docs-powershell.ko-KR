---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368558"
---
# <span data-ttu-id="e2f0d-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2f0d-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="e2f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f0d-103">데이터베이스 장기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="e2f0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2f0d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2f0d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="e2f0d-106">**Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 장기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="e2f0d-107">정책은 백업 저장소 정책을 정의하는 데 사용되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="e2f0d-108">예제</span><span class="sxs-lookup"><span data-stu-id="e2f0d-108">EXAMPLES</span></span>

### <span data-ttu-id="e2f0d-109">예제 1: 현재 버전의 장기 보존 정책 다운로드</span><span class="sxs-lookup"><span data-stu-id="e2f0d-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="e2f0d-110">이 명령은 database01에 대한 장기 보존 정책의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="e2f0d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2f0d-111">PARAMETERS</span></span>

### <span data-ttu-id="e2f0d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2f0d-112">-DatabaseName</span></span>
<span data-ttu-id="e2f0d-113">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-113">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f0d-114">-DefaultProfile</span></span>
<span data-ttu-id="e2f0d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f0d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f0d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e2f0d-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2f0d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2f0d-118">-ServerName</span></span>
<span data-ttu-id="e2f0d-119">데이터베이스가 있는 azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="e2f0d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f0d-120">-Confirm</span></span>
<span data-ttu-id="e2f0d-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f0d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f0d-122">-WhatIf</span></span>
<span data-ttu-id="e2f0d-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2f0d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f0d-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f0d-125">CommonParameters</span></span>
<span data-ttu-id="e2f0d-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f0d-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f0d-128">입력</span><span class="sxs-lookup"><span data-stu-id="e2f0d-128">INPUTS</span></span>

### <span data-ttu-id="e2f0d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e2f0d-129">System.String</span></span>

## <span data-ttu-id="e2f0d-130">출력</span><span class="sxs-lookup"><span data-stu-id="e2f0d-130">OUTPUTS</span></span>

### <span data-ttu-id="e2f0d-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e2f0d-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="e2f0d-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2f0d-132">NOTES</span></span>

## <span data-ttu-id="e2f0d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2f0d-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2f0d-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e2f0d-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e2f0d-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e2f0d-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e2f0d-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2f0d-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e2f0d-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e2f0d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)