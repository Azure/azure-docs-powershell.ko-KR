---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333645"
---
# <span data-ttu-id="24f89-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="24f89-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="24f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f89-102">SYNOPSIS</span></span>
<span data-ttu-id="24f89-103">Data Factory의 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="24f89-104">구문</span><span class="sxs-lookup"><span data-stu-id="24f89-104">SYNTAX</span></span>

### <span data-ttu-id="24f89-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="24f89-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f89-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="24f89-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f89-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24f89-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24f89-108">설명</span><span class="sxs-lookup"><span data-stu-id="24f89-108">DESCRIPTION</span></span>
<span data-ttu-id="24f89-109">Get-AzDataFactoryV2LinkedService cmdlet은 Azure Data Factory의 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="24f89-110">연결된 서비스의 이름을 지정하는 경우 이 cmdlet은 해당 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="24f89-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="24f89-112">예제</span><span class="sxs-lookup"><span data-stu-id="24f89-112">EXAMPLES</span></span>

### <span data-ttu-id="24f89-113">예제 1: 모든 연결된 서비스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="24f89-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="24f89-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 구한 다음, 파이프라인 연산자를 사용하여 Format-List cmdlet에 연결된 서비스를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24f89-115">이 Windows PowerShell 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="24f89-116">자세한 내용은 서식 Get-Help 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="24f89-117">다음 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="24f89-118">예제 2: 특정 연결된 서비스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="24f89-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="24f89-119">이 명령은 WikiADF라는 데이터 팩터리에서 LinkedServiceCuratedWikiData라는 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="24f89-120">예제 3: DataFactory 매개 변수를 지정하여 특정 연결된 서비스에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="24f89-121">첫 번째 명령은 Get-AzDataFactoryV2 cmdlet을 사용하여 ContosoFactory라는 데이터 팩터리를 한 다음, $DataFactory 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="24f89-122">두 번째 명령은 파이프라인 연산자를 사용하여 $DataFactory 데이터 팩터리에 대한 연결된 서비스에 대한 정보를 Format-Table cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24f89-123">이 Format-Table cmdlet은 지정된 속성을 데이터 세트 열로 사용하여 출력을 데이터 세트로 포맷합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="24f89-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24f89-124">PARAMETERS</span></span>

### <span data-ttu-id="24f89-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="24f89-125">-DataFactory</span></span>
<span data-ttu-id="24f89-126">PSDataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="24f89-127">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="24f89-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24f89-128">-DataFactoryName</span></span>
<span data-ttu-id="24f89-129">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="24f89-130">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="24f89-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f89-131">-DefaultProfile</span></span>
<span data-ttu-id="24f89-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f89-133">-Name</span><span class="sxs-lookup"><span data-stu-id="24f89-133">-Name</span></span>
<span data-ttu-id="24f89-134">정보를 얻을 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="24f89-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f89-135">-ResourceGroupName</span></span>
<span data-ttu-id="24f89-136">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="24f89-137">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 연결된 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="24f89-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f89-138">-ResourceId</span></span>
<span data-ttu-id="24f89-139">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24f89-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f89-140">CommonParameters</span></span>
<span data-ttu-id="24f89-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24f89-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f89-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="24f89-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f89-143">입력</span><span class="sxs-lookup"><span data-stu-id="24f89-143">INPUTS</span></span>

### <span data-ttu-id="24f89-144">System.String</span><span class="sxs-lookup"><span data-stu-id="24f89-144">System.String</span></span>

### <span data-ttu-id="24f89-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="24f89-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="24f89-146">출력</span><span class="sxs-lookup"><span data-stu-id="24f89-146">OUTPUTS</span></span>

### <span data-ttu-id="24f89-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="24f89-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="24f89-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24f89-148">NOTES</span></span>
<span data-ttu-id="24f89-149">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="24f89-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="24f89-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24f89-150">RELATED LINKS</span></span>

[<span data-ttu-id="24f89-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="24f89-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="24f89-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="24f89-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
