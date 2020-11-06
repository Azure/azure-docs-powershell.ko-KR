---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532009"
---
# <span data-ttu-id="d2f04-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d2f04-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="d2f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f04-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f04-103">Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2f04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2f04-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2f04-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f04-106">New-AzureRmDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="d2f04-107">이 cmdlet은 기존 Azure 리소스 그룹의 이름, 만들려는 Azure Database 마이그레이션 서비스의 새 인스턴스에 대 한 고유 이름, 인스턴스가 프로 비전 된 지역, DMS 작업자 SKU의 이름, 서비스를 상주할 Azure 가상 서브넷의 이름에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="d2f04-108">구독 이름에 대 한 매개 변수는 사용자가 Azure 로그인 세션의 기본 구독을 지정 하거나 Get-AzureRmSubscription를 실행 하는 데 필요 하기 때문에 (SubscriptionName "MySubscription" |) 할 수 없습니다. 다른 구독을 선택 Select-AzureRmSubscription.</span><span class="sxs-lookup"><span data-stu-id="d2f04-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="d2f04-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2f04-109">EXAMPLES</span></span>

### <span data-ttu-id="d2f04-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2f04-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="d2f04-111">위 예제에서는 중앙 US 지역에서 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="d2f04-112">변수</span><span class="sxs-lookup"><span data-stu-id="d2f04-112">PARAMETERS</span></span>

### <span data-ttu-id="d2f04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f04-113">-DefaultProfile</span></span>
<span data-ttu-id="d2f04-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f04-115">-위치</span><span class="sxs-lookup"><span data-stu-id="d2f04-115">-Location</span></span>
<span data-ttu-id="d2f04-116">만들 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치 이며, Azure 지역에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f04-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d2f04-117">-Name</span></span>
<span data-ttu-id="d2f04-118">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f04-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2f04-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f04-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="d2f04-121">-Sku</span></span>
<span data-ttu-id="d2f04-122">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="d2f04-123">사용할 수 있는 값은 현재 Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="d2f04-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f04-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="d2f04-124">-VirtualSubnetId</span></span>
<span data-ttu-id="d2f04-125">Azure 데이터베이스 마이그레이션 서비스 인스턴스에 사용할 지정 된 가상 네트워크 아래 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f04-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d2f04-126">-Confirm</span></span>
<span data-ttu-id="d2f04-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f04-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f04-128">-WhatIf</span></span>
<span data-ttu-id="d2f04-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2f04-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f04-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f04-131">CommonParameters</span></span>
<span data-ttu-id="d2f04-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f04-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f04-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f04-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f04-134">입력</span><span class="sxs-lookup"><span data-stu-id="d2f04-134">INPUTS</span></span>

### <span data-ttu-id="d2f04-135">않아야</span><span class="sxs-lookup"><span data-stu-id="d2f04-135">None</span></span>

## <span data-ttu-id="d2f04-136">출력</span><span class="sxs-lookup"><span data-stu-id="d2f04-136">OUTPUTS</span></span>

### <span data-ttu-id="d2f04-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d2f04-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="d2f04-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d2f04-138">NOTES</span></span>

## <span data-ttu-id="d2f04-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2f04-139">RELATED LINKS</span></span>