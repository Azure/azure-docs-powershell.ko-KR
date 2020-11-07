---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702890"
---
# <span data-ttu-id="415c0-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="415c0-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="415c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="415c0-102">SYNOPSIS</span></span>
<span data-ttu-id="415c0-103">데이터베이스 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="415c0-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="415c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="415c0-105">DESCRIPTION</span></span>
<span data-ttu-id="415c0-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="415c0-107">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="415c0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="415c0-108">EXAMPLES</span></span>

### <span data-ttu-id="415c0-109">예제 1: 장기 보존 정책의 현재 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="415c0-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="415c0-110">이 명령은 database01에 대 한 장기 보존 정책의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="415c0-111">예제 2: 이전 버전의 장기 보존 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="415c0-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="415c0-112">이 명령은 database01의 장기 보존 정책의 레거시 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="415c0-113">변수</span><span class="sxs-lookup"><span data-stu-id="415c0-113">PARAMETERS</span></span>

### <span data-ttu-id="415c0-114">-현재</span><span class="sxs-lookup"><span data-stu-id="415c0-114">-Current</span></span>
<span data-ttu-id="415c0-115">지정 하지 않으면 명령이 레거시 장기 보존 정책 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="415c0-116">그렇지 않으면 명령이 장기 보존 정책의 현재 버전을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415c0-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="415c0-117">-DatabaseName</span></span>
<span data-ttu-id="415c0-118">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="415c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415c0-119">-DefaultProfile</span></span>
<span data-ttu-id="415c0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="415c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="415c0-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="415c0-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="415c0-123">-ServerName</span></span>
<span data-ttu-id="415c0-124">데이터베이스가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="415c0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="415c0-125">-Confirm</span></span>
<span data-ttu-id="415c0-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415c0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415c0-127">-WhatIf</span></span>
<span data-ttu-id="415c0-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415c0-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415c0-130">CommonParameters</span></span>
<span data-ttu-id="415c0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="415c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415c0-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415c0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415c0-133">입력</span><span class="sxs-lookup"><span data-stu-id="415c0-133">INPUTS</span></span>

### <span data-ttu-id="415c0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="415c0-134">System.String</span></span>

## <span data-ttu-id="415c0-135">출력</span><span class="sxs-lookup"><span data-stu-id="415c0-135">OUTPUTS</span></span>

### <span data-ttu-id="415c0-136">AzureSqlDatabaseBackupLongTermRetentionPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="415c0-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="415c0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="415c0-137">NOTES</span></span>

## <span data-ttu-id="415c0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="415c0-138">RELATED LINKS</span></span>

[<span data-ttu-id="415c0-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="415c0-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="415c0-140">제거-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="415c0-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="415c0-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="415c0-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="415c0-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="415c0-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
