---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346094"
---
# <span data-ttu-id="9278a-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9278a-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9278a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9278a-102">SYNOPSIS</span></span>
<span data-ttu-id="9278a-103">데이터베이스를 삭제하여 로그 재생 서비스를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="9278a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9278a-104">SYNTAX</span></span>

### <span data-ttu-id="9278a-105">LogReplayInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="9278a-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9278a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9278a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9278a-107">설명</span><span class="sxs-lookup"><span data-stu-id="9278a-107">DESCRIPTION</span></span>
<span data-ttu-id="9278a-108">**Stop-AzSqlInstanceDatabaseLogReplay** cmdlet은 데이터베이스를 삭제하여 로그 재생 서비스를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="9278a-109">예제</span><span class="sxs-lookup"><span data-stu-id="9278a-109">EXAMPLES</span></span>

### <span data-ttu-id="9278a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9278a-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="9278a-111">이 명령은 주어진 데이터베이스에서 로그 재생 서비스를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="9278a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9278a-112">PARAMETERS</span></span>

### <span data-ttu-id="9278a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9278a-113">-DefaultProfile</span></span>
<span data-ttu-id="9278a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9278a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9278a-115">-Force</span></span>
<span data-ttu-id="9278a-116">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="9278a-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9278a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9278a-117">-InputObject</span></span>
<span data-ttu-id="9278a-118">인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-118">The instance database object.</span></span>

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

### <span data-ttu-id="9278a-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9278a-119">-InstanceName</span></span>
<span data-ttu-id="9278a-120">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-120">The name of the instance.</span></span>

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

### <span data-ttu-id="9278a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9278a-121">-Name</span></span>
<span data-ttu-id="9278a-122">인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="9278a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9278a-123">-PassThru</span></span>
<span data-ttu-id="9278a-124">동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="9278a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9278a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9278a-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9278a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9278a-127">-Confirm</span></span>
<span data-ttu-id="9278a-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9278a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9278a-129">-WhatIf</span></span>
<span data-ttu-id="9278a-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9278a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9278a-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9278a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9278a-132">CommonParameters</span></span>
<span data-ttu-id="9278a-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9278a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9278a-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9278a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9278a-135">입력</span><span class="sxs-lookup"><span data-stu-id="9278a-135">INPUTS</span></span>

### <span data-ttu-id="9278a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9278a-136">System.String</span></span>

### <span data-ttu-id="9278a-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9278a-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9278a-138">출력</span><span class="sxs-lookup"><span data-stu-id="9278a-138">OUTPUTS</span></span>

### <span data-ttu-id="9278a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9278a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9278a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9278a-140">NOTES</span></span>

## <span data-ttu-id="9278a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9278a-141">RELATED LINKS</span></span>
