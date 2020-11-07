---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877534"
---
# <span data-ttu-id="6fe0f-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="6fe0f-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="6fe0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe0f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe0f-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="6fe0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fe0f-104">SYNTAX</span></span>

### <span data-ttu-id="6fe0f-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fe0f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe0f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe0f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe0f-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe0f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6fe0f-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe0f-109">Remove-AzDataMigrationTask cmdlet은 Azure에서 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="6fe0f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6fe0f-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe0f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fe0f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="6fe0f-112">앞의 예제에서는 작업 이름 매개 변수를 기준으로 Azure에서 TestTask 라는 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="6fe0f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6fe0f-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="6fe0f-114">앞의 예제에서는 전달 된 PSProjectTask 개체를 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="6fe0f-115">변수</span><span class="sxs-lookup"><span data-stu-id="6fe0f-115">PARAMETERS</span></span>

### <span data-ttu-id="6fe0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe0f-116">-DefaultProfile</span></span>
<span data-ttu-id="6fe0f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fe0f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6fe0f-118">-Force</span></span>
<span data-ttu-id="6fe0f-119">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="6fe0f-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6fe0f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe0f-120">-InputObject</span></span>
<span data-ttu-id="6fe0f-121">PSProjectTask 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6fe0f-122">-Name</span></span>
<span data-ttu-id="6fe0f-123">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fe0f-124">-PassThru</span></span>
<span data-ttu-id="6fe0f-125">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-125">Returns an true/false.</span></span>
<span data-ttu-id="6fe0f-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6fe0f-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="6fe0f-127">-ProjectName</span></span>
<span data-ttu-id="6fe0f-128">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-128">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="6fe0f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe0f-131">-ResourceId</span></span>
<span data-ttu-id="6fe0f-132">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-132">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6fe0f-133">-ServiceName</span></span>
<span data-ttu-id="6fe0f-134">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-134">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe0f-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6fe0f-135">-Confirm</span></span>
<span data-ttu-id="6fe0f-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe0f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe0f-137">-WhatIf</span></span>
<span data-ttu-id="6fe0f-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe0f-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe0f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe0f-140">CommonParameters</span></span>
<span data-ttu-id="6fe0f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe0f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe0f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe0f-143">입력</span><span class="sxs-lookup"><span data-stu-id="6fe0f-143">INPUTS</span></span>

### <span data-ttu-id="6fe0f-144">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="6fe0f-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fe0f-145">System.String</span></span>

## <span data-ttu-id="6fe0f-146">출력</span><span class="sxs-lookup"><span data-stu-id="6fe0f-146">OUTPUTS</span></span>

### <span data-ttu-id="6fe0f-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6fe0f-147">System.Boolean</span></span>

## <span data-ttu-id="6fe0f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6fe0f-148">NOTES</span></span>

## <span data-ttu-id="6fe0f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fe0f-149">RELATED LINKS</span></span>
