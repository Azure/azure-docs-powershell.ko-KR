---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188025"
---
# <span data-ttu-id="792e7-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="792e7-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="792e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792e7-102">SYNOPSIS</span></span>
<span data-ttu-id="792e7-103">장기 보존 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="792e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="792e7-104">SYNTAX</span></span>

### <span data-ttu-id="792e7-105">RemoveBackupDefault(기본값)</span><span class="sxs-lookup"><span data-stu-id="792e7-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792e7-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="792e7-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792e7-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="792e7-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="792e7-108">설명</span><span class="sxs-lookup"><span data-stu-id="792e7-108">DESCRIPTION</span></span>
<span data-ttu-id="792e7-109">**Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet은 지정된 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="792e7-110">예제</span><span class="sxs-lookup"><span data-stu-id="792e7-110">EXAMPLES</span></span>

### <span data-ttu-id="792e7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="792e7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="792e7-112">이름이 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000인 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="792e7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="792e7-113">PARAMETERS</span></span>

### <span data-ttu-id="792e7-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="792e7-114">-BackupName</span></span>
<span data-ttu-id="792e7-115">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="792e7-116">-DatabaseName</span></span>
<span data-ttu-id="792e7-117">백업이 시작된 관리되는 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792e7-118">-DefaultProfile</span></span>
<span data-ttu-id="792e7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792e7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="792e7-120">-Force</span></span>
<span data-ttu-id="792e7-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="792e7-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792e7-122">-InputObject</span></span>
<span data-ttu-id="792e7-123">제거할 데이터베이스 장기 보존 백업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="792e7-124">-InstanceName</span></span>
<span data-ttu-id="792e7-125">백업이 진행되는 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-126">-Location</span><span class="sxs-lookup"><span data-stu-id="792e7-126">-Location</span></span>
<span data-ttu-id="792e7-127">백업의 원본 Managed Instance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="792e7-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="792e7-130">-ResourceId</span></span>
<span data-ttu-id="792e7-131">제거할 데이터베이스 장기 보존 백업의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="792e7-132">-Confirm</span></span>
<span data-ttu-id="792e7-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792e7-134">-WhatIf</span></span>
<span data-ttu-id="792e7-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="792e7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792e7-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792e7-137">CommonParameters</span></span>
<span data-ttu-id="792e7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="792e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792e7-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="792e7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792e7-140">입력</span><span class="sxs-lookup"><span data-stu-id="792e7-140">INPUTS</span></span>

### <span data-ttu-id="792e7-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="792e7-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="792e7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="792e7-142">System.String</span></span>

## <span data-ttu-id="792e7-143">출력</span><span class="sxs-lookup"><span data-stu-id="792e7-143">OUTPUTS</span></span>

### <span data-ttu-id="792e7-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="792e7-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="792e7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="792e7-145">NOTES</span></span>

## <span data-ttu-id="792e7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="792e7-146">RELATED LINKS</span></span>

[<span data-ttu-id="792e7-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="792e7-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="792e7-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="792e7-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="792e7-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="792e7-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="792e7-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="792e7-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)