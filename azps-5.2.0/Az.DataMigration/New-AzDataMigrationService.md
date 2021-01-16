---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350402"
---
# <span data-ttu-id="bc369-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="bc369-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="bc369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc369-102">SYNOPSIS</span></span>
<span data-ttu-id="bc369-103">Azure Database Migration Service의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="bc369-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc369-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc369-105">설명</span><span class="sxs-lookup"><span data-stu-id="bc369-105">DESCRIPTION</span></span>
<span data-ttu-id="bc369-106">이 New-AzDataMigrationService cmdlet은 Azure Database Migration Service의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="bc369-107">이 cmdlet은 기존 Azure 리소스 그룹의 이름, 만들 Azure Database Migration Service의 새 인스턴스에 대한 고유 이름, 인스턴스가 프로비전되는 지역, DMS Worker SKU의 이름 및 서비스가 상주할 Azure Virtual Subnet의 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="bc369-108">사용자가 Azure 로그인 세션의 기본 구독을 지정하거나 -SubscriptionName "MySubscription" Get-AzSubscription 실행해야 하기 때문에 구독 이름에 대한 매개 변수가 없습니다. | Select-AzSubscription 구독을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="bc369-109">예제</span><span class="sxs-lookup"><span data-stu-id="bc369-109">EXAMPLES</span></span>

### <span data-ttu-id="bc369-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc369-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="bc369-111">위의 예제에서는 미국 중부 지역에 TestService라는 Azure Database Migration Service의 새 인스턴스를 만드는 방법을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="bc369-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="bc369-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc369-112">PARAMETERS</span></span>

### <span data-ttu-id="bc369-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc369-113">-DefaultProfile</span></span>
<span data-ttu-id="bc369-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc369-115">-Location</span><span class="sxs-lookup"><span data-stu-id="bc369-115">-Location</span></span>
<span data-ttu-id="bc369-116">만들 Azure Database Migration Service 인스턴스의 위치로, Azure 지역에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="bc369-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bc369-117">-Name</span></span>
<span data-ttu-id="bc369-118">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="bc369-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc369-119">-ResourceGroupName</span></span>
<span data-ttu-id="bc369-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc369-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="bc369-121">-Sku</span></span>
<span data-ttu-id="bc369-122">Azure Database Migration Service 인스턴스에 대한 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="bc369-123">가능한 값은 현재 Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="bc369-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="bc369-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="bc369-124">-VirtualSubnetId</span></span>
<span data-ttu-id="bc369-125">Azure Database Migration Service 인스턴스에 사용할 지정된 가상 네트워크의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="bc369-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc369-126">-Confirm</span></span>
<span data-ttu-id="bc369-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc369-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc369-128">-WhatIf</span></span>
<span data-ttu-id="bc369-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bc369-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc369-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc369-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc369-131">CommonParameters</span></span>
<span data-ttu-id="bc369-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc369-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc369-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc369-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc369-134">입력</span><span class="sxs-lookup"><span data-stu-id="bc369-134">INPUTS</span></span>

### <span data-ttu-id="bc369-135">없음</span><span class="sxs-lookup"><span data-stu-id="bc369-135">None</span></span>

## <span data-ttu-id="bc369-136">출력</span><span class="sxs-lookup"><span data-stu-id="bc369-136">OUTPUTS</span></span>

### <span data-ttu-id="bc369-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="bc369-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="bc369-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc369-138">NOTES</span></span>

## <span data-ttu-id="bc369-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc369-139">RELATED LINKS</span></span>
