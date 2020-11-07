---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 737f723fddd7b351a0f1e9189590a61d83454976
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701023"
---
# <span data-ttu-id="78e97-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78e97-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="78e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e97-102">SYNOPSIS</span></span>
<span data-ttu-id="78e97-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="78e97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78e97-104">SYNTAX</span></span>

### <span data-ttu-id="78e97-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="78e97-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e97-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e97-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e97-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e97-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e97-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78e97-108">DESCRIPTION</span></span>
<span data-ttu-id="78e97-109">Remove-AzDataMigrationService cmdlet은 Azure에서 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="78e97-110">DeleteRunningTask 매개 변수를 제공 하면 제거 되는 서비스와 연결 된 Azure 데이터베이스 마이그레이션 서비스 작업이 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="78e97-111">예제의</span><span class="sxs-lookup"><span data-stu-id="78e97-111">EXAMPLES</span></span>

### <span data-ttu-id="78e97-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="78e97-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="78e97-113">위 예제에서는 MyResourceGroup 이라는 Azure 리소스 그룹에 포함 된 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="78e97-114">변수</span><span class="sxs-lookup"><span data-stu-id="78e97-114">PARAMETERS</span></span>

### <span data-ttu-id="78e97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e97-115">-DefaultProfile</span></span>
<span data-ttu-id="78e97-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78e97-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="78e97-117">-DeleteRunningTask</span></span>
<span data-ttu-id="78e97-118">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="78e97-118">Delete any running task</span></span>

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

### <span data-ttu-id="78e97-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78e97-119">-Force</span></span>
<span data-ttu-id="78e97-120">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="78e97-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="78e97-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78e97-121">-InputObject</span></span>
<span data-ttu-id="78e97-122">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="78e97-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="78e97-123">-이름</span><span class="sxs-lookup"><span data-stu-id="78e97-123">-Name</span></span>
<span data-ttu-id="78e97-124">데이터베이스 마이그레이션 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="78e97-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78e97-125">-PassThru</span></span>
<span data-ttu-id="78e97-126">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-126">Returns an true/false.</span></span>
<span data-ttu-id="78e97-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78e97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e97-128">-ResourceGroupName</span></span>
<span data-ttu-id="78e97-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="78e97-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78e97-130">-ResourceId</span></span>
<span data-ttu-id="78e97-131">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="78e97-132">-확인</span><span class="sxs-lookup"><span data-stu-id="78e97-132">-Confirm</span></span>
<span data-ttu-id="78e97-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e97-134">-WhatIf</span></span>
<span data-ttu-id="78e97-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e97-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e97-137">CommonParameters</span></span>
<span data-ttu-id="78e97-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e97-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e97-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e97-140">입력</span><span class="sxs-lookup"><span data-stu-id="78e97-140">INPUTS</span></span>

### <span data-ttu-id="78e97-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78e97-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="78e97-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78e97-142">System.String</span></span>

## <span data-ttu-id="78e97-143">출력</span><span class="sxs-lookup"><span data-stu-id="78e97-143">OUTPUTS</span></span>

### <span data-ttu-id="78e97-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="78e97-144">System.Boolean</span></span>

## <span data-ttu-id="78e97-145">상속자</span><span class="sxs-lookup"><span data-stu-id="78e97-145">NOTES</span></span>

## <span data-ttu-id="78e97-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78e97-146">RELATED LINKS</span></span>