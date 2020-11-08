---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213222"
---
# <span data-ttu-id="e898f-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e898f-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e898f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e898f-102">SYNOPSIS</span></span>
<span data-ttu-id="e898f-103">주어진 매개 변수를 사용 하 여 로그 재생 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="e898f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e898f-104">SYNTAX</span></span>

### <span data-ttu-id="e898f-105">Logreplayinstancedatabase Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="e898f-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e898f-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e898f-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e898f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e898f-107">DESCRIPTION</span></span>
<span data-ttu-id="e898f-108">**AzSqlInstanceDatabaseLogReplay** cmdlet이 로그 재생 서비스의 시작을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="e898f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e898f-109">EXAMPLES</span></span>

### <span data-ttu-id="e898f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e898f-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="e898f-111">이 명령은 새 관리 데이터베이스를 만들고 last_backup .bak가 복원 될 때까지 지정 된 컨테이너에서 백업을 복원 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="e898f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e898f-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="e898f-113">이 명령은 새 관리 데이터베이스를 만들고, 마지막 백업을 위해 Complete-AzSqlInstanceDatabaseLogReplay이 호출 될 때까지 지정 된 컨테이너에서 백업을 복원 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="e898f-114">변수</span><span class="sxs-lookup"><span data-stu-id="e898f-114">PARAMETERS</span></span>

### <span data-ttu-id="e898f-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="e898f-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="e898f-116">완료 시 자동으로 복원을 수행할지 여부를 나타내는 표시기입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="e898f-117">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="e898f-117">-Collation</span></span>
<span data-ttu-id="e898f-118">사용할 인스턴스 데이터베이스의 데이터 정렬입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="e898f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e898f-119">-DefaultProfile</span></span>
<span data-ttu-id="e898f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e898f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e898f-121">-InputObject</span></span>
<span data-ttu-id="e898f-122">인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-122">The instance database object.</span></span>

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

### <span data-ttu-id="e898f-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e898f-123">-InstanceName</span></span>
<span data-ttu-id="e898f-124">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-124">The name of the instance.</span></span>

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

### <span data-ttu-id="e898f-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="e898f-125">-LastBackupName</span></span>
<span data-ttu-id="e898f-126">복원할 마지막 백업 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="e898f-127">-이름</span><span class="sxs-lookup"><span data-stu-id="e898f-127">-Name</span></span>
<span data-ttu-id="e898f-128">인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="e898f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e898f-129">-PassThru</span></span>
<span data-ttu-id="e898f-130">동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e898f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e898f-131">-ResourceGroupName</span></span>
<span data-ttu-id="e898f-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="e898f-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="e898f-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="e898f-134">저장소 컨테이너 Sas 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="e898f-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="e898f-135">-StorageContainerUri</span></span>
<span data-ttu-id="e898f-136">저장소 컨테이너 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-136">The storage container URI.</span></span>

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

### <span data-ttu-id="e898f-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e898f-137">-Confirm</span></span>
<span data-ttu-id="e898f-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e898f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e898f-139">-WhatIf</span></span>
<span data-ttu-id="e898f-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e898f-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e898f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e898f-142">CommonParameters</span></span>
<span data-ttu-id="e898f-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e898f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e898f-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e898f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e898f-145">입력</span><span class="sxs-lookup"><span data-stu-id="e898f-145">INPUTS</span></span>

### <span data-ttu-id="e898f-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e898f-146">System.String</span></span>

### <span data-ttu-id="e898f-147">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="e898f-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e898f-148">출력</span><span class="sxs-lookup"><span data-stu-id="e898f-148">OUTPUTS</span></span>

### <span data-ttu-id="e898f-149">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="e898f-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e898f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e898f-150">NOTES</span></span>

## <span data-ttu-id="e898f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e898f-151">RELATED LINKS</span></span>
