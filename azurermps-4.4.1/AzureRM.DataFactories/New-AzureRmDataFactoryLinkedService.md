---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 9ae1dfe79361e926325b82199469eaf9a9f5d92b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530780"
---
# <span data-ttu-id="dab20-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dab20-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="dab20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab20-102">SYNOPSIS</span></span>
<span data-ttu-id="dab20-103">데이터 저장소 또는 클라우드 서비스를 Azure Data Factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dab20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dab20-104">SYNTAX</span></span>

### <span data-ttu-id="dab20-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dab20-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dab20-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dab20-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab20-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dab20-107">DESCRIPTION</span></span>
<span data-ttu-id="dab20-108">**새로운 AzureRmDataFactoryLinkedService** cmdlet은 데이터 저장소 또는 클라우드 서비스를 Azure data Factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="dab20-109">이미 존재 하는 연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스를 대체 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="dab20-110">*Force* 매개 변수를 지정 하면 cmdlet은 확인 없이 기존에 연결 된 서비스를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="dab20-111">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="dab20-112">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-112">Create a data factory.</span></span> 
- <span data-ttu-id="dab20-113">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-113">Create linked services.</span></span> 
- <span data-ttu-id="dab20-114">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-114">Create datasets.</span></span> 
- <span data-ttu-id="dab20-115">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-115">Create a pipeline.</span></span>

## <span data-ttu-id="dab20-116">예제의</span><span class="sxs-lookup"><span data-stu-id="dab20-116">EXAMPLES</span></span>

### <span data-ttu-id="dab20-117">예제 1: 연결 된 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="dab20-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="dab20-118">이 명령은 WikiADF 이라는 data factory에 LinkedServiceCuratedWikiData 이라는 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="dab20-119">이 연결 된 서비스는 파일에 지정 된 Azure blob 저장소를 WikiADF 이라는 data factory에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="dab20-120">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dab20-121">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="dab20-122">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="dab20-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="dab20-123">변수</span><span class="sxs-lookup"><span data-stu-id="dab20-123">PARAMETERS</span></span>

### <span data-ttu-id="dab20-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dab20-124">-DataFactory</span></span>
<span data-ttu-id="dab20-125">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dab20-126">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dab20-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dab20-127">-DataFactoryName</span></span>
<span data-ttu-id="dab20-128">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dab20-129">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dab20-130">-파일</span><span class="sxs-lookup"><span data-stu-id="dab20-130">-File</span></span>
<span data-ttu-id="dab20-131">연결 된 서비스에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="dab20-132">-Force</span><span class="sxs-lookup"><span data-stu-id="dab20-132">-Force</span></span>
<span data-ttu-id="dab20-133">이 cmdlet이 확인 메시지를 표시 하지 않고 기존에 연결 된 서비스를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-133">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dab20-134">-이름</span><span class="sxs-lookup"><span data-stu-id="dab20-134">-Name</span></span>
<span data-ttu-id="dab20-135">만들 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-135">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="dab20-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab20-136">-ResourceGroupName</span></span>
<span data-ttu-id="dab20-137">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dab20-138">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-138">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dab20-139">-확인</span><span class="sxs-lookup"><span data-stu-id="dab20-139">-Confirm</span></span>
<span data-ttu-id="dab20-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab20-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab20-141">-WhatIf</span></span>
<span data-ttu-id="dab20-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab20-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab20-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab20-144">-DefaultProfile</span></span>
<span data-ttu-id="dab20-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab20-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab20-146">CommonParameters</span></span>
<span data-ttu-id="dab20-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab20-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab20-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab20-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab20-149">입력</span><span class="sxs-lookup"><span data-stu-id="dab20-149">INPUTS</span></span>

## <span data-ttu-id="dab20-150">출력</span><span class="sxs-lookup"><span data-stu-id="dab20-150">OUTPUTS</span></span>

### <span data-ttu-id="dab20-151">WindowsAzure. 유틸리티. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="dab20-151">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="dab20-152">상속자</span><span class="sxs-lookup"><span data-stu-id="dab20-152">NOTES</span></span>
* <span data-ttu-id="dab20-153">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="dab20-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dab20-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dab20-154">RELATED LINKS</span></span>

[<span data-ttu-id="dab20-155">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dab20-155">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="dab20-156">제거-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dab20-156">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


