---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: c92f3bf2a124d5fc533fa86914cd218052e71e57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526868"
---
# <span data-ttu-id="f6e0f-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f6e0f-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="f6e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e0f-103">Data Factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6e0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6e0f-104">SYNTAX</span></span>

### <span data-ttu-id="f6e0f-105">BySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6e0f-105">BySubscriptionId (Default)</span></span>
```
Get-AzureRmDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6e0f-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="f6e0f-106">ByFactoryName</span></span>
```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e0f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f6e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e0f-108">Get-AzureRmDataFactoryV2 cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-108">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="f6e0f-109">Data factory의 이름을 지정 하는 경우이 cmdlet은 해당 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="f6e0f-110">이름을 지정 하지 않으면이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="f6e0f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f6e0f-111">EXAMPLES</span></span>

### <span data-ttu-id="f6e0f-112">예제 1: 모든 데이터 팩토리 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6e0f-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="f6e0f-113">Azure 구독에서 모든 데이터 팩터리에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="f6e0f-114">예제 2: 특정 data factory 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6e0f-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="f6e0f-115">이 명령은 ADF 라는 리소스 그룹에 대 한 구독에서 WikiADF 이라는 data factory에 대 한 정보를 표시 한 다음이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="f6e0f-116">후속 cmdlet에서 DataFactory 매개 변수를 지정 하 여 $DataFactory에 저장 된 data factory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="f6e0f-117">변수</span><span class="sxs-lookup"><span data-stu-id="f6e0f-117">PARAMETERS</span></span>

### <span data-ttu-id="f6e0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e0f-118">-DefaultProfile</span></span>
<span data-ttu-id="f6e0f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6e0f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f6e0f-120">-Name</span></span>
<span data-ttu-id="f6e0f-121">정보를 가져올 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e0f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e0f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6e0f-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f6e0f-124">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e0f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e0f-125">CommonParameters</span></span>
<span data-ttu-id="f6e0f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e0f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e0f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e0f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e0f-128">입력</span><span class="sxs-lookup"><span data-stu-id="f6e0f-128">INPUTS</span></span>

### <span data-ttu-id="f6e0f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6e0f-129">System.String</span></span>

## <span data-ttu-id="f6e0f-130">출력</span><span class="sxs-lookup"><span data-stu-id="f6e0f-130">OUTPUTS</span></span>

### <span data-ttu-id="f6e0f-131">DataFactoryV2, [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory Microsoft Azure. 0.1.9.0, Version =, Culture = 중립, PublicKeyToken = null]] 목록의 목록 ' 1</span><span class="sxs-lookup"><span data-stu-id="f6e0f-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f6e0f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f6e0f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f6e0f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f6e0f-133">NOTES</span></span>
<span data-ttu-id="f6e0f-134">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="f6e0f-134">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f6e0f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6e0f-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6e0f-136">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f6e0f-136">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="f6e0f-137">제거-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f6e0f-137">Remove-AzureRmDataFactoryV2</span></span>]()

