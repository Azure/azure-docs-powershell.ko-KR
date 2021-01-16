---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372338"
---
# <span data-ttu-id="bd360-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="bd360-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="bd360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd360-102">SYNOPSIS</span></span>
<span data-ttu-id="bd360-103">Azure Data Factory에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="bd360-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd360-104">SYNTAX</span></span>

### <span data-ttu-id="bd360-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd360-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd360-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bd360-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd360-107">설명</span><span class="sxs-lookup"><span data-stu-id="bd360-107">DESCRIPTION</span></span>
<span data-ttu-id="bd360-108">**Remove-AzDataFactoryLinkedService** cmdlet은 Azure Data Factory에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="bd360-109">예제</span><span class="sxs-lookup"><span data-stu-id="bd360-109">EXAMPLES</span></span>

### <span data-ttu-id="bd360-110">예제 1: 연결된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="bd360-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="bd360-111">이 명령은 WikiADF라는 데이터 팩터리에서 LinkedServiceTest라는 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="bd360-112">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="bd360-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="bd360-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd360-113">PARAMETERS</span></span>

### <span data-ttu-id="bd360-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bd360-114">-DataFactory</span></span>
<span data-ttu-id="bd360-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="bd360-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bd360-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd360-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bd360-117">-DataFactoryName</span></span>
<span data-ttu-id="bd360-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bd360-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd360-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd360-120">-DefaultProfile</span></span>
<span data-ttu-id="bd360-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd360-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd360-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bd360-122">-Force</span></span>
<span data-ttu-id="bd360-123">이 cmdlet이 확인 메시지를 표시하지 않고 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bd360-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bd360-124">-Name</span></span>
<span data-ttu-id="bd360-125">제거할 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd360-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd360-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd360-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bd360-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd360-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd360-129">-Confirm</span></span>
<span data-ttu-id="bd360-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd360-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd360-131">-WhatIf</span></span>
<span data-ttu-id="bd360-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd360-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd360-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd360-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd360-134">CommonParameters</span></span>
<span data-ttu-id="bd360-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd360-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd360-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd360-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd360-137">입력</span><span class="sxs-lookup"><span data-stu-id="bd360-137">INPUTS</span></span>

### <span data-ttu-id="bd360-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bd360-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bd360-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bd360-139">System.String</span></span>

## <span data-ttu-id="bd360-140">출력</span><span class="sxs-lookup"><span data-stu-id="bd360-140">OUTPUTS</span></span>

### <span data-ttu-id="bd360-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="bd360-141">System.Void</span></span>

## <span data-ttu-id="bd360-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd360-142">NOTES</span></span>
* <span data-ttu-id="bd360-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="bd360-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bd360-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd360-144">RELATED LINKS</span></span>

[<span data-ttu-id="bd360-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="bd360-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="bd360-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="bd360-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


