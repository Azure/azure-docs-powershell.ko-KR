---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: dc6315c16072a736c0db10df6615efb1696b78f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697052"
---
# <span data-ttu-id="b6e80-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b6e80-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b6e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e80-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e80-103">Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="b6e80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6e80-104">SYNTAX</span></span>

### <span data-ttu-id="b6e80-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6e80-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e80-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b6e80-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e80-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e80-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6e80-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6e80-108">DESCRIPTION</span></span>
<span data-ttu-id="b6e80-109">Get-AzDataFactoryV2LinkedService cmdlet은 Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="b6e80-110">연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="b6e80-111">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="b6e80-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b6e80-112">EXAMPLES</span></span>

### <span data-ttu-id="b6e80-113">예제 1: 연결 된 모든 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6e80-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="b6e80-114">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 서비스에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 연결 된 서비스를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b6e80-115">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b6e80-116">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="b6e80-117">다음 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="b6e80-118">예제 2: 연결 된 특정 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6e80-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b6e80-119">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceCuratedWikiData 라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b6e80-120">예제 3: DataFactory 매개 변수를 지정 하 여 특정 연결 된 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6e80-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="b6e80-121">첫 번째 명령은 Get-AzDataFactoryV2 cmdlet을 사용 하 여 ContosoFactory 이라는 data factory를 가져오고이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b6e80-122">두 번째 명령은 $DataFactory에 저장 된 data factory에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 해당 정보를 Format-Table cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b6e80-123">Format-Table cmdlet은 출력의 형식을 데이터 집합 열로 지정 된 속성을 갖는 데이터로 데이터 집합으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="b6e80-124">변수</span><span class="sxs-lookup"><span data-stu-id="b6e80-124">PARAMETERS</span></span>

### <span data-ttu-id="b6e80-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6e80-125">-DataFactory</span></span>
<span data-ttu-id="b6e80-126">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b6e80-127">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6e80-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b6e80-128">-DataFactoryName</span></span>
<span data-ttu-id="b6e80-129">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b6e80-130">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6e80-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e80-131">-DefaultProfile</span></span>
<span data-ttu-id="b6e80-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6e80-133">-이름</span><span class="sxs-lookup"><span data-stu-id="b6e80-133">-Name</span></span>
<span data-ttu-id="b6e80-134">정보를 가져올 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e80-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e80-135">-ResourceGroupName</span></span>
<span data-ttu-id="b6e80-136">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b6e80-137">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6e80-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e80-138">-ResourceId</span></span>
<span data-ttu-id="b6e80-139">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-139">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e80-140">CommonParameters</span></span>
<span data-ttu-id="b6e80-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e80-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e80-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e80-143">입력</span><span class="sxs-lookup"><span data-stu-id="b6e80-143">INPUTS</span></span>

### <span data-ttu-id="b6e80-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6e80-144">System.String</span></span>

### <span data-ttu-id="b6e80-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b6e80-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b6e80-146">출력</span><span class="sxs-lookup"><span data-stu-id="b6e80-146">OUTPUTS</span></span>

### <span data-ttu-id="b6e80-147">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="b6e80-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="b6e80-148">상속자</span><span class="sxs-lookup"><span data-stu-id="b6e80-148">NOTES</span></span>
<span data-ttu-id="b6e80-149">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="b6e80-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b6e80-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6e80-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6e80-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b6e80-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b6e80-152">제거-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b6e80-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
