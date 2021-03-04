---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975419"
---
# <span data-ttu-id="6b170-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6b170-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="6b170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b170-102">SYNOPSIS</span></span>
<span data-ttu-id="6b170-103">Azure Data Factory에서 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="6b170-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b170-104">SYNTAX</span></span>

### <span data-ttu-id="6b170-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b170-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b170-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6b170-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b170-107">설명</span><span class="sxs-lookup"><span data-stu-id="6b170-107">DESCRIPTION</span></span>
<span data-ttu-id="6b170-108">**Get-AzDataFactoryLinkedService** cmdlet은 Azure Data Factory의 연결된 서비스에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="6b170-109">연결된 서비스의 이름을 지정하는 경우 이 cmdlet은 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="6b170-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="6b170-111">예제</span><span class="sxs-lookup"><span data-stu-id="6b170-111">EXAMPLES</span></span>

### <span data-ttu-id="6b170-112">예제 1: 연결된 모든 서비스에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="6b170-113">이 명령은 WikiADF라는 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 얻은 다음 파이프라인 연산자를 사용하여 연결된 Format-List cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6b170-114">이 cmdlet은 결과를 서식 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="6b170-115">자세한 내용은 `Get-Help Format-List` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="6b170-116">예제 2: 특정 연결된 서비스에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="6b170-117">이 명령은 WikiADF라는 데이터 팩터리에서 HDILinkedService라는 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="6b170-118">예제 3: DataFactory 매개 변수를 지정하여 특정 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="6b170-119">첫 번째 명령은 Get-AzDataFactory cmdlet을 사용하여 ContosoFactory라는 데이터 팩터리를 한 다음, $DataFactory 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="6b170-120">두 번째 명령은 데이터 팩터리에 저장된 데이터 팩터리에 대한 연결된 서비스에 대한 정보를 $DataFactory 파이프라인 연산자를 사용하여 해당 Format-Table cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6b170-121">**Format-Table은** 지정된 속성을 데이터 세트 열로 사용하여 출력을 데이터 세트로 서식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="6b170-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b170-122">PARAMETERS</span></span>

### <span data-ttu-id="6b170-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6b170-123">-DataFactory</span></span>
<span data-ttu-id="6b170-124">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="6b170-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6b170-125">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b170-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6b170-126">-DataFactoryName</span></span>
<span data-ttu-id="6b170-127">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6b170-128">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b170-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b170-129">-DefaultProfile</span></span>
<span data-ttu-id="6b170-130">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6b170-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b170-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6b170-131">-Name</span></span>
<span data-ttu-id="6b170-132">정보를 얻을 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b170-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b170-133">-ResourceGroupName</span></span>
<span data-ttu-id="6b170-134">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6b170-135">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b170-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b170-136">CommonParameters</span></span>
<span data-ttu-id="6b170-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b170-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b170-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6b170-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b170-139">입력</span><span class="sxs-lookup"><span data-stu-id="6b170-139">INPUTS</span></span>

### <span data-ttu-id="6b170-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6b170-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6b170-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6b170-141">System.String</span></span>

## <span data-ttu-id="6b170-142">출력</span><span class="sxs-lookup"><span data-stu-id="6b170-142">OUTPUTS</span></span>

### <span data-ttu-id="6b170-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="6b170-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="6b170-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b170-144">NOTES</span></span>
* <span data-ttu-id="6b170-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="6b170-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6b170-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b170-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b170-147">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6b170-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="6b170-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6b170-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


