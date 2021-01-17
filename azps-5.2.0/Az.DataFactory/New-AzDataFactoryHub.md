---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324526"
---
# <span data-ttu-id="ee0ea-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ee0ea-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="ee0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0ea-103">Azure Data Factory에 대한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="ee0ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee0ea-104">SYNTAX</span></span>

### <span data-ttu-id="ee0ea-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee0ea-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee0ea-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee0ea-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee0ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="ee0ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ee0ea-108">**New-AzDataFactoryHub** cmdlet은 지정된 Azure 리소스 그룹 및 지정된 파일 정의를 사용하여 지정된 데이터 팩터리에 Azure Data Factory에 대한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="ee0ea-109">허브를 만든 후 허브를 사용하여 그룹에 연결된 서비스를 저장하고 관리할 수 있으며 허브에 파이프라인을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="ee0ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="ee0ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ee0ea-111">예제 1: 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="ee0ea-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="ee0ea-112">이 명령은 리소스 그룹 ADFResourceGroup 및 ADFDataFactory라는 데이터 팩터리에 ContosoDataHub라는 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="ee0ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee0ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ee0ea-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee0ea-114">-DataFactory</span></span>
<span data-ttu-id="ee0ea-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="ee0ea-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ee0ea-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee0ea-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee0ea-117">-DataFactoryName</span></span>
<span data-ttu-id="ee0ea-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee0ea-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee0ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0ea-120">-DefaultProfile</span></span>
<span data-ttu-id="ee0ea-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ee0ea-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee0ea-122">-File</span><span class="sxs-lookup"><span data-stu-id="ee0ea-122">-File</span></span>
<span data-ttu-id="ee0ea-123">허브에 대한 설명이 포함된 JSON(JavaScript Object Notation) 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="ee0ea-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ee0ea-124">-Force</span></span>
<span data-ttu-id="ee0ea-125">확인 메시지를 표시하지 않고 이 cmdlet이 기존 허브를 대체하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ee0ea-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0ea-126">-Name</span></span>
<span data-ttu-id="ee0ea-127">만들 허브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="ee0ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee0ea-129">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee0ea-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee0ea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee0ea-131">-Confirm</span></span>
<span data-ttu-id="ee0ea-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee0ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee0ea-133">-WhatIf</span></span>
<span data-ttu-id="ee0ea-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee0ea-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee0ea-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee0ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0ea-136">CommonParameters</span></span>
<span data-ttu-id="ee0ea-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0ea-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ee0ea-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0ea-139">입력</span><span class="sxs-lookup"><span data-stu-id="ee0ea-139">INPUTS</span></span>

### <span data-ttu-id="ee0ea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee0ea-140">System.String</span></span>

### <span data-ttu-id="ee0ea-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ee0ea-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ee0ea-142">출력</span><span class="sxs-lookup"><span data-stu-id="ee0ea-142">OUTPUTS</span></span>

### <span data-ttu-id="ee0ea-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="ee0ea-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="ee0ea-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee0ea-144">NOTES</span></span>
* <span data-ttu-id="ee0ea-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="ee0ea-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee0ea-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee0ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="ee0ea-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ee0ea-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="ee0ea-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ee0ea-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


