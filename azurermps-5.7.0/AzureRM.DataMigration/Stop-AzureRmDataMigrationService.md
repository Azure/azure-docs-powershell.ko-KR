---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537759"
---
# <span data-ttu-id="a294d-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a294d-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="a294d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a294d-102">SYNOPSIS</span></span>
<span data-ttu-id="a294d-103">실행 상태인 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a294d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a294d-104">SYNTAX</span></span>

### <span data-ttu-id="a294d-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a294d-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a294d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a294d-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a294d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a294d-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a294d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a294d-108">DESCRIPTION</span></span>
<span data-ttu-id="a294d-109">Stop-AzureRmDataMigrationService cmdlet은 실행 상태인 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="a294d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a294d-110">EXAMPLES</span></span>

### <span data-ttu-id="a294d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a294d-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="a294d-112">위 예제에서는 입력 매개 변수로 전달 된 서비스 이름을 기반으로 하는 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="a294d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a294d-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="a294d-114">위 예제에서는 입력 매개 변수로 전달 된 PSDataMigrationService 개체를 기반으로 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="a294d-115">변수</span><span class="sxs-lookup"><span data-stu-id="a294d-115">PARAMETERS</span></span>

### <span data-ttu-id="a294d-116">-확인</span><span class="sxs-lookup"><span data-stu-id="a294d-116">-Confirm</span></span>
<span data-ttu-id="a294d-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a294d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a294d-118">-DefaultProfile</span></span>
<span data-ttu-id="a294d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a294d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a294d-120">-InputObject</span></span>
<span data-ttu-id="a294d-121">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="a294d-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="a294d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a294d-122">-Name</span></span>
<span data-ttu-id="a294d-123">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="a294d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a294d-124">-PassThru</span></span>
<span data-ttu-id="a294d-125">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-125">Returns an true/false.</span></span>
<span data-ttu-id="a294d-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a294d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a294d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a294d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a294d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a294d-129">-ResourceId</span></span>
<span data-ttu-id="a294d-130">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="a294d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a294d-131">-WhatIf</span></span>
<span data-ttu-id="a294d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a294d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a294d-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a294d-134">입력</span><span class="sxs-lookup"><span data-stu-id="a294d-134">INPUTS</span></span>

### <span data-ttu-id="a294d-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a294d-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="a294d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a294d-136">System.String</span></span>


## <span data-ttu-id="a294d-137">출력</span><span class="sxs-lookup"><span data-stu-id="a294d-137">OUTPUTS</span></span>

### <span data-ttu-id="a294d-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a294d-138">System.Boolean</span></span>


## <span data-ttu-id="a294d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a294d-139">NOTES</span></span>

## <span data-ttu-id="a294d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a294d-140">RELATED LINKS</span></span>

