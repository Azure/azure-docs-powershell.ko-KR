---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495605"
---
# <span data-ttu-id="51ced-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51ced-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="51ced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ced-102">SYNOPSIS</span></span>
<span data-ttu-id="51ced-103">데이터 저장소 또는 클라우드 서비스를 Data Factory에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="51ced-104">구문</span><span class="sxs-lookup"><span data-stu-id="51ced-104">SYNTAX</span></span>

### <span data-ttu-id="51ced-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="51ced-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51ced-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51ced-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51ced-107">설명</span><span class="sxs-lookup"><span data-stu-id="51ced-107">DESCRIPTION</span></span>
<span data-ttu-id="51ced-108">이 Set-AzDataFactoryV2LinkedService cmdlet은 데이터 저장소 또는 클라우드 서비스를 Azure Data Factory에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="51ced-109">이미 존재하는 연결된 서비스의 이름을 지정하는 경우 이 cmdlet은 연결된 서비스를 바꾸기 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="51ced-110">Force 매개 변수를 지정하는 경우 cmdlet은 확인 없이 기존 연결된 서비스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="51ced-111">다음 순서로 이러한 작업을 수행 합니다. -- 데이터 팩터리 만들기.</span><span class="sxs-lookup"><span data-stu-id="51ced-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="51ced-112">-- 연결된 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-112">-- Create linked services.</span></span>
<span data-ttu-id="51ced-113">-- 데이터 세트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-113">-- Create datasets.</span></span>
<span data-ttu-id="51ced-114">-- 파이프라인을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="51ced-115">예제</span><span class="sxs-lookup"><span data-stu-id="51ced-115">EXAMPLES</span></span>

### <span data-ttu-id="51ced-116">예제 1: 연결된 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="51ced-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="51ced-117">이 명령은 WikiADF라는 데이터 팩터리에 LinkedServiceCuratedWikiData라는 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="51ced-118">이 연결된 서비스는 파일에 지정된 Azure Blob 저장소를 WikiADF라는 데이터 팩터리에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="51ced-119">이 명령은 파이프라인 연산자를 사용하여 Format-List cmdlet에 결과를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51ced-120">이 Windows PowerShell 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="51ced-121">자세한 내용은 서식 Get-Help 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="51ced-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51ced-122">PARAMETERS</span></span>

### <span data-ttu-id="51ced-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51ced-123">-DataFactoryName</span></span>
<span data-ttu-id="51ced-124">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="51ced-125">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="51ced-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ced-126">-DefaultProfile</span></span>
<span data-ttu-id="51ced-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ced-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="51ced-128">-DefinitionFile</span></span>
<span data-ttu-id="51ced-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ced-130">-Force</span><span class="sxs-lookup"><span data-stu-id="51ced-130">-Force</span></span>
<span data-ttu-id="51ced-131">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ced-132">-Name</span><span class="sxs-lookup"><span data-stu-id="51ced-132">-Name</span></span>
<span data-ttu-id="51ced-133">만들 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51ced-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51ced-134">-ResourceGroupName</span></span>
<span data-ttu-id="51ced-135">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="51ced-136">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51ced-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51ced-137">-ResourceId</span></span>
<span data-ttu-id="51ced-138">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="51ced-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51ced-139">-Confirm</span></span>
<span data-ttu-id="51ced-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ced-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51ced-141">-WhatIf</span></span>
<span data-ttu-id="51ced-142">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ced-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ced-143">CommonParameters</span></span>
<span data-ttu-id="51ced-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51ced-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ced-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="51ced-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ced-146">입력</span><span class="sxs-lookup"><span data-stu-id="51ced-146">INPUTS</span></span>

### <span data-ttu-id="51ced-147">System.String</span><span class="sxs-lookup"><span data-stu-id="51ced-147">System.String</span></span>

## <span data-ttu-id="51ced-148">출력</span><span class="sxs-lookup"><span data-stu-id="51ced-148">OUTPUTS</span></span>

### <span data-ttu-id="51ced-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="51ced-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="51ced-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51ced-150">NOTES</span></span>
<span data-ttu-id="51ced-151">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="51ced-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="51ced-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51ced-152">RELATED LINKS</span></span>

[<span data-ttu-id="51ced-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51ced-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="51ced-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51ced-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
