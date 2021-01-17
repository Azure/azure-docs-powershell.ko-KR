---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375397"
---
# <span data-ttu-id="d9739-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d9739-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="d9739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9739-102">SYNOPSIS</span></span>
<span data-ttu-id="d9739-103">주어진 데이터베이스에 대한 로그 재생 서비스를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="d9739-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9739-104">SYNTAX</span></span>

### <span data-ttu-id="d9739-105">LogReplayInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9739-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9739-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d9739-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9739-107">설명</span><span class="sxs-lookup"><span data-stu-id="d9739-107">DESCRIPTION</span></span>
<span data-ttu-id="d9739-108">**Complete-AzSqlInstanceDatabaseLogReplay** cmdlet은 주어진 데이터베이스에서 로그 재생 서비스를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="d9739-109">예제</span><span class="sxs-lookup"><span data-stu-id="d9739-109">EXAMPLES</span></span>

### <span data-ttu-id="d9739-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9739-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="d9739-111">이 명령은 마지막 백업이 복원된 후 주어진 데이터베이스에 대한 로그 재생 서비스를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="d9739-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9739-112">PARAMETERS</span></span>

### <span data-ttu-id="d9739-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9739-113">-DefaultProfile</span></span>
<span data-ttu-id="d9739-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9739-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9739-115">-InputObject</span></span>
<span data-ttu-id="d9739-116">인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-116">The instance database object.</span></span>

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

### <span data-ttu-id="d9739-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d9739-117">-InstanceName</span></span>
<span data-ttu-id="d9739-118">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-118">The name of the instance.</span></span>

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

### <span data-ttu-id="d9739-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="d9739-119">-LastBackupName</span></span>
<span data-ttu-id="d9739-120">복원할 마지막 백업 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9739-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d9739-121">-Name</span></span>
<span data-ttu-id="d9739-122">인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="d9739-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9739-123">-PassThru</span></span>
<span data-ttu-id="d9739-124">동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="d9739-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9739-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9739-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9739-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9739-127">-Confirm</span></span>
<span data-ttu-id="d9739-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9739-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9739-129">-WhatIf</span></span>
<span data-ttu-id="d9739-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9739-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9739-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9739-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9739-132">CommonParameters</span></span>
<span data-ttu-id="d9739-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9739-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9739-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9739-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9739-135">입력</span><span class="sxs-lookup"><span data-stu-id="d9739-135">INPUTS</span></span>

### <span data-ttu-id="d9739-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d9739-136">System.String</span></span>

### <span data-ttu-id="d9739-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d9739-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d9739-138">출력</span><span class="sxs-lookup"><span data-stu-id="d9739-138">OUTPUTS</span></span>

## <span data-ttu-id="d9739-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9739-139">NOTES</span></span>

## <span data-ttu-id="d9739-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9739-140">RELATED LINKS</span></span>
