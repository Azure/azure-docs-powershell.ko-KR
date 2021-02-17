---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198180"
---
# <span data-ttu-id="8a320-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a320-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="8a320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a320-102">SYNOPSIS</span></span>
<span data-ttu-id="8a320-103">Data Factories에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="8a320-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a320-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a320-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a320-105">DESCRIPTION</span></span>
<span data-ttu-id="8a320-106">**Get-AzDataFactory** cmdlet은 Azure 리소스 그룹의 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="8a320-107">데이터 팩터리의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="8a320-108">이름을 지정하지 않으면 이 cmdlet은 Azure 리소스 그룹의 모든 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="8a320-109">예제</span><span class="sxs-lookup"><span data-stu-id="8a320-109">EXAMPLES</span></span>

### <span data-ttu-id="8a320-110">예제 1: 모든 데이터 팩터리 얻기</span><span class="sxs-lookup"><span data-stu-id="8a320-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="8a320-111">이 명령은 Azure 구독의 모든 데이터 팩터리에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="8a320-112">예제 2: 특정 데이터 팩터리 얻기</span><span class="sxs-lookup"><span data-stu-id="8a320-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="8a320-113">이 명령은 ADF라는 리소스 그룹에 대한 구독에서 WikiADF라는 데이터 팩터리에 대한 정보를 표시한 다음, $DataFactory 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="8a320-114">다음 cmdlet에서 *DataFactory* 매개 변수를 지정하여 데이터 팩터리에 $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="8a320-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="8a320-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a320-115">PARAMETERS</span></span>

### <span data-ttu-id="8a320-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a320-116">-DefaultProfile</span></span>
<span data-ttu-id="8a320-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8a320-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a320-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8a320-118">-Name</span></span>
<span data-ttu-id="8a320-119">정보를 얻을 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="8a320-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a320-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a320-121">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8a320-122">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속한 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a320-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a320-123">CommonParameters</span></span>
<span data-ttu-id="8a320-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a320-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a320-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8a320-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a320-126">입력</span><span class="sxs-lookup"><span data-stu-id="8a320-126">INPUTS</span></span>

### <span data-ttu-id="8a320-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8a320-127">System.String</span></span>

## <span data-ttu-id="8a320-128">출력</span><span class="sxs-lookup"><span data-stu-id="8a320-128">OUTPUTS</span></span>

### <span data-ttu-id="8a320-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a320-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8a320-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a320-130">NOTES</span></span>
* <span data-ttu-id="8a320-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="8a320-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8a320-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a320-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a320-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a320-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="8a320-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a320-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


