---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213277"
---
# <span data-ttu-id="cdfd0-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cdfd0-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="cdfd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfd0-103">지정 된 데이터베이스에 대 한 로그 재생 서비스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="cdfd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdfd0-104">SYNTAX</span></span>

### <span data-ttu-id="cdfd0-105">Logreplayinstancedatabase Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="cdfd0-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdfd0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cdfd0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdfd0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cdfd0-107">DESCRIPTION</span></span>
<span data-ttu-id="cdfd0-108">**전체 AzSqlInstanceDatabaseLogReplay** cmdlet은 지정 된 데이터베이스에서 로그 재생 서비스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="cdfd0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cdfd0-109">EXAMPLES</span></span>

### <span data-ttu-id="cdfd0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdfd0-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="cdfd0-111">이 명령은 마지막 백업이 복원 된 후 지정 된 데이터베이스에 대 한 로그 재생 서비스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="cdfd0-112">변수</span><span class="sxs-lookup"><span data-stu-id="cdfd0-112">PARAMETERS</span></span>

### <span data-ttu-id="cdfd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfd0-113">-DefaultProfile</span></span>
<span data-ttu-id="cdfd0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdfd0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdfd0-115">-InputObject</span></span>
<span data-ttu-id="cdfd0-116">인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-116">The instance database object.</span></span>

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

### <span data-ttu-id="cdfd0-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cdfd0-117">-InstanceName</span></span>
<span data-ttu-id="cdfd0-118">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-118">The name of the instance.</span></span>

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

### <span data-ttu-id="cdfd0-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="cdfd0-119">-LastBackupName</span></span>
<span data-ttu-id="cdfd0-120">복원할 마지막 백업 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="cdfd0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="cdfd0-121">-Name</span></span>
<span data-ttu-id="cdfd0-122">인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="cdfd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdfd0-123">-PassThru</span></span>
<span data-ttu-id="cdfd0-124">동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="cdfd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdfd0-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="cdfd0-127">-확인</span><span class="sxs-lookup"><span data-stu-id="cdfd0-127">-Confirm</span></span>
<span data-ttu-id="cdfd0-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfd0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfd0-129">-WhatIf</span></span>
<span data-ttu-id="cdfd0-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdfd0-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdfd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfd0-132">CommonParameters</span></span>
<span data-ttu-id="cdfd0-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfd0-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdfd0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfd0-135">입력</span><span class="sxs-lookup"><span data-stu-id="cdfd0-135">INPUTS</span></span>

### <span data-ttu-id="cdfd0-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cdfd0-136">System.String</span></span>

### <span data-ttu-id="cdfd0-137">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="cdfd0-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cdfd0-138">출력</span><span class="sxs-lookup"><span data-stu-id="cdfd0-138">OUTPUTS</span></span>

## <span data-ttu-id="cdfd0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="cdfd0-139">NOTES</span></span>

## <span data-ttu-id="cdfd0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdfd0-140">RELATED LINKS</span></span>
