---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: b838cef6b72c783c8a9252df1e448e27bd100e36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696752"
---
# <span data-ttu-id="e4983-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e4983-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="e4983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4983-102">SYNOPSIS</span></span>
<span data-ttu-id="e4983-103">실행 상태인 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e4983-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4983-104">SYNTAX</span></span>

### <span data-ttu-id="e4983-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4983-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4983-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4983-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4983-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4983-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4983-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e4983-108">DESCRIPTION</span></span>
<span data-ttu-id="e4983-109">Stop-AzDataMigrationService cmdlet은 실행 상태인 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="e4983-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e4983-110">EXAMPLES</span></span>

### <span data-ttu-id="e4983-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4983-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e4983-112">위 예제에서는 입력 매개 변수로 전달 된 서비스 이름을 기반으로 하는 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="e4983-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e4983-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e4983-114">위 예제에서는 입력 매개 변수로 전달 된 PSDataMigrationService 개체를 기반으로 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="e4983-115">변수</span><span class="sxs-lookup"><span data-stu-id="e4983-115">PARAMETERS</span></span>

### <span data-ttu-id="e4983-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4983-116">-DefaultProfile</span></span>
<span data-ttu-id="e4983-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4983-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4983-118">-InputObject</span></span>
<span data-ttu-id="e4983-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="e4983-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e4983-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e4983-120">-Name</span></span>
<span data-ttu-id="e4983-121">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e4983-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4983-122">-PassThru</span></span>
<span data-ttu-id="e4983-123">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-123">Returns an true/false.</span></span>
<span data-ttu-id="e4983-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4983-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4983-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4983-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4983-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4983-127">-ResourceId</span></span>
<span data-ttu-id="e4983-128">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e4983-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e4983-129">-Confirm</span></span>
<span data-ttu-id="e4983-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4983-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4983-131">-WhatIf</span></span>
<span data-ttu-id="e4983-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4983-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4983-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4983-134">CommonParameters</span></span>
<span data-ttu-id="e4983-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4983-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4983-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4983-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4983-137">입력</span><span class="sxs-lookup"><span data-stu-id="e4983-137">INPUTS</span></span>

### <span data-ttu-id="e4983-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e4983-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e4983-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4983-139">System.String</span></span>

## <span data-ttu-id="e4983-140">출력</span><span class="sxs-lookup"><span data-stu-id="e4983-140">OUTPUTS</span></span>

### <span data-ttu-id="e4983-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e4983-141">System.Boolean</span></span>

## <span data-ttu-id="e4983-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e4983-142">NOTES</span></span>

## <span data-ttu-id="e4983-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4983-143">RELATED LINKS</span></span>