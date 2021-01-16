---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328964"
---
# <span data-ttu-id="8d9d3-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8d9d3-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="8d9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9d3-103">실행 중인 상태인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8d9d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d9d3-104">SYNTAX</span></span>

### <span data-ttu-id="8d9d3-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8d9d3-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9d3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d9d3-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d9d3-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9d3-108">설명</span><span class="sxs-lookup"><span data-stu-id="8d9d3-108">DESCRIPTION</span></span>
<span data-ttu-id="8d9d3-109">이 Stop-AzDataMigrationService cmdlet은 실행 중인 상태인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8d9d3-110">예제</span><span class="sxs-lookup"><span data-stu-id="8d9d3-110">EXAMPLES</span></span>

### <span data-ttu-id="8d9d3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d9d3-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="8d9d3-112">위의 예제에서는 입력 매개 변수로 전달된 서비스 이름을 기반으로 TestService라는 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="8d9d3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d9d3-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="8d9d3-114">위의 예제에서는 입력 매개 변수로 전달된 PSDataMigrationService 개체를 기반으로 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="8d9d3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d9d3-115">PARAMETERS</span></span>

### <span data-ttu-id="8d9d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9d3-116">-DefaultProfile</span></span>
<span data-ttu-id="8d9d3-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d9d3-118">-InputObject</span></span>
<span data-ttu-id="8d9d3-119">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8d9d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8d9d3-120">-Name</span></span>
<span data-ttu-id="8d9d3-121">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8d9d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d9d3-122">-PassThru</span></span>
<span data-ttu-id="8d9d3-123">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-123">Returns an true/false.</span></span>
<span data-ttu-id="8d9d3-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d9d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d9d3-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d9d3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d9d3-127">-ResourceId</span></span>
<span data-ttu-id="8d9d3-128">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8d9d3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d9d3-129">-Confirm</span></span>
<span data-ttu-id="8d9d3-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9d3-131">-WhatIf</span></span>
<span data-ttu-id="8d9d3-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d9d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9d3-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9d3-134">CommonParameters</span></span>
<span data-ttu-id="8d9d3-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9d3-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8d9d3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9d3-137">입력</span><span class="sxs-lookup"><span data-stu-id="8d9d3-137">INPUTS</span></span>

### <span data-ttu-id="8d9d3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8d9d3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="8d9d3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8d9d3-139">System.String</span></span>

## <span data-ttu-id="8d9d3-140">출력</span><span class="sxs-lookup"><span data-stu-id="8d9d3-140">OUTPUTS</span></span>

### <span data-ttu-id="8d9d3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d9d3-141">System.Boolean</span></span>

## <span data-ttu-id="8d9d3-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d9d3-142">NOTES</span></span>

## <span data-ttu-id="8d9d3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d9d3-143">RELATED LINKS</span></span>
