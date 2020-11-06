---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525132"
---
# <span data-ttu-id="668d6-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="668d6-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="668d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668d6-102">SYNOPSIS</span></span>
<span data-ttu-id="668d6-103">Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="668d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="668d6-104">SYNTAX</span></span>

### <span data-ttu-id="668d6-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="668d6-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="668d6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="668d6-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="668d6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="668d6-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="668d6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="668d6-108">DESCRIPTION</span></span>
<span data-ttu-id="668d6-109">Start-AzureRmDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="668d6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="668d6-110">EXAMPLES</span></span>

### <span data-ttu-id="668d6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="668d6-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="668d6-112">위의 예제에서는 입력으로 전달 된 서비스 이름을 기반으로 하는 중지 된 상태의 Test Service 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="668d6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="668d6-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="668d6-114">위 예제에서는 입력 매개 변수로 전달 된 PSDataMigrationService를 기반으로 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="668d6-115">변수</span><span class="sxs-lookup"><span data-stu-id="668d6-115">PARAMETERS</span></span>

### <span data-ttu-id="668d6-116">-확인</span><span class="sxs-lookup"><span data-stu-id="668d6-116">-Confirm</span></span>
<span data-ttu-id="668d6-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668d6-118">-DefaultProfile</span></span>
<span data-ttu-id="668d6-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="668d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="668d6-120">-InputObject</span></span>
<span data-ttu-id="668d6-121">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="668d6-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="668d6-122">-이름</span><span class="sxs-lookup"><span data-stu-id="668d6-122">-Name</span></span>
<span data-ttu-id="668d6-123">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="668d6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="668d6-124">-PassThru</span></span>
<span data-ttu-id="668d6-125">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-125">Returns an true/false.</span></span>
<span data-ttu-id="668d6-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="668d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="668d6-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="668d6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="668d6-129">-ResourceId</span></span>
<span data-ttu-id="668d6-130">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="668d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668d6-131">-WhatIf</span></span>
<span data-ttu-id="668d6-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668d6-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="668d6-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="668d6-134">입력</span><span class="sxs-lookup"><span data-stu-id="668d6-134">INPUTS</span></span>

### <span data-ttu-id="668d6-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="668d6-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="668d6-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="668d6-136">System.String</span></span>


## <span data-ttu-id="668d6-137">출력</span><span class="sxs-lookup"><span data-stu-id="668d6-137">OUTPUTS</span></span>

### <span data-ttu-id="668d6-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="668d6-138">System.Boolean</span></span>


## <span data-ttu-id="668d6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="668d6-139">NOTES</span></span>

## <span data-ttu-id="668d6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="668d6-140">RELATED LINKS</span></span>


