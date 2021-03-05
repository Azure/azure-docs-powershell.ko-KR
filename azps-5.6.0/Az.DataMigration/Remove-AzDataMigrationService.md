---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996772"
---
# <span data-ttu-id="69339-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="69339-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="69339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69339-102">SYNOPSIS</span></span>
<span data-ttu-id="69339-103">Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69339-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="69339-104">구문</span><span class="sxs-lookup"><span data-stu-id="69339-104">SYNTAX</span></span>

### <span data-ttu-id="69339-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="69339-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69339-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69339-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69339-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69339-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69339-108">설명</span><span class="sxs-lookup"><span data-stu-id="69339-108">DESCRIPTION</span></span>
<span data-ttu-id="69339-109">Remove-AzDataMigrationService cmdlet은 Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69339-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="69339-110">DeleteRunningTask 매개 변수를 제공하면 제거되는 서비스와 연결된 모든 Azure Database Migration Service 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="69339-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="69339-111">예제</span><span class="sxs-lookup"><span data-stu-id="69339-111">EXAMPLES</span></span>

### <span data-ttu-id="69339-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="69339-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="69339-113">위의 예제에서는 MyResourceGroup이라는 Azure 리소스 그룹에 포함된 TestService라는 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69339-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="69339-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="69339-114">PARAMETERS</span></span>

### <span data-ttu-id="69339-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69339-115">-DefaultProfile</span></span>
<span data-ttu-id="69339-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69339-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69339-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="69339-117">-DeleteRunningTask</span></span>
<span data-ttu-id="69339-118">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="69339-118">Delete any running task</span></span>

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

### <span data-ttu-id="69339-119">-Force</span><span class="sxs-lookup"><span data-stu-id="69339-119">-Force</span></span>
<span data-ttu-id="69339-120">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="69339-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="69339-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69339-121">-InputObject</span></span>
<span data-ttu-id="69339-122">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="69339-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="69339-123">-Name</span><span class="sxs-lookup"><span data-stu-id="69339-123">-Name</span></span>
<span data-ttu-id="69339-124">데이터베이스 마이그레이션 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69339-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="69339-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69339-125">-PassThru</span></span>
<span data-ttu-id="69339-126">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="69339-126">Returns an true/false.</span></span>
<span data-ttu-id="69339-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69339-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69339-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69339-128">-ResourceGroupName</span></span>
<span data-ttu-id="69339-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69339-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="69339-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69339-130">-ResourceId</span></span>
<span data-ttu-id="69339-131">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69339-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="69339-132">-확인</span><span class="sxs-lookup"><span data-stu-id="69339-132">-Confirm</span></span>
<span data-ttu-id="69339-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="69339-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69339-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69339-134">-WhatIf</span></span>
<span data-ttu-id="69339-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="69339-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69339-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69339-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69339-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69339-137">CommonParameters</span></span>
<span data-ttu-id="69339-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69339-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69339-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="69339-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69339-140">입력</span><span class="sxs-lookup"><span data-stu-id="69339-140">INPUTS</span></span>

### <span data-ttu-id="69339-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="69339-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="69339-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69339-142">System.String</span></span>

## <span data-ttu-id="69339-143">출력</span><span class="sxs-lookup"><span data-stu-id="69339-143">OUTPUTS</span></span>

### <span data-ttu-id="69339-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69339-144">System.Boolean</span></span>

## <span data-ttu-id="69339-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69339-145">NOTES</span></span>

## <span data-ttu-id="69339-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69339-146">RELATED LINKS</span></span>
