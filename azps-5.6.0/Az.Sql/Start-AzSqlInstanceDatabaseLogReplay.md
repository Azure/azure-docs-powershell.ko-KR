---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: ce937cc6f7e4bc68592ed089a3028e2919fde29f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963584"
---
# <span data-ttu-id="23ffb-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="23ffb-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="23ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="23ffb-103">주어진 매개 변수를 사용하여 Log Replay 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="23ffb-104">구문</span><span class="sxs-lookup"><span data-stu-id="23ffb-104">SYNTAX</span></span>

### <span data-ttu-id="23ffb-105">LogReplayInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="23ffb-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ffb-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="23ffb-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23ffb-107">설명</span><span class="sxs-lookup"><span data-stu-id="23ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="23ffb-108">**Start-AzSqlInstanceDatabaseLogReplay** cmdlet은 로그 재생 서비스의 시작을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="23ffb-109">예제</span><span class="sxs-lookup"><span data-stu-id="23ffb-109">EXAMPLES</span></span>

### <span data-ttu-id="23ffb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="23ffb-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="23ffb-111">이 명령은 새 관리되는 데이터베이스를 만들고, last_backup.bak가 복원될 때까지 해당 컨테이너에서 백업을 복원하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="23ffb-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="23ffb-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="23ffb-113">이 명령은 새 관리되는 데이터베이스를 만들고 마지막 백업이 원하는 마지막 백업으로 호출될 때까지 Complete-AzSqlInstanceDatabaseLogReplay 컨테이너에서 백업을 복원하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="23ffb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="23ffb-114">PARAMETERS</span></span>

### <span data-ttu-id="23ffb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23ffb-115">-AsJob</span></span>
<span data-ttu-id="23ffb-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="23ffb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23ffb-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="23ffb-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="23ffb-118">완료 시 복원을 자동으로 완료할지 여부를 나타내는 표시기입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="23ffb-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="23ffb-119">-Collation</span></span>
<span data-ttu-id="23ffb-120">사용할 인스턴스 데이터베이스의 데이터 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ffb-121">-DefaultProfile</span></span>
<span data-ttu-id="23ffb-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ffb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23ffb-123">-InputObject</span></span>
<span data-ttu-id="23ffb-124">인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23ffb-125">-InstanceName</span></span>
<span data-ttu-id="23ffb-126">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="23ffb-127">-LastBackupName</span></span>
<span data-ttu-id="23ffb-128">복원할 마지막 백업 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="23ffb-129">-Name</span></span>
<span data-ttu-id="23ffb-130">인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23ffb-131">-PassThru</span></span>
<span data-ttu-id="23ffb-132">동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="23ffb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ffb-133">-ResourceGroupName</span></span>
<span data-ttu-id="23ffb-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="23ffb-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="23ffb-136">저장소 컨테이너 Sas 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="23ffb-137">-StorageContainerUri</span></span>
<span data-ttu-id="23ffb-138">저장소 컨테이너 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ffb-139">-확인</span><span class="sxs-lookup"><span data-stu-id="23ffb-139">-Confirm</span></span>
<span data-ttu-id="23ffb-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ffb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ffb-141">-WhatIf</span></span>
<span data-ttu-id="23ffb-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23ffb-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ffb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ffb-144">CommonParameters</span></span>
<span data-ttu-id="23ffb-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23ffb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ffb-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23ffb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ffb-147">입력</span><span class="sxs-lookup"><span data-stu-id="23ffb-147">INPUTS</span></span>

### <span data-ttu-id="23ffb-148">System.String</span><span class="sxs-lookup"><span data-stu-id="23ffb-148">System.String</span></span>

### <span data-ttu-id="23ffb-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23ffb-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="23ffb-150">출력</span><span class="sxs-lookup"><span data-stu-id="23ffb-150">OUTPUTS</span></span>

### <span data-ttu-id="23ffb-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23ffb-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="23ffb-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23ffb-152">NOTES</span></span>

## <span data-ttu-id="23ffb-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23ffb-153">RELATED LINKS</span></span>
