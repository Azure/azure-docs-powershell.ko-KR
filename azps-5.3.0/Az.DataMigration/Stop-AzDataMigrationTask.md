---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377532"
---
# <span data-ttu-id="679b0-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="679b0-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="679b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679b0-102">SYNOPSIS</span></span>
<span data-ttu-id="679b0-103">실행 중인 상태인 Azure Database Migration Service 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="679b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="679b0-104">SYNTAX</span></span>

### <span data-ttu-id="679b0-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="679b0-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679b0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="679b0-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="679b0-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679b0-108">설명</span><span class="sxs-lookup"><span data-stu-id="679b0-108">DESCRIPTION</span></span>
<span data-ttu-id="679b0-109">Stop-AzDataMigrationTask cmdlet은 실행 중인 상태의 데이터베이스 마이그레이션 활동을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="679b0-110">예제</span><span class="sxs-lookup"><span data-stu-id="679b0-110">EXAMPLES</span></span>

### <span data-ttu-id="679b0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="679b0-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="679b0-112">위의 예제에서는 myDMSProject 프로젝트 및 TestService라는 Azure Database Migration Service 인스턴스와 연결된 myDMSTask라는 Azure Database Migration Service 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="679b0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="679b0-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="679b0-114">위의 예제에서는 입력 매개 변수 PSProjectTask 개체로 전달된 Azure Database Migration Service 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="679b0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679b0-115">PARAMETERS</span></span>

### <span data-ttu-id="679b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679b0-116">-DefaultProfile</span></span>
<span data-ttu-id="679b0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="679b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679b0-118">-InputObject</span></span>
<span data-ttu-id="679b0-119">PSProjectTask 개체.</span><span class="sxs-lookup"><span data-stu-id="679b0-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="679b0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="679b0-120">-Name</span></span>
<span data-ttu-id="679b0-121">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-121">The name of the task.</span></span>

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

### <span data-ttu-id="679b0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="679b0-122">-PassThru</span></span>
<span data-ttu-id="679b0-123">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-123">Returns an true/false.</span></span>
<span data-ttu-id="679b0-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="679b0-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="679b0-125">-ProjectName</span></span>
<span data-ttu-id="679b0-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-126">The name of the project.</span></span>

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

### <span data-ttu-id="679b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="679b0-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="679b0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="679b0-129">-ResourceId</span></span>
<span data-ttu-id="679b0-130">ProjectTask 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="679b0-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="679b0-131">-ServiceName</span></span>
<span data-ttu-id="679b0-132">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="679b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679b0-133">-Confirm</span></span>
<span data-ttu-id="679b0-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679b0-135">-WhatIf</span></span>
<span data-ttu-id="679b0-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="679b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679b0-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679b0-138">CommonParameters</span></span>
<span data-ttu-id="679b0-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="679b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679b0-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="679b0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679b0-141">입력</span><span class="sxs-lookup"><span data-stu-id="679b0-141">INPUTS</span></span>

### <span data-ttu-id="679b0-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="679b0-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="679b0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="679b0-143">System.String</span></span>

## <span data-ttu-id="679b0-144">출력</span><span class="sxs-lookup"><span data-stu-id="679b0-144">OUTPUTS</span></span>

### <span data-ttu-id="679b0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="679b0-145">System.Boolean</span></span>

## <span data-ttu-id="679b0-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="679b0-146">NOTES</span></span>

## <span data-ttu-id="679b0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="679b0-147">RELATED LINKS</span></span>
