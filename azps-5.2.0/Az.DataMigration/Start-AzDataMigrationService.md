---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328978"
---
# <span data-ttu-id="4d3b1-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4d3b1-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="4d3b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3b1-103">중지된 상태로 Azure Database Migration Service의 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="4d3b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d3b1-104">SYNTAX</span></span>

### <span data-ttu-id="4d3b1-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d3b1-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d3b1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d3b1-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d3b1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d3b1-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3b1-108">설명</span><span class="sxs-lookup"><span data-stu-id="4d3b1-108">DESCRIPTION</span></span>
<span data-ttu-id="4d3b1-109">이 Start-AzDataMigrationService cmdlet은 중지된 상태로 Azure Database Migration Service의 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="4d3b1-110">예제</span><span class="sxs-lookup"><span data-stu-id="4d3b1-110">EXAMPLES</span></span>

### <span data-ttu-id="4d3b1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d3b1-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="4d3b1-112">위의 예제에서는 입력으로 전달된 서비스 이름을 기반으로 중지된 상태로 테스트 서비스라는 Azure Database Migration Service 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="4d3b1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4d3b1-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="4d3b1-114">위의 예제에서는 입력 매개 변수로 전달된 PSDataMigrationService를 기반으로 Azure Database Migration Service 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="4d3b1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d3b1-115">PARAMETERS</span></span>

### <span data-ttu-id="4d3b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3b1-116">-DefaultProfile</span></span>
<span data-ttu-id="4d3b1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d3b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d3b1-118">-InputObject</span></span>
<span data-ttu-id="4d3b1-119">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="4d3b1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d3b1-120">-Name</span></span>
<span data-ttu-id="4d3b1-121">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="4d3b1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d3b1-122">-PassThru</span></span>
<span data-ttu-id="4d3b1-123">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-123">Returns an true/false.</span></span>
<span data-ttu-id="4d3b1-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d3b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d3b1-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d3b1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d3b1-127">-ResourceId</span></span>
<span data-ttu-id="4d3b1-128">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="4d3b1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d3b1-129">-Confirm</span></span>
<span data-ttu-id="4d3b1-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d3b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3b1-131">-WhatIf</span></span>
<span data-ttu-id="4d3b1-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4d3b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3b1-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d3b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3b1-134">CommonParameters</span></span>
<span data-ttu-id="4d3b1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3b1-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4d3b1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3b1-137">입력</span><span class="sxs-lookup"><span data-stu-id="4d3b1-137">INPUTS</span></span>

### <span data-ttu-id="4d3b1-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4d3b1-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="4d3b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4d3b1-139">System.String</span></span>

## <span data-ttu-id="4d3b1-140">출력</span><span class="sxs-lookup"><span data-stu-id="4d3b1-140">OUTPUTS</span></span>

### <span data-ttu-id="4d3b1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d3b1-141">System.Boolean</span></span>

## <span data-ttu-id="4d3b1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d3b1-142">NOTES</span></span>

## <span data-ttu-id="4d3b1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d3b1-143">RELATED LINKS</span></span>
