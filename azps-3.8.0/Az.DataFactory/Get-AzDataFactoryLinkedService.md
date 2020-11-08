---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042375"
---
# <span data-ttu-id="23ee1-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="23ee1-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="23ee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="23ee1-103">Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="23ee1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23ee1-104">SYNTAX</span></span>

### <span data-ttu-id="23ee1-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="23ee1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ee1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="23ee1-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ee1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="23ee1-107">DESCRIPTION</span></span>
<span data-ttu-id="23ee1-108">**AzDataFactoryLinkedService** Cmdlet은 Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="23ee1-109">연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="23ee1-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="23ee1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="23ee1-111">EXAMPLES</span></span>

### <span data-ttu-id="23ee1-112">예제 1: 연결 된 모든 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="23ee1-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="23ee1-113">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 서비스에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 연결 된 서비스를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23ee1-114">해당 cmdlet은 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="23ee1-115">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="23ee1-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="23ee1-116">예제 2: 연결 된 특정 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="23ee1-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="23ee1-117">이 명령은 WikiADF 이라는 data factory에서 HDILinkedService 라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="23ee1-118">예제 3: DataFactory 매개 변수를 지정 하 여 특정 연결 된 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="23ee1-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="23ee1-119">첫 번째 명령은 Get-AzDataFactory cmdlet을 사용 하 여 ContosoFactory 이라는 data factory를 가져오고이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="23ee1-120">두 번째 명령은 $DataFactory에 저장 된 data factory에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 해당 정보를 Format-Table cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23ee1-121">**Format-테이블** 출력의 형식을 데이터 집합 열로 지정 된 속성을 갖는 데이터 집합으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="23ee1-122">변수</span><span class="sxs-lookup"><span data-stu-id="23ee1-122">PARAMETERS</span></span>

### <span data-ttu-id="23ee1-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="23ee1-123">-DataFactory</span></span>
<span data-ttu-id="23ee1-124">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="23ee1-125">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="23ee1-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="23ee1-126">-DataFactoryName</span></span>
<span data-ttu-id="23ee1-127">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="23ee1-128">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="23ee1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ee1-129">-DefaultProfile</span></span>
<span data-ttu-id="23ee1-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="23ee1-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23ee1-131">-이름</span><span class="sxs-lookup"><span data-stu-id="23ee1-131">-Name</span></span>
<span data-ttu-id="23ee1-132">정보를 가져올 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="23ee1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ee1-133">-ResourceGroupName</span></span>
<span data-ttu-id="23ee1-134">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="23ee1-135">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="23ee1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ee1-136">CommonParameters</span></span>
<span data-ttu-id="23ee1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23ee1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ee1-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ee1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ee1-139">입력</span><span class="sxs-lookup"><span data-stu-id="23ee1-139">INPUTS</span></span>

### <span data-ttu-id="23ee1-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="23ee1-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="23ee1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23ee1-141">System.String</span></span>

## <span data-ttu-id="23ee1-142">출력</span><span class="sxs-lookup"><span data-stu-id="23ee1-142">OUTPUTS</span></span>

### <span data-ttu-id="23ee1-143">DataFactories. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="23ee1-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="23ee1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="23ee1-144">NOTES</span></span>
* <span data-ttu-id="23ee1-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="23ee1-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="23ee1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23ee1-146">RELATED LINKS</span></span>

[<span data-ttu-id="23ee1-147">새로운 AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="23ee1-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="23ee1-148">제거-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="23ee1-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)

