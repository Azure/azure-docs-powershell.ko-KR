---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377609"
---
# <span data-ttu-id="f7dce-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f7dce-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="f7dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7dce-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dce-103">Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="f7dce-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7dce-104">SYNTAX</span></span>

### <span data-ttu-id="f7dce-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f7dce-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7dce-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dce-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7dce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dce-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7dce-108">설명</span><span class="sxs-lookup"><span data-stu-id="f7dce-108">DESCRIPTION</span></span>
<span data-ttu-id="f7dce-109">이 Remove-AzDataMigrationService cmdlet은 Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="f7dce-110">DeleteRunningTask 매개 변수를 제공하면 제거되는 서비스에 연결된 모든 Azure Database Migration Service 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="f7dce-111">예제</span><span class="sxs-lookup"><span data-stu-id="f7dce-111">EXAMPLES</span></span>

### <span data-ttu-id="f7dce-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7dce-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="f7dce-113">위의 예제에서는 MyResourceGroup이라는 Azure 리소스 그룹에 포함된 TestService라는 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="f7dce-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7dce-114">PARAMETERS</span></span>

### <span data-ttu-id="f7dce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dce-115">-DefaultProfile</span></span>
<span data-ttu-id="f7dce-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7dce-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="f7dce-117">-DeleteRunningTask</span></span>
<span data-ttu-id="f7dce-118">실행 중인 모든 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="f7dce-118">Delete any running task</span></span>

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

### <span data-ttu-id="f7dce-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f7dce-119">-Force</span></span>
<span data-ttu-id="f7dce-120">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="f7dce-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f7dce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7dce-121">-InputObject</span></span>
<span data-ttu-id="f7dce-122">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dce-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f7dce-123">-Name</span></span>
<span data-ttu-id="f7dce-124">Database Migration Service의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dce-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7dce-125">-PassThru</span></span>
<span data-ttu-id="f7dce-126">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-126">Returns an true/false.</span></span>
<span data-ttu-id="f7dce-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7dce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dce-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7dce-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7dce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7dce-130">-ResourceId</span></span>
<span data-ttu-id="f7dce-131">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="f7dce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7dce-132">-Confirm</span></span>
<span data-ttu-id="f7dce-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7dce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7dce-134">-WhatIf</span></span>
<span data-ttu-id="f7dce-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f7dce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7dce-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7dce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dce-137">CommonParameters</span></span>
<span data-ttu-id="f7dce-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dce-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f7dce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dce-140">입력</span><span class="sxs-lookup"><span data-stu-id="f7dce-140">INPUTS</span></span>

### <span data-ttu-id="f7dce-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f7dce-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="f7dce-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f7dce-142">System.String</span></span>

## <span data-ttu-id="f7dce-143">출력</span><span class="sxs-lookup"><span data-stu-id="f7dce-143">OUTPUTS</span></span>

### <span data-ttu-id="f7dce-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7dce-144">System.Boolean</span></span>

## <span data-ttu-id="f7dce-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7dce-145">NOTES</span></span>

## <span data-ttu-id="f7dce-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7dce-146">RELATED LINKS</span></span>
