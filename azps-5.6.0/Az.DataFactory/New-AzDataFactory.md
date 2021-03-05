---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975008"
---
# <span data-ttu-id="0734b-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0734b-101">New-AzDataFactory</span></span>

## <span data-ttu-id="0734b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0734b-102">SYNOPSIS</span></span>
<span data-ttu-id="0734b-103">데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-103">Creates a data factory.</span></span>

## <span data-ttu-id="0734b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0734b-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0734b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0734b-105">DESCRIPTION</span></span>
<span data-ttu-id="0734b-106">**New-AzDataFactory** cmdlet은 지정된 리소스 그룹 이름 및 위치를 사용하여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="0734b-107">다음 순서대로 이러한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="0734b-108">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="0734b-108">Create a data factory.</span></span> 
- <span data-ttu-id="0734b-109">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-109">Create linked services.</span></span> 
- <span data-ttu-id="0734b-110">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-110">Create datasets.</span></span> 
- <span data-ttu-id="0734b-111">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-111">Create a pipeline.</span></span>

## <span data-ttu-id="0734b-112">예제</span><span class="sxs-lookup"><span data-stu-id="0734b-112">EXAMPLES</span></span>

### <span data-ttu-id="0734b-113">예제 1: 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="0734b-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="0734b-114">이 명령은 WestUS 위치의 ADF라는 리소스 그룹에 WikiADF라는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="0734b-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0734b-115">PARAMETERS</span></span>

### <span data-ttu-id="0734b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0734b-116">-DefaultProfile</span></span>
<span data-ttu-id="0734b-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0734b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0734b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0734b-118">-Force</span></span>
<span data-ttu-id="0734b-119">확인을 요청하지 않고 이 cmdlet이 기존 데이터 팩터리로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0734b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="0734b-120">-Location</span></span>
<span data-ttu-id="0734b-121">WestUS 또는 EastUS와 같은 데이터 팩터리의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="0734b-122">현재 WestUS만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="0734b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0734b-123">-Name</span></span>
<span data-ttu-id="0734b-124">만들 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="0734b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0734b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0734b-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0734b-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0734b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0734b-128">-Tag</span></span>
<span data-ttu-id="0734b-129">데이터 팩터리의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="0734b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0734b-130">-Confirm</span></span>
<span data-ttu-id="0734b-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0734b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0734b-132">-WhatIf</span></span>
<span data-ttu-id="0734b-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0734b-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0734b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0734b-135">CommonParameters</span></span>
<span data-ttu-id="0734b-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0734b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0734b-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0734b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0734b-138">입력</span><span class="sxs-lookup"><span data-stu-id="0734b-138">INPUTS</span></span>

### <span data-ttu-id="0734b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0734b-139">System.String</span></span>

### <span data-ttu-id="0734b-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0734b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0734b-141">출력</span><span class="sxs-lookup"><span data-stu-id="0734b-141">OUTPUTS</span></span>

### <span data-ttu-id="0734b-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0734b-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0734b-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0734b-143">NOTES</span></span>
* <span data-ttu-id="0734b-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="0734b-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0734b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0734b-145">RELATED LINKS</span></span>

[<span data-ttu-id="0734b-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0734b-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="0734b-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0734b-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


