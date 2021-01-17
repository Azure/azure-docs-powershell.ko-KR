---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489028"
---
# <span data-ttu-id="aee34-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="aee34-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="aee34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aee34-102">SYNOPSIS</span></span>
<span data-ttu-id="aee34-103">기존 DMS 작업에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="aee34-104">구문</span><span class="sxs-lookup"><span data-stu-id="aee34-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="aee34-105">설명</span><span class="sxs-lookup"><span data-stu-id="aee34-105">DESCRIPTION</span></span>
<span data-ttu-id="aee34-106">이 Invoke-AzDataMigrationCommand cmdlet은 기존 마이그레이션 작업에서 실행할 새 명령 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="aee34-107">예제</span><span class="sxs-lookup"><span data-stu-id="aee34-107">EXAMPLES</span></span>

### <span data-ttu-id="aee34-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aee34-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="aee34-109">위의 예제에서는 Invoke-AzDataMigrationCommand cmdlet을 사용하여 기존 서비스, 프로젝트 및 작업에 대한 명령을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="aee34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aee34-110">PARAMETERS</span></span>

### <span data-ttu-id="aee34-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="aee34-111">-CommandType</span></span>
<span data-ttu-id="aee34-112">명령 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee34-113">-DefaultProfile</span></span>
<span data-ttu-id="aee34-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee34-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="aee34-115">-ProjectName</span></span>
<span data-ttu-id="aee34-116">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee34-117">-ResourceGroupName</span></span>
<span data-ttu-id="aee34-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee34-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aee34-119">-ServiceName</span></span>
<span data-ttu-id="aee34-120">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee34-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="aee34-121">-TaskName</span></span>
<span data-ttu-id="aee34-122">명령이 실행된 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="aee34-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="aee34-123">-ObjectName</span></span>
<span data-ttu-id="aee34-124">명령이 실행될 데이터베이스 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="aee34-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aee34-125">-Confirm</span></span>
<span data-ttu-id="aee34-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee34-127">-WhatIf</span></span>
<span data-ttu-id="aee34-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aee34-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee34-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee34-130">CommonParameters</span></span>
<span data-ttu-id="aee34-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aee34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee34-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aee34-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee34-133">입력</span><span class="sxs-lookup"><span data-stu-id="aee34-133">INPUTS</span></span>

### <span data-ttu-id="aee34-134">System.String</span><span class="sxs-lookup"><span data-stu-id="aee34-134">System.String</span></span>

## <span data-ttu-id="aee34-135">출력</span><span class="sxs-lookup"><span data-stu-id="aee34-135">OUTPUTS</span></span>

### <span data-ttu-id="aee34-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="aee34-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="aee34-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aee34-137">NOTES</span></span>

## <span data-ttu-id="aee34-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aee34-138">RELATED LINKS</span></span>
