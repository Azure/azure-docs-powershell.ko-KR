---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537632"
---
# <span data-ttu-id="68755-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="68755-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="68755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68755-102">SYNOPSIS</span></span>
<span data-ttu-id="68755-103">Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68755-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68755-104">SYNTAX</span></span>

### <span data-ttu-id="68755-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="68755-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68755-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68755-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68755-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68755-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68755-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68755-108">DESCRIPTION</span></span>
<span data-ttu-id="68755-109">Start-AzureRmDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="68755-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68755-110">EXAMPLES</span></span>

### <span data-ttu-id="68755-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="68755-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="68755-112">위의 예제에서는 입력으로 전달 된 서비스 이름을 기반으로 하는 중지 된 상태의 Test Service 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="68755-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="68755-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="68755-114">위 예제에서는 입력 매개 변수로 전달 된 PSDataMigrationService를 기반으로 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="68755-115">변수</span><span class="sxs-lookup"><span data-stu-id="68755-115">PARAMETERS</span></span>

### <span data-ttu-id="68755-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68755-116">-DefaultProfile</span></span>
<span data-ttu-id="68755-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68755-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68755-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68755-118">-InputObject</span></span>
<span data-ttu-id="68755-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="68755-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="68755-120">-이름</span><span class="sxs-lookup"><span data-stu-id="68755-120">-Name</span></span>
<span data-ttu-id="68755-121">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68755-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="68755-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68755-122">-PassThru</span></span>
<span data-ttu-id="68755-123">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-123">Returns an true/false.</span></span>
<span data-ttu-id="68755-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68755-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="68755-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68755-125">-ResourceGroupName</span></span>
<span data-ttu-id="68755-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68755-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="68755-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68755-127">-ResourceId</span></span>
<span data-ttu-id="68755-128">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="68755-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="68755-129">-확인</span><span class="sxs-lookup"><span data-stu-id="68755-129">-Confirm</span></span>
<span data-ttu-id="68755-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68755-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68755-131">-WhatIf</span></span>
<span data-ttu-id="68755-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68755-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68755-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68755-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68755-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68755-134">CommonParameters</span></span>
<span data-ttu-id="68755-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68755-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68755-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68755-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68755-137">입력</span><span class="sxs-lookup"><span data-stu-id="68755-137">INPUTS</span></span>

### <span data-ttu-id="68755-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="68755-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="68755-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68755-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="68755-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68755-140">System.String</span></span>

## <span data-ttu-id="68755-141">출력</span><span class="sxs-lookup"><span data-stu-id="68755-141">OUTPUTS</span></span>

### <span data-ttu-id="68755-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="68755-142">System.Boolean</span></span>

## <span data-ttu-id="68755-143">상속자</span><span class="sxs-lookup"><span data-stu-id="68755-143">NOTES</span></span>

## <span data-ttu-id="68755-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68755-144">RELATED LINKS</span></span>
