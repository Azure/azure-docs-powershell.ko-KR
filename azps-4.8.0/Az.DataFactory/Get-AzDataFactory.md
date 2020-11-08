---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214179"
---
# <span data-ttu-id="d9ce3-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9ce3-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="d9ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ce3-103">데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="d9ce3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9ce3-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ce3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d9ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ce3-106">**AzDataFactory** Cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="d9ce3-107">Data factory의 이름을 지정 하는 경우이 cmdlet은 해당 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="d9ce3-108">이름을 지정 하지 않으면이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="d9ce3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d9ce3-109">EXAMPLES</span></span>

### <span data-ttu-id="d9ce3-110">예제 1: 모든 데이터 팩토리 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9ce3-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="d9ce3-111">이 명령은 Azure 구독에 있는 모든 데이터 팩터리에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="d9ce3-112">예제 2: 특정 data factory 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9ce3-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="d9ce3-113">이 명령은 ADF 라는 리소스 그룹에 대 한 구독에서 WikiADF 이라는 data factory에 대 한 정보를 표시 한 다음이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="d9ce3-114">후속 cmdlet에서 *DataFactory* 매개 변수를 지정 하 여 $DataFactory에 저장 된 data factory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="d9ce3-115">변수</span><span class="sxs-lookup"><span data-stu-id="d9ce3-115">PARAMETERS</span></span>

### <span data-ttu-id="d9ce3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ce3-116">-DefaultProfile</span></span>
<span data-ttu-id="d9ce3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d9ce3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9ce3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d9ce3-118">-Name</span></span>
<span data-ttu-id="d9ce3-119">정보를 가져올 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ce3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ce3-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9ce3-121">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d9ce3-122">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 팩터리에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ce3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ce3-123">CommonParameters</span></span>
<span data-ttu-id="d9ce3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ce3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ce3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ce3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ce3-126">입력</span><span class="sxs-lookup"><span data-stu-id="d9ce3-126">INPUTS</span></span>

### <span data-ttu-id="d9ce3-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9ce3-127">System.String</span></span>

## <span data-ttu-id="d9ce3-128">출력</span><span class="sxs-lookup"><span data-stu-id="d9ce3-128">OUTPUTS</span></span>

### <span data-ttu-id="d9ce3-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9ce3-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d9ce3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d9ce3-130">NOTES</span></span>
* <span data-ttu-id="d9ce3-131">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d9ce3-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d9ce3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9ce3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9ce3-133">새로운 AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9ce3-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="d9ce3-134">제거-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9ce3-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


