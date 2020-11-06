---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 47cbd81fa7e2e8f3877c2e933254cde4e2cee8ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524475"
---
# <span data-ttu-id="55e83-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="55e83-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="55e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e83-102">SYNOPSIS</span></span>
<span data-ttu-id="55e83-103">데이터 저장소 또는 클라우드 서비스를 Data Factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55e83-104">SYNTAX</span></span>

### <span data-ttu-id="55e83-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="55e83-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55e83-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="55e83-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e83-107">설명은</span><span class="sxs-lookup"><span data-stu-id="55e83-107">DESCRIPTION</span></span>
<span data-ttu-id="55e83-108">Set-AzureRmDataFactoryV2LinkedService cmdlet은 데이터 저장소 또는 클라우드 서비스를 Azure Data Factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="55e83-109">이미 존재 하는 연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스를 대체 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="55e83-110">Force 매개 변수를 지정 하면 cmdlet은 확인 없이 기존에 연결 된 서비스를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="55e83-111">다음 순서 대로 이러한 작업을 수행 합니다.--data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="55e83-112">--연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-112">-- Create linked services.</span></span>
<span data-ttu-id="55e83-113">--데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-113">-- Create datasets.</span></span>
<span data-ttu-id="55e83-114">--파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="55e83-115">예제의</span><span class="sxs-lookup"><span data-stu-id="55e83-115">EXAMPLES</span></span>

### <span data-ttu-id="55e83-116">예제 1: 연결 된 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="55e83-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="55e83-117">이 명령은 WikiADF 이라는 data factory에 LinkedServiceCuratedWikiData 이라는 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="55e83-118">이 연결 된 서비스는 파일에 지정 된 Azure blob 저장소를 WikiADF 이라는 data factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="55e83-119">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="55e83-120">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="55e83-121">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="55e83-122">변수</span><span class="sxs-lookup"><span data-stu-id="55e83-122">PARAMETERS</span></span>

### <span data-ttu-id="55e83-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="55e83-123">-DataFactoryName</span></span>
<span data-ttu-id="55e83-124">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="55e83-125">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="55e83-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e83-126">-DefaultProfile</span></span>
<span data-ttu-id="55e83-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e83-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="55e83-128">-DefinitionFile</span></span>
<span data-ttu-id="55e83-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-129">The JSON file path.</span></span>

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

### <span data-ttu-id="55e83-130">-Force</span><span class="sxs-lookup"><span data-stu-id="55e83-130">-Force</span></span>
<span data-ttu-id="55e83-131">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="55e83-132">-이름</span><span class="sxs-lookup"><span data-stu-id="55e83-132">-Name</span></span>
<span data-ttu-id="55e83-133">만들 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="55e83-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e83-134">-ResourceGroupName</span></span>
<span data-ttu-id="55e83-135">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="55e83-136">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="55e83-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55e83-137">-ResourceId</span></span>
<span data-ttu-id="55e83-138">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="55e83-139">-확인</span><span class="sxs-lookup"><span data-stu-id="55e83-139">-Confirm</span></span>
<span data-ttu-id="55e83-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e83-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e83-141">-WhatIf</span></span>
<span data-ttu-id="55e83-142">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="55e83-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e83-143">CommonParameters</span></span>
<span data-ttu-id="55e83-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e83-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e83-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e83-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e83-146">입력</span><span class="sxs-lookup"><span data-stu-id="55e83-146">INPUTS</span></span>

### <span data-ttu-id="55e83-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55e83-147">System.String</span></span>

## <span data-ttu-id="55e83-148">출력</span><span class="sxs-lookup"><span data-stu-id="55e83-148">OUTPUTS</span></span>

### <span data-ttu-id="55e83-149">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="55e83-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="55e83-150">상속자</span><span class="sxs-lookup"><span data-stu-id="55e83-150">NOTES</span></span>
<span data-ttu-id="55e83-151">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="55e83-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="55e83-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55e83-152">RELATED LINKS</span></span>

[<span data-ttu-id="55e83-153">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="55e83-153">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="55e83-154">제거-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="55e83-154">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()