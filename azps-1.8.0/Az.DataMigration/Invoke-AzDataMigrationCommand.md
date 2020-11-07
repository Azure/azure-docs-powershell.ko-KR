---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868470"
---
# <span data-ttu-id="7c5d2-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="7c5d2-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="7c5d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5d2-103">기존 DMS 작업에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="7c5d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c5d2-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="7c5d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c5d2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5d2-106">Invoke-AzDataMigrationCommand cmdlet은 기존 마이그레이션 작업에서 실행할 새 명령 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="7c5d2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c5d2-107">EXAMPLES</span></span>

### <span data-ttu-id="7c5d2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c5d2-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="7c5d2-109">위의 예제에서는 Invoke-AzDataMigrationCommand cmdlet을 사용 하 여 기존 서비스, 프로젝트 및 작업에 대 한 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="7c5d2-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c5d2-110">PARAMETERS</span></span>

### <span data-ttu-id="7c5d2-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="7c5d2-111">-CommandType</span></span>
<span data-ttu-id="7c5d2-112">명령 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-112">Command Type.</span></span>

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

### <span data-ttu-id="7c5d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-113">-DefaultProfile</span></span>
<span data-ttu-id="7c5d2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c5d2-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-115">-ProjectName</span></span>
<span data-ttu-id="7c5d2-116">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-116">The name of the project.</span></span>

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

### <span data-ttu-id="7c5d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c5d2-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c5d2-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-119">-ServiceName</span></span>
<span data-ttu-id="7c5d2-120">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="7c5d2-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-121">-TaskName</span></span>
<span data-ttu-id="7c5d2-122">명령이 실행 되는 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="7c5d2-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-123">-ObjectName</span></span>
<span data-ttu-id="7c5d2-124">명령이 실행 되는 데이터베이스 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="7c5d2-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7c5d2-125">-Confirm</span></span>
<span data-ttu-id="7c5d2-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c5d2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c5d2-127">-WhatIf</span></span>
<span data-ttu-id="7c5d2-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c5d2-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c5d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-130">CommonParameters</span></span>
<span data-ttu-id="7c5d2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5d2-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c5d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5d2-133">입력</span><span class="sxs-lookup"><span data-stu-id="7c5d2-133">INPUTS</span></span>

### <span data-ttu-id="7c5d2-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c5d2-134">System.String</span></span>

## <span data-ttu-id="7c5d2-135">출력</span><span class="sxs-lookup"><span data-stu-id="7c5d2-135">OUTPUTS</span></span>

### <span data-ttu-id="7c5d2-136">DataMigration의 CommandProperties (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7c5d2-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="7c5d2-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7c5d2-137">NOTES</span></span>

## <span data-ttu-id="7c5d2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c5d2-138">RELATED LINKS</span></span>
