---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372870"
---
# <span data-ttu-id="53c40-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="53c40-101">New-AzDataFactory</span></span>

## <span data-ttu-id="53c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c40-102">SYNOPSIS</span></span>
<span data-ttu-id="53c40-103">데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-103">Creates a data factory.</span></span>

## <span data-ttu-id="53c40-104">구문</span><span class="sxs-lookup"><span data-stu-id="53c40-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53c40-105">설명</span><span class="sxs-lookup"><span data-stu-id="53c40-105">DESCRIPTION</span></span>
<span data-ttu-id="53c40-106">**New-AzDataFactory** cmdlet은 지정된 리소스 그룹 이름 및 위치를 사용하여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="53c40-107">다음 순서로 이러한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="53c40-108">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="53c40-108">Create a data factory.</span></span> 
- <span data-ttu-id="53c40-109">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-109">Create linked services.</span></span> 
- <span data-ttu-id="53c40-110">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-110">Create datasets.</span></span> 
- <span data-ttu-id="53c40-111">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-111">Create a pipeline.</span></span>

## <span data-ttu-id="53c40-112">예제</span><span class="sxs-lookup"><span data-stu-id="53c40-112">EXAMPLES</span></span>

### <span data-ttu-id="53c40-113">예제 1: 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="53c40-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="53c40-114">이 명령은 WestUS 위치의 ADF라는 리소스 그룹에 WikiADF라는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="53c40-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c40-115">PARAMETERS</span></span>

### <span data-ttu-id="53c40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c40-116">-DefaultProfile</span></span>
<span data-ttu-id="53c40-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="53c40-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53c40-118">-Force</span><span class="sxs-lookup"><span data-stu-id="53c40-118">-Force</span></span>
<span data-ttu-id="53c40-119">확인 메시지를 표시하지 않고 이 cmdlet이 기존 데이터 팩터리로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="53c40-120">-Location</span><span class="sxs-lookup"><span data-stu-id="53c40-120">-Location</span></span>
<span data-ttu-id="53c40-121">WestUS 또는 EastUS와 같은 데이터 팩터리의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="53c40-122">현재 WestUS만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-122">Only WestUS is currently supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c40-123">-Name</span><span class="sxs-lookup"><span data-stu-id="53c40-123">-Name</span></span>
<span data-ttu-id="53c40-124">만들 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c40-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c40-125">-ResourceGroupName</span></span>
<span data-ttu-id="53c40-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="53c40-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53c40-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="53c40-128">-Tag</span></span>
<span data-ttu-id="53c40-129">데이터 팩터리의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c40-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53c40-130">-Confirm</span></span>
<span data-ttu-id="53c40-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c40-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c40-132">-WhatIf</span></span>
<span data-ttu-id="53c40-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53c40-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c40-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c40-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c40-135">CommonParameters</span></span>
<span data-ttu-id="53c40-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53c40-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c40-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="53c40-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c40-138">입력</span><span class="sxs-lookup"><span data-stu-id="53c40-138">INPUTS</span></span>

### <span data-ttu-id="53c40-139">System.String</span><span class="sxs-lookup"><span data-stu-id="53c40-139">System.String</span></span>

### <span data-ttu-id="53c40-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53c40-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53c40-141">출력</span><span class="sxs-lookup"><span data-stu-id="53c40-141">OUTPUTS</span></span>

### <span data-ttu-id="53c40-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="53c40-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="53c40-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53c40-143">NOTES</span></span>
* <span data-ttu-id="53c40-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="53c40-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="53c40-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53c40-145">RELATED LINKS</span></span>

[<span data-ttu-id="53c40-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="53c40-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="53c40-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="53c40-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


