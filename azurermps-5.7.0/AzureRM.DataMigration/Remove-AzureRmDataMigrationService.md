---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532173"
---
# <span data-ttu-id="c5c88-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c5c88-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="c5c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c88-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c88-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5c88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5c88-104">SYNTAX</span></span>

### <span data-ttu-id="c5c88-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5c88-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c5c88-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c88-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c5c88-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c88-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c5c88-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5c88-108">DESCRIPTION</span></span>
<span data-ttu-id="c5c88-109">Remove-AzureRmDataMigrationService cmdlet은 Azure에서 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="c5c88-110">DeleteRunningTask 매개 변수를 제공 하면 제거 되는 서비스와 연결 된 Azure 데이터베이스 마이그레이션 서비스 작업이 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="c5c88-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c5c88-111">EXAMPLES</span></span>

### <span data-ttu-id="c5c88-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5c88-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="c5c88-113">위 예제에서는 MyResourceGroup 이라는 Azure 리소스 그룹에 포함 된 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="c5c88-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5c88-114">PARAMETERS</span></span>

### <span data-ttu-id="c5c88-115">-확인</span><span class="sxs-lookup"><span data-stu-id="c5c88-115">-Confirm</span></span>
<span data-ttu-id="c5c88-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c88-117">-DefaultProfile</span></span>
<span data-ttu-id="c5c88-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="c5c88-119">-DeleteRunningTask</span></span>
<span data-ttu-id="c5c88-120">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="c5c88-120">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c5c88-121">-Force</span></span>
<span data-ttu-id="c5c88-122">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="c5c88-122">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c88-123">-InputObject</span></span>
<span data-ttu-id="c5c88-124">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="c5c88-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-125">-이름</span><span class="sxs-lookup"><span data-stu-id="c5c88-125">-Name</span></span>
<span data-ttu-id="c5c88-126">데이터 마이그레이션 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5c88-127">-PassThru</span></span>
<span data-ttu-id="c5c88-128">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-128">Returns an true/false.</span></span>
<span data-ttu-id="c5c88-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c88-130">-ResourceGroupName</span></span>
<span data-ttu-id="c5c88-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c88-132">-ResourceId</span></span>
<span data-ttu-id="c5c88-133">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-133">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c88-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c88-134">-WhatIf</span></span>
<span data-ttu-id="c5c88-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c88-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5c88-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c5c88-137">입력</span><span class="sxs-lookup"><span data-stu-id="c5c88-137">INPUTS</span></span>

### <span data-ttu-id="c5c88-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c5c88-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="c5c88-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5c88-139">System.String</span></span>


## <span data-ttu-id="c5c88-140">출력</span><span class="sxs-lookup"><span data-stu-id="c5c88-140">OUTPUTS</span></span>

### <span data-ttu-id="c5c88-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c5c88-141">System.Boolean</span></span>


## <span data-ttu-id="c5c88-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c5c88-142">NOTES</span></span>

## <span data-ttu-id="c5c88-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5c88-143">RELATED LINKS</span></span>


