---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354489"
---
# <span data-ttu-id="772f2-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="772f2-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="772f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="772f2-102">SYNOPSIS</span></span>
<span data-ttu-id="772f2-103">Data Factory에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="772f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="772f2-104">SYNTAX</span></span>

### <span data-ttu-id="772f2-105">BySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="772f2-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="772f2-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="772f2-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="772f2-107">설명</span><span class="sxs-lookup"><span data-stu-id="772f2-107">DESCRIPTION</span></span>
<span data-ttu-id="772f2-108">Get-AzDataFactoryV2 cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="772f2-109">데이터 팩터리의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="772f2-110">이름을 지정하지 않으면 이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="772f2-111">예제</span><span class="sxs-lookup"><span data-stu-id="772f2-111">EXAMPLES</span></span>

### <span data-ttu-id="772f2-112">예제 1: 모든 데이터 팩터리 얻기</span><span class="sxs-lookup"><span data-stu-id="772f2-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded
```

<span data-ttu-id="772f2-113">Azure 구독의 모든 데이터 팩터리에 대한 정보를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="772f2-114">예제 2: 특정 데이터 팩터리 얻기</span><span class="sxs-lookup"><span data-stu-id="772f2-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="772f2-115">이 명령은 ADF라는 리소스 그룹에 대한 구독에서 WikiADF라는 데이터 팩터리에 대한 정보를 표시한 다음, $DataFactory 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="772f2-116">후속 cmdlet에서 DataFactory 매개 변수를 지정하여 데이터 팩터리에 $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="772f2-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="772f2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="772f2-117">PARAMETERS</span></span>

### <span data-ttu-id="772f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772f2-118">-DefaultProfile</span></span>
<span data-ttu-id="772f2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="772f2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="772f2-120">-Name</span></span>
<span data-ttu-id="772f2-121">정보를 얻을 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="772f2-123">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="772f2-124">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772f2-125">CommonParameters</span></span>
<span data-ttu-id="772f2-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="772f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772f2-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="772f2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772f2-128">입력</span><span class="sxs-lookup"><span data-stu-id="772f2-128">INPUTS</span></span>

### <span data-ttu-id="772f2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="772f2-129">System.String</span></span>

## <span data-ttu-id="772f2-130">출력</span><span class="sxs-lookup"><span data-stu-id="772f2-130">OUTPUTS</span></span>

### <span data-ttu-id="772f2-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="772f2-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="772f2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="772f2-132">NOTES</span></span>
<span data-ttu-id="772f2-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="772f2-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="772f2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="772f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="772f2-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="772f2-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="772f2-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="772f2-136">Remove-AzDataFactoryV2</span></span>]()

