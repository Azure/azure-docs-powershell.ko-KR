---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525216"
---
# <span data-ttu-id="95faf-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="95faf-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="95faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95faf-102">SYNOPSIS</span></span>
<span data-ttu-id="95faf-103">데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95faf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95faf-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95faf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95faf-105">DESCRIPTION</span></span>
<span data-ttu-id="95faf-106">**AzureRmDataFactory** Cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="95faf-107">Data factory의 이름을 지정 하는 경우이 cmdlet은 해당 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="95faf-108">이름을 지정 하지 않으면이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="95faf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95faf-109">EXAMPLES</span></span>

### <span data-ttu-id="95faf-110">예제 1: 모든 데이터 팩토리 가져오기</span><span class="sxs-lookup"><span data-stu-id="95faf-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="95faf-111">이 명령은 Azure 구독에 있는 모든 데이터 팩터리에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="95faf-112">예제 2: 특정 data factory 가져오기</span><span class="sxs-lookup"><span data-stu-id="95faf-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="95faf-113">이 명령은 ADF 라는 리소스 그룹에 대 한 구독에서 WikiADF 이라는 data factory에 대 한 정보를 표시 한 다음이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="95faf-114">후속 cmdlet에서 *DataFactory* 매개 변수를 지정 하 여 $DataFactory에 저장 된 data factory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="95faf-115">변수</span><span class="sxs-lookup"><span data-stu-id="95faf-115">PARAMETERS</span></span>

### <span data-ttu-id="95faf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95faf-116">-DefaultProfile</span></span>
<span data-ttu-id="95faf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95faf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95faf-118">-이름</span><span class="sxs-lookup"><span data-stu-id="95faf-118">-Name</span></span>
<span data-ttu-id="95faf-119">정보를 가져올 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95faf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95faf-120">-ResourceGroupName</span></span>
<span data-ttu-id="95faf-121">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="95faf-122">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="95faf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95faf-123">CommonParameters</span></span>
<span data-ttu-id="95faf-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95faf-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95faf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95faf-126">입력</span><span class="sxs-lookup"><span data-stu-id="95faf-126">INPUTS</span></span>

### <span data-ttu-id="95faf-127">않아야</span><span class="sxs-lookup"><span data-stu-id="95faf-127">None</span></span>
<span data-ttu-id="95faf-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95faf-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95faf-129">출력</span><span class="sxs-lookup"><span data-stu-id="95faf-129">OUTPUTS</span></span>

### <span data-ttu-id="95faf-130">System.webserver. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory 0.8.2.0, Microsoft WindowsAzure. 유틸리티, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="95faf-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="95faf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="95faf-131">NOTES</span></span>
* <span data-ttu-id="95faf-132">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="95faf-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="95faf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95faf-133">RELATED LINKS</span></span>

[<span data-ttu-id="95faf-134">새로운 AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="95faf-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="95faf-135">제거-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="95faf-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


