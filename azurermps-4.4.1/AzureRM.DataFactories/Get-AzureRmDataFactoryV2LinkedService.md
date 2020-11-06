---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8ee5ba855e1c9f9815e9dbcb844ebb23d7118d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527675"
---
# <span data-ttu-id="4eacc-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="4eacc-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="4eacc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eacc-102">SYNOPSIS</span></span>
<span data-ttu-id="4eacc-103">Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eacc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4eacc-104">SYNTAX</span></span>

### <span data-ttu-id="4eacc-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4eacc-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eacc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4eacc-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eacc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4eacc-107">DESCRIPTION</span></span>
<span data-ttu-id="4eacc-108">Get-AzureRmDataFactoryV2LinkedService cmdlet은 Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="4eacc-109">연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="4eacc-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="4eacc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4eacc-111">EXAMPLES</span></span>

### <span data-ttu-id="4eacc-112">예제 1: 연결 된 모든 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eacc-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="4eacc-113">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 서비스에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 연결 된 서비스를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4eacc-114">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="4eacc-115">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="4eacc-116">다음 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="4eacc-117">예제 2: 연결 된 특정 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eacc-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="4eacc-118">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceCuratedWikiData 라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="4eacc-119">예제 3: DataFactory 매개 변수를 지정 하 여 특정 연결 된 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eacc-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="4eacc-120">첫 번째 명령은 Get-AzureRmDataFactoryV2 cmdlet을 사용 하 여 ContosoFactory 이라는 data factory를 가져오고이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="4eacc-121">두 번째 명령은 $DataFactory에 저장 된 data factory에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 해당 정보를 Format-Table cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4eacc-122">Format-Table cmdlet은 출력의 형식을 데이터 집합 열로 지정 된 속성을 갖는 데이터로 데이터 집합으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="4eacc-123">변수</span><span class="sxs-lookup"><span data-stu-id="4eacc-123">PARAMETERS</span></span>

### <span data-ttu-id="4eacc-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4eacc-124">-DataFactory</span></span>
<span data-ttu-id="4eacc-125">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="4eacc-126">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eacc-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4eacc-127">-DataFactoryName</span></span>
<span data-ttu-id="4eacc-128">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4eacc-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4eacc-130">-이름</span><span class="sxs-lookup"><span data-stu-id="4eacc-130">-Name</span></span>
<span data-ttu-id="4eacc-131">정보를 가져올 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eacc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eacc-132">-ResourceGroupName</span></span>
<span data-ttu-id="4eacc-133">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4eacc-134">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4eacc-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eacc-135">-DefaultProfile</span></span>
<span data-ttu-id="4eacc-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eacc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eacc-137">CommonParameters</span></span>
<span data-ttu-id="4eacc-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eacc-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eacc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eacc-140">입력</span><span class="sxs-lookup"><span data-stu-id="4eacc-140">INPUTS</span></span>

### <span data-ttu-id="4eacc-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4eacc-141">System.String</span></span>
<span data-ttu-id="4eacc-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4eacc-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4eacc-143">출력</span><span class="sxs-lookup"><span data-stu-id="4eacc-143">OUTPUTS</span></span>

### <span data-ttu-id="4eacc-144">DataFactoryV2 ' 1 [[Microsoft Azure. PSLinkedService, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4eacc-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4eacc-145">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="4eacc-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="4eacc-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4eacc-146">NOTES</span></span>
<span data-ttu-id="4eacc-147">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="4eacc-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4eacc-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eacc-148">RELATED LINKS</span></span>

[<span data-ttu-id="4eacc-149">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="4eacc-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="4eacc-150">제거-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="4eacc-150">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
