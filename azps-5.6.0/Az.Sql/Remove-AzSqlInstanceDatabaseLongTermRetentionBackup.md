---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: d3faa342d1f54abe2433ec7de8ee1c3f910fa58d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967467"
---
# <span data-ttu-id="7af14-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7af14-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="7af14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7af14-102">SYNOPSIS</span></span>
<span data-ttu-id="7af14-103">장기 보존 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="7af14-104">구문</span><span class="sxs-lookup"><span data-stu-id="7af14-104">SYNTAX</span></span>

### <span data-ttu-id="7af14-105">RemoveBackupDefault(기본값)</span><span class="sxs-lookup"><span data-stu-id="7af14-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af14-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="7af14-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af14-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="7af14-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7af14-108">설명</span><span class="sxs-lookup"><span data-stu-id="7af14-108">DESCRIPTION</span></span>
<span data-ttu-id="7af14-109">**Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet은 지정된 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="7af14-110">예제</span><span class="sxs-lookup"><span data-stu-id="7af14-110">EXAMPLES</span></span>

### <span data-ttu-id="7af14-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7af14-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="7af14-112">이름 15be823c-7e2c-49d8-819f-a3fdcad92215;13226825050000000000</span><span class="sxs-lookup"><span data-stu-id="7af14-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="7af14-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7af14-113">PARAMETERS</span></span>

### <span data-ttu-id="7af14-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="7af14-114">-BackupName</span></span>
<span data-ttu-id="7af14-115">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-115">The name of the backup.</span></span>

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

### <span data-ttu-id="7af14-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7af14-116">-DatabaseName</span></span>
<span data-ttu-id="7af14-117">백업이 시작된 관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="7af14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af14-118">-DefaultProfile</span></span>
<span data-ttu-id="7af14-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7af14-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7af14-120">-Force</span></span>
<span data-ttu-id="7af14-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="7af14-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7af14-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7af14-122">-InputObject</span></span>
<span data-ttu-id="7af14-123">제거할 데이터베이스 장기 보존 백업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-123">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="7af14-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7af14-124">-InstanceName</span></span>
<span data-ttu-id="7af14-125">백업이 있는 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="7af14-126">-Location</span><span class="sxs-lookup"><span data-stu-id="7af14-126">-Location</span></span>
<span data-ttu-id="7af14-127">백업의 원본 Managed Instance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="7af14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af14-128">-ResourceGroupName</span></span>
<span data-ttu-id="7af14-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7af14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af14-130">-ResourceId</span></span>
<span data-ttu-id="7af14-131">제거할 데이터베이스 장기 보존 백업의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="7af14-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7af14-132">-Confirm</span></span>
<span data-ttu-id="7af14-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7af14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af14-134">-WhatIf</span></span>
<span data-ttu-id="7af14-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7af14-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7af14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af14-137">CommonParameters</span></span>
<span data-ttu-id="7af14-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7af14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af14-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7af14-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af14-140">입력</span><span class="sxs-lookup"><span data-stu-id="7af14-140">INPUTS</span></span>

### <span data-ttu-id="7af14-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="7af14-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="7af14-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7af14-142">System.String</span></span>

## <span data-ttu-id="7af14-143">출력</span><span class="sxs-lookup"><span data-stu-id="7af14-143">OUTPUTS</span></span>

### <span data-ttu-id="7af14-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="7af14-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="7af14-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7af14-145">NOTES</span></span>

## <span data-ttu-id="7af14-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7af14-146">RELATED LINKS</span></span>

[<span data-ttu-id="7af14-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7af14-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7af14-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af14-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7af14-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af14-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7af14-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7af14-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)