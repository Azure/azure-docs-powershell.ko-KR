---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5b11273e61689c515cc7ed72f013514fcd309dcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971248"
---
# <span data-ttu-id="37dee-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="37dee-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="37dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dee-102">SYNOPSIS</span></span>
<span data-ttu-id="37dee-103">Azure Data Factory에 데이터 저장소 또는 클라우드 서비스를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="37dee-104">구문</span><span class="sxs-lookup"><span data-stu-id="37dee-104">SYNTAX</span></span>

### <span data-ttu-id="37dee-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="37dee-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37dee-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37dee-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37dee-107">설명</span><span class="sxs-lookup"><span data-stu-id="37dee-107">DESCRIPTION</span></span>
<span data-ttu-id="37dee-108">**New-AzDataFactoryLinkedService** cmdlet은 데이터 저장소 또는 클라우드 서비스를 Azure Data Factory에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="37dee-109">이미 존재하는 연결된 서비스에 대한 이름을 지정하는 경우 이 cmdlet은 연결된 서비스를 대체하기 전에 확인을 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="37dee-110">Force 매개 *변수를 지정하는* 경우 cmdlet은 확인 없이 기존 연결된 서비스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="37dee-111">다음 순서대로 이러한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="37dee-112">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="37dee-112">Create a data factory.</span></span> 
- <span data-ttu-id="37dee-113">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-113">Create linked services.</span></span> 
- <span data-ttu-id="37dee-114">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-114">Create datasets.</span></span> 
- <span data-ttu-id="37dee-115">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-115">Create a pipeline.</span></span>

## <span data-ttu-id="37dee-116">예제</span><span class="sxs-lookup"><span data-stu-id="37dee-116">EXAMPLES</span></span>

### <span data-ttu-id="37dee-117">예제 1: 연결된 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="37dee-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="37dee-118">이 명령은 WikiADF라는 데이터 팩터리에 LinkedServiceCuratedWikiData라는 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="37dee-119">이 연결된 서비스는 파일에 지정된 Azure Blob 저장소를 WikiADF라는 데이터 팩터리에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="37dee-120">명령은 파이프라인 연산자를 사용하여 결과를 Format-List cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37dee-121">cmdlet이 Windows PowerShell 서식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="37dee-122">자세한 내용은 `Get-Help Format-List` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="37dee-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="37dee-123">PARAMETERS</span></span>

### <span data-ttu-id="37dee-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="37dee-124">-DataFactory</span></span>
<span data-ttu-id="37dee-125">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="37dee-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="37dee-126">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="37dee-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="37dee-127">-DataFactoryName</span></span>
<span data-ttu-id="37dee-128">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="37dee-129">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="37dee-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dee-130">-DefaultProfile</span></span>
<span data-ttu-id="37dee-131">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37dee-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37dee-132">-File</span><span class="sxs-lookup"><span data-stu-id="37dee-132">-File</span></span>
<span data-ttu-id="37dee-133">연결된 서비스의 설명이 포함된 JSON(JavaScript 개체 표기)파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dee-134">-Force</span><span class="sxs-lookup"><span data-stu-id="37dee-134">-Force</span></span>
<span data-ttu-id="37dee-135">이 cmdlet은 확인을 요청하지 않고 기존 연결된 서비스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="37dee-136">-Name</span><span class="sxs-lookup"><span data-stu-id="37dee-136">-Name</span></span>
<span data-ttu-id="37dee-137">만들 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="37dee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dee-138">-ResourceGroupName</span></span>
<span data-ttu-id="37dee-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="37dee-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="37dee-141">-확인</span><span class="sxs-lookup"><span data-stu-id="37dee-141">-Confirm</span></span>
<span data-ttu-id="37dee-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dee-143">-WhatIf</span></span>
<span data-ttu-id="37dee-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dee-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dee-146">CommonParameters</span></span>
<span data-ttu-id="37dee-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37dee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dee-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37dee-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dee-149">입력</span><span class="sxs-lookup"><span data-stu-id="37dee-149">INPUTS</span></span>

### <span data-ttu-id="37dee-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="37dee-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="37dee-151">System.String</span><span class="sxs-lookup"><span data-stu-id="37dee-151">System.String</span></span>

## <span data-ttu-id="37dee-152">출력</span><span class="sxs-lookup"><span data-stu-id="37dee-152">OUTPUTS</span></span>

### <span data-ttu-id="37dee-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="37dee-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="37dee-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37dee-154">NOTES</span></span>
* <span data-ttu-id="37dee-155">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="37dee-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37dee-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37dee-156">RELATED LINKS</span></span>

[<span data-ttu-id="37dee-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="37dee-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="37dee-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="37dee-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


