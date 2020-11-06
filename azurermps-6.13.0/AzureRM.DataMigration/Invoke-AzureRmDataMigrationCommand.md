---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532010"
---
# <span data-ttu-id="5f58e-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="5f58e-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="5f58e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f58e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f58e-103">기존 DMS 작업에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f58e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f58e-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f58e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f58e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f58e-106">New-AzureRmDataMigrationCommand cmdlet은 기존 마이그레이션 작업에서 실행할 새 명령 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="5f58e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5f58e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f58e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f58e-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="5f58e-109">위의 예제에서는 New-AzureRmDmsCommand cmdlet을 사용 하 여 기존 서비스, 프로젝트 및 작업에 대 한 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="5f58e-110">변수</span><span class="sxs-lookup"><span data-stu-id="5f58e-110">PARAMETERS</span></span>

### <span data-ttu-id="5f58e-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="5f58e-111">-CommandType</span></span>
<span data-ttu-id="5f58e-112">명령 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-112">Command Type.</span></span>

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

### <span data-ttu-id="5f58e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f58e-113">-DefaultProfile</span></span>
<span data-ttu-id="5f58e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f58e-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="5f58e-115">-ProjectName</span></span>
<span data-ttu-id="5f58e-116">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-116">The name of the project.</span></span>

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

### <span data-ttu-id="5f58e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f58e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f58e-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f58e-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5f58e-119">-ServiceName</span></span>
<span data-ttu-id="5f58e-120">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5f58e-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="5f58e-121">-TaskName</span></span>
<span data-ttu-id="5f58e-122">명령이 실행 되는 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="5f58e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5f58e-123">-Confirm</span></span>
<span data-ttu-id="5f58e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f58e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f58e-125">-WhatIf</span></span>
<span data-ttu-id="5f58e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f58e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f58e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f58e-128">CommonParameters</span></span>
<span data-ttu-id="5f58e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f58e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f58e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f58e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f58e-131">입력</span><span class="sxs-lookup"><span data-stu-id="5f58e-131">INPUTS</span></span>

### <span data-ttu-id="5f58e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f58e-132">System.String</span></span>

## <span data-ttu-id="5f58e-133">출력</span><span class="sxs-lookup"><span data-stu-id="5f58e-133">OUTPUTS</span></span>

### <span data-ttu-id="5f58e-134">DataMigration의 CommandProperties (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f58e-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="5f58e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5f58e-135">NOTES</span></span>

## <span data-ttu-id="5f58e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f58e-136">RELATED LINKS</span></span>
