---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: 9a6d2ba213054ea6b670205e84e3fd3893c59eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978560"
---
# <span data-ttu-id="c232b-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c232b-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="c232b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c232b-102">SYNOPSIS</span></span>
<span data-ttu-id="c232b-103">실행 중인 상태인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="c232b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c232b-104">SYNTAX</span></span>

### <span data-ttu-id="c232b-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c232b-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c232b-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c232b-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c232b-108">설명</span><span class="sxs-lookup"><span data-stu-id="c232b-108">DESCRIPTION</span></span>
<span data-ttu-id="c232b-109">Stop-AzDataMigrationService cmdlet은 실행 중인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="c232b-110">예제</span><span class="sxs-lookup"><span data-stu-id="c232b-110">EXAMPLES</span></span>

### <span data-ttu-id="c232b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c232b-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="c232b-112">위의 예제에서는 입력 매개 변수로 전달된 서비스 이름을 기반으로 TestService라는 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="c232b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c232b-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="c232b-114">위의 예제에서는 입력 매개 변수로 전달된 PSDataMigrationService 개체를 기반으로 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="c232b-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c232b-115">PARAMETERS</span></span>

### <span data-ttu-id="c232b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c232b-116">-DefaultProfile</span></span>
<span data-ttu-id="c232b-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c232b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c232b-118">-InputObject</span></span>
<span data-ttu-id="c232b-119">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="c232b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c232b-120">-Name</span></span>
<span data-ttu-id="c232b-121">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c232b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c232b-122">-PassThru</span></span>
<span data-ttu-id="c232b-123">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-123">Returns an true/false.</span></span>
<span data-ttu-id="c232b-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c232b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c232b-125">-ResourceGroupName</span></span>
<span data-ttu-id="c232b-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c232b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c232b-127">-ResourceId</span></span>
<span data-ttu-id="c232b-128">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="c232b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c232b-129">-Confirm</span></span>
<span data-ttu-id="c232b-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c232b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c232b-131">-WhatIf</span></span>
<span data-ttu-id="c232b-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c232b-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c232b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c232b-134">CommonParameters</span></span>
<span data-ttu-id="c232b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c232b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c232b-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c232b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c232b-137">입력</span><span class="sxs-lookup"><span data-stu-id="c232b-137">INPUTS</span></span>

### <span data-ttu-id="c232b-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c232b-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="c232b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c232b-139">System.String</span></span>

## <span data-ttu-id="c232b-140">출력</span><span class="sxs-lookup"><span data-stu-id="c232b-140">OUTPUTS</span></span>

### <span data-ttu-id="c232b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c232b-141">System.Boolean</span></span>

## <span data-ttu-id="c232b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c232b-142">NOTES</span></span>

## <span data-ttu-id="c232b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c232b-143">RELATED LINKS</span></span>
