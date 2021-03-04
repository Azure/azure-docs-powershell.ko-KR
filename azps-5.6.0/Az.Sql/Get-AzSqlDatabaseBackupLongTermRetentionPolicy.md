---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b0f3f657caea0da29ecf78baff15fe0afb7008ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967520"
---
# <span data-ttu-id="49cfc-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="49cfc-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="49cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="49cfc-103">데이터베이스 장기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="49cfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="49cfc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49cfc-105">설명</span><span class="sxs-lookup"><span data-stu-id="49cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="49cfc-106">**Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 장기 보존 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="49cfc-107">이 정책은 백업 저장소 정책을 정의하는 데 사용되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="49cfc-108">예제</span><span class="sxs-lookup"><span data-stu-id="49cfc-108">EXAMPLES</span></span>

### <span data-ttu-id="49cfc-109">예제 1: 현재 버전의 장기 보존 정책 다운로드</span><span class="sxs-lookup"><span data-stu-id="49cfc-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="49cfc-110">이 명령은 Database01에 대한 장기 보존 정책의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="49cfc-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49cfc-111">PARAMETERS</span></span>

### <span data-ttu-id="49cfc-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49cfc-112">-DatabaseName</span></span>
<span data-ttu-id="49cfc-113">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="49cfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cfc-114">-DefaultProfile</span></span>
<span data-ttu-id="49cfc-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49cfc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49cfc-116">-ResourceGroupName</span></span>
<span data-ttu-id="49cfc-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="49cfc-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49cfc-118">-ServerName</span></span>
<span data-ttu-id="49cfc-119">데이터베이스가 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="49cfc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="49cfc-120">-Confirm</span></span>
<span data-ttu-id="49cfc-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49cfc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49cfc-122">-WhatIf</span></span>
<span data-ttu-id="49cfc-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49cfc-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49cfc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cfc-125">CommonParameters</span></span>
<span data-ttu-id="49cfc-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49cfc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cfc-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49cfc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cfc-128">입력</span><span class="sxs-lookup"><span data-stu-id="49cfc-128">INPUTS</span></span>

### <span data-ttu-id="49cfc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="49cfc-129">System.String</span></span>

## <span data-ttu-id="49cfc-130">출력</span><span class="sxs-lookup"><span data-stu-id="49cfc-130">OUTPUTS</span></span>

### <span data-ttu-id="49cfc-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="49cfc-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="49cfc-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49cfc-132">NOTES</span></span>

## <span data-ttu-id="49cfc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49cfc-133">RELATED LINKS</span></span>

[<span data-ttu-id="49cfc-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="49cfc-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="49cfc-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="49cfc-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="49cfc-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="49cfc-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="49cfc-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="49cfc-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)