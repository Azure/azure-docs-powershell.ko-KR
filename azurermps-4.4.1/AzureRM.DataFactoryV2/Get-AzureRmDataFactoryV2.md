---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531806"
---
# <span data-ttu-id="5ea89-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5ea89-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="5ea89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea89-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea89-103">Data Factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ea89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ea89-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="5ea89-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ea89-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea89-106">Get-AzureRmDataFactoryV2 cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5ea89-107">Data factory의 이름을 지정 하는 경우이 cmdlet은 해당 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5ea89-108">이름을 지정 하지 않으면이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="5ea89-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5ea89-109">EXAMPLES</span></span>

### <span data-ttu-id="5ea89-110">예제 1: 모든 데이터 팩토리 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ea89-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="5ea89-111">Azure 구독에서 모든 데이터 팩터리에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5ea89-112">예제 2: 특정 data factory 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ea89-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="5ea89-113">이 명령은 ADF 라는 리소스 그룹에 대 한 구독에서 WikiADF 이라는 data factory에 대 한 정보를 표시 한 다음이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5ea89-114">후속 cmdlet에서 DataFactory 매개 변수를 지정 하 여 $DataFactory에 저장 된 data factory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5ea89-115">변수</span><span class="sxs-lookup"><span data-stu-id="5ea89-115">PARAMETERS</span></span>

### <span data-ttu-id="5ea89-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5ea89-116">-Name</span></span>
<span data-ttu-id="5ea89-117">정보를 가져올 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea89-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea89-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ea89-119">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5ea89-120">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea89-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="5ea89-121">입력</span><span class="sxs-lookup"><span data-stu-id="5ea89-121">INPUTS</span></span>

### <span data-ttu-id="5ea89-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ea89-122">System.String</span></span>


## <span data-ttu-id="5ea89-123">출력</span><span class="sxs-lookup"><span data-stu-id="5ea89-123">OUTPUTS</span></span>

### <span data-ttu-id="5ea89-124">DataFactoryV2, [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory Microsoft Azure. 0.1.9.0, Version =, Culture = 중립, PublicKeyToken = null]] 목록의 목록 ' 1</span><span class="sxs-lookup"><span data-stu-id="5ea89-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5ea89-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea89-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="5ea89-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5ea89-126">NOTES</span></span>
<span data-ttu-id="5ea89-127">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="5ea89-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ea89-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ea89-128">RELATED LINKS</span></span>
[<span data-ttu-id="5ea89-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5ea89-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="5ea89-130">제거-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5ea89-130">Remove-AzureRmDataFactoryV2</span></span>]()

